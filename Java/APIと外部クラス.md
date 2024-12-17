## 〇APIとは
- API(Application Program Interface)とは。Javaが提供する便利なソースコード群で、高度で複雑なプログラムを実装することが可能になる。
  ex.) printlnメソッド、parseIntメソッド etc.

- 「https://docs.oracle.com/javase/jp/8/docs/api/
  」で、APIにどんなクラスやメソッドが存在するか確認可能。

### APIの格納場所
- 「JDK(Java開発環境)のフォルダ > JRE(Java実行環境) > lib > rt.jar」(2018年)

### APIの使い方

#### <インポート>
- APIはパッケージと呼ばれるフォルダに管理されており、使用したいクラスをインポートすることで使用可能になる。

#### <「import kitchen. microwave ;」のイメージ >
「API：料理道具」「メモリ：キッチン」「ソースコード：材料」

キッチンで材料を加工中、電子レンジが必要になったので、料理道具から取り出し、キッチンに置くことで使える状態にした。

## 〇ArrayList
- ArrayListは要素数を自由に変更できる配列のようなもの
- 「List < 型 > 変数名 = new ArrayList < 型 > () ;」で生成
- java.utilパッケージで管理されているAPIのため、「java.util.ArrayList」&「java.util.List」をインポートする必要有
- 参照型の要素しか扱えないため、プリミティブ型(真偽値.mdで確認)のデータを扱いたい場合、対応するラッパークラスを型として指定しなければならない

  ex.)[ 対応するクラス：基本型 ] = Integer：int, Boolean：boolean, Character：char etc.
  
[![Image from Gyazo](https://i.gyazo.com/e86771c5196232dcec3e786923b9fa65.png)](https://gyazo.com/e86771c5196232dcec3e786923b9fa65)
  
