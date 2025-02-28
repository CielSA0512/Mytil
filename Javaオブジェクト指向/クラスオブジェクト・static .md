# 〇クラスオブジェクトとは
**Java実行時のロードで、メモリ上に生成されるファイル情報[^1]を格納しているメモリ領域のこと**
- クラスオブジェクトでは「ファイル情報」「フィールド」「メソッド」を保有することが可能
- フィールドを**クラス変数**、メソッドを**クラスメソッド**、合わせて**静的メンバ**[^2]と言う
- クラスオブジェクトは変数名としてクラス名が使われるので「**クラス名.〇〇**」でアクセス可能
- クラスオブジェクトのメンバはすべてのインスタンスからアクセス可能で、すべてのインスタンス間で共有的に使われる
  
  [![Image from Gyazo](https://i.gyazo.com/7f99c9cdfbb9c601fb1cd8604977921f.png)](https://gyazo.com/7f99c9cdfbb9c601fb1cd8604977921f)\
  ※値は同じ

[^1]:インスタンスの元
[^2]:静的メンバはクラスオブジェクトで管理されるため、インスタンス化の際に複製されない。\
クラスで固有、すべてのインスタンスで共通のものとして扱われる

**⇒ Javaが実行されたタイミングで、常に使えるようにあらかじめ確保されたメモリ領域のこと**

# 〇staticとは
- 修飾子のひとつ
- これをつけた変数やメソッドは、静的メンバとして扱える
  [![Image from Gyazo](https://i.gyazo.com/991a20b6f86e89e15de0870c5abec007.png)](https://gyazo.com/991a20b6f86e89e15de0870c5abec007)

#### ※mainメソッドはJVMから呼び出され、プログラム終了まで動作し続ける必要があり、クラスオブジェクトの生成のみで使用できるようにstaticが付けられている
  
- 静的メンバは「**インスタンス名.〇〇**」のように、インスタンスから自分の物のようにアクセス可
  [![Image from Gyazo](https://i.gyazo.com/1a7a5911f17ba5db1be63cc8f7f126b7.png)](https://gyazo.com/1a7a5911f17ba5db1be63cc8f7f126b7)
  
- Java実行時点で既にメモリ上に存在する\
  ⇒ 通常のメンバと違い**インスタンス化せずに使用可能**

**⇒ staticをつけると、変数やメソッドはJava実行時のロードで、いつでも使える状態になる**

# 〇staticの扱いの注意点
### --- エラーパターン ---
「**staticがついてないメソッドを参照しようとして、存在しなかったため参照できなかった**」
  [![Image from Gyazo](https://i.gyazo.com/8b16ebc5f7a5c9146299f32db85014bf.png)](https://gyazo.com/8b16ebc5f7a5c9146299f32db85014bf)
  [![Image from Gyazo](https://i.gyazo.com/489db1d8bf872b17af4f2aaca172cf50.png)](https://gyazo.com/489db1d8bf872b17af4f2aaca172cf50)

### --- 解説 ---
#### ①「Sample2_06_2」をコンパイル時に、mainメソッドの7行目で、「calcSizeTriangle」メソッドが呼び出されている
#### ②「calcSizeTriangle」メソッドはstaticがついてないため、コンパイル時にクラスオブジェクトには存在しない
#### ③クラスオブジェクトに存在しないものを参照しようとしているため、エラーが発生
#### ④12行目で「static」をつけると解決するが・・・・
  [![Image from Gyazo](https://i.gyazo.com/1828dd6aabdf7a2be950fab24ba557b7.png)](https://gyazo.com/1828dd6aabdf7a2be950fab24ba557b7)
#### ⑤メモリを使う分だけ消費する「インスタンス化」とは異なり、staticは余分に消費するため、大規模開発の場合、メモリをかなり喰ってしまい、障害のもとになるかもしれない
#### ⑥なので、インスタンス化の特性を活用することで、解決するのが望ましい
  [![Image from Gyazo](https://i.gyazo.com/bff4175affe04d9b8b2ca57b428b9d84.png)](https://gyazo.com/bff4175affe04d9b8b2ca57b428b9d84)
