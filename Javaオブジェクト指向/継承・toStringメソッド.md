# 〇継承とは
- 継承元のクラス（スーパークラス）の機能を引き継いで、継承先のクラス（サブクラス）を作成すること
- スーパークラスのフィールドやメソッドを引き継ぎながら、システムを拡張するときに必要なものだけ追加していくプログラミングを実現可能
- 「**class サブクラス名 extends スーパークラス名 { }**」で表現
  [![Image from Gyazo](https://i.gyazo.com/43b6e02078cce4adf19b51454a5f2f68.png)](https://gyazo.com/43b6e02078cce4adf19b51454a5f2f68)  
- Javaは単一継承のみが認められており、一つのクラスが複数のスーパークラスをもつことはダイヤモンド問題[^1]を引き起こす可能性があるためできない。

  **※コンストラクタはそのクラス固有のメソッドのため、コンストラクタは継承されない**

[^1]:複数のクラスをスーパークラスに指定すると、コンパイラはどのスーパークラスのメソッドを実行するかわからなくなり、あいまいさが生じてしまう問題のこと

## --- 継承関係を持つクラスのコンストラクタの動き ---
- スーパークラスのフィールドの初期化をする際は、スーパークラスのコンストラクタを呼び出す必要がある\
「**super(引数)**」を用いてサブクラス内にスーパークラスのコンストラクタを明示的に呼び出すことが可能\
[![Image from Gyazo](https://i.gyazo.com/a39271953645f1d007cc2523465a7d4b.png)](https://gyazo.com/a39271953645f1d007cc2523465a7d4b)\
この画像の「super(v)」は親クラスである「Sample2_05_1_Dog」のコンストラクタ(下記画像)が呼び出される\
[![Image from Gyazo](https://i.gyazo.com/0a20382b6125a2d941ec99a8304b5ec4.png)](https://gyazo.com/0a20382b6125a2d941ec99a8304b5ec4)

- コンストラクタの中で他のコンストラクタを呼び出す際はその先頭で呼び出さなければならないという仕様から、一つのコンストラクタ内でsuperやthisを二つ以上使用できない\
[![Image from Gyazo](https://i.gyazo.com/89365538df7e0741112da79c3a32bec0.png)](https://gyazo.com/89365538df7e0741112da79c3a32bec0)
  
- サブクラスのコンストラクタでスーパークラスの呼び出し処理を記述しなかった場合、処理の先頭で暗黙的に「super();」（引数なしのスーパークラスのコンストラクタの呼び出し）が実行される。(デフォルトコンストラクトっぽいやつ)\
  [![Image from Gyazo](https://i.gyazo.com/56d564019b306d2852955e99fddbc959.png)](https://gyazo.com/56d564019b306d2852955e99fddbc959)
[![Image from Gyazo](https://i.gyazo.com/fd16b5a1dc0b1b17c475f3b0942d5d55.png)](https://gyazo.com/fd16b5a1dc0b1b17c475f3b0942d5d55)

# 〇オーバーライド
- スーパークラスのメンバをサブクラス側で同じ名前で再定義すること

#### （Carクラスは親[スーパークラス]で、FireTruckクラスは子[サブクラス]）
[![Image from Gyazo](https://i.gyazo.com/0f565d70c6e4de000ad033e5fa0c69e5.png)](https://gyazo.com/0f565d70c6e4de000ad033e5fa0c69e5)

[![Image from Gyazo](https://i.gyazo.com/cd1ee9f42872884dc2cfb2a6f7aa0f5b.png)](https://gyazo.com/cd1ee9f42872884dc2cfb2a6f7aa0f5b)

#### 青枠の部分は、親クラスで定義された「accelerator」メソッドを再定義 ⇒ オーバーライド

## --- オーバーライドのルール --- 
- オーバーライドするスーパークラスのメソッドとメソッド名、戻り値の型、引数および方が同じあること
- スーパークラスのメソッドとアクセス制御が同じか緩い

# 〇toStringメソッド
## --- インスタンス名を呼び出すとどうなるのか？ ---
### < System.out.println( インスタンス名.name ) >
[![Image from Gyazo](https://i.gyazo.com/1b6d093e09addd0e1365503836356b91.png)](https://gyazo.com/1b6d093e09addd0e1365503836356b91)

#### 出力：「 MOCO 」

### < System.out.println( インスタンス名 ) >
[![Image from Gyazo](https://i.gyazo.com/a76efa97161439e238773a8c23fdcfa0.png)](https://gyazo.com/a76efa97161439e238773a8c23fdcfa0)

#### 出力：「 Sample2_05_3_ToyPoodle@54bedef2 」

## --- 結果 ---
#### 「System.out.println( インスタンス名 )」の場合、インスタンスが保存された場所の情報が出力
## --- なぜ？ ---
#### ① Javaの全クラスは「Java.lang.Object」クラスを暗黙的に継承している。
#### ② そのため、Objectクラスで定義されたメソッドはどんなインスタンスでも使用可能
#### ③ Objectクラスでは、「toStringメソッド（インスタンスを文字列として表現した結果を返す）」が定義されている
#### ④ この「toStringメソッド」は「クラス名@ハッシュコード(インスタンスの場所情報)」を戻り値として返すため、場所情報が出力されてしまった
## --- どうしたら、場所情報ではなく名前が表示されるか？ ---
### 「toStringメソッド」を" オーバーライド "して、そのクラス固有の情報を戻り値として返すよう再定義することが必要

[![Image from Gyazo](https://i.gyazo.com/0c482b33623315aec4dfad9bdba74170.png)](https://gyazo.com/0c482b33623315aec4dfad9bdba74170)
[![Image from Gyazo](https://i.gyazo.com/79a4a7ed9badb107ed27c0fdaf1f44d4.png)](https://gyazo.com/79a4a7ed9badb107ed27c0fdaf1f44d4)
