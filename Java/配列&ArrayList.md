## 〇配列
- 配列は変数のセットのようなもの
- 「データ型 [] 変数名={配列}」で定義される

  ※[]の間にスペースは入れないこと
  
  [![Image from Gyazo](https://i.gyazo.com/5222427759c33390fd0a7686c20ab3d3.png)](https://gyazo.com/5222427759c33390fd0a7686c20ab3d3)

  ※varを使った型推論は配列の宣言時に代入する値が確定しているときは使えない
[![Image from Gyazo](https://i.gyazo.com/6cc3071a9e363bd01466e1377c6ba0e5.png)](https://gyazo.com/6cc3071a9e363bd01466e1377c6ba0e5)

#### <多次元配列>
[![Image from Gyazo](https://i.gyazo.com/017be2de216b59b82a1a580fef43601a.png)](https://gyazo.com/017be2de216b59b82a1a580fef43601a)

[![Image from Gyazo](https://i.gyazo.com/3dbf34118d53437a3b1dd44fded33c9b.png)](https://gyazo.com/3dbf34118d53437a3b1dd44fded33c9b)
[![Image from Gyazo](https://i.gyazo.com/453d824c845372b8ef3c2ef527487e4a.png)](https://gyazo.com/453d824c845372b8ef3c2ef527487e4a)

#### <コマンドライン引数>
[![Image from Gyazo](https://i.gyazo.com/61aeed9526e6990745338cd4bbbd5386.png)](https://gyazo.com/61aeed9526e6990745338cd4bbbd5386)

※先に任意のファイルをコンパイルしておくこと

### 使い方(今回は「Java.practice」直下に「Array.java」を作成)
[![Image from Gyazo](https://i.gyazo.com/4b63c8cbf9b2710d0bfc41fb1679c8ad.png)](https://gyazo.com/4b63c8cbf9b2710d0bfc41fb1679c8ad)

※配列の各要素は、配列名[インデックス番号]とすることで取得できる

### 要素の上書き
- 配列の特定の要素に値を代入することで、要素を上書きすることができる

  ※配列に存在しない要素に値を代入することはできない

  [![Image from Gyazo](https://i.gyazo.com/551842b8de649dff7b6a40e16b4011b8.png)](https://gyazo.com/551842b8de649dff7b6a40e16b4011b8)

### 配列の繰り返し
- for文を用いると定義した配列の要素をすべて出力できる

#### <要素数を数字で表した場合(i<3)>

 [![Image from Gyazo](https://i.gyazo.com/f81efd8b4dd305f71f82ccc2396dcdca.png)](https://gyazo.com/f81efd8b4dd305f71f82ccc2396dcdca)

#### <「要素数をlengthで表した場合(i< names.length)>

 [![Image from Gyazo](https://i.gyazo.com/6b45bfe8f0eec8c5900d5666297479e4.png)](https://gyazo.com/6b45bfe8f0eec8c5900d5666297479e4)

  ※lengthは要素の数を数える機能のことで、「配列.length」で表される

### for文の小ネタ
#### <普通のfor文>

[![Image from Gyazo](https://i.gyazo.com/2315afd34e7d732aa117635ffc775e53.png)](https://gyazo.com/2315afd34e7d732aa117635ffc775e53)

#### <拡張for文>

[![Image from Gyazo](https://i.gyazo.com/d759a67377f8efe8a46b16f03c19b53f.png)](https://gyazo.com/d759a67377f8efe8a46b16f03c19b53f)

- 拡張for文は「for(データ型　変数名：　配列){}」で表現
- 画像のように普通のfor文から拡張for文への書き換えることで、変数に配列の要素自体が代入されるため、シンプルに書ける。

## 〇ArrayList
- ArrayListは要素数を自由に変更できる配列のようなもの
- 「List < 型 > 変数名 = new ArrayList < 型 > () ;」で生成
- java.utilパッケージで管理されているAPIのため、「java.util.ArrayList」&「java.util.List」をインポートする必要有
- 参照型の要素しか扱えないため、プリミティブ型(真偽値.mdで確認)のデータを扱いたい場合、対応するラッパークラスを＜型＞内に指定しなければならない
[![Image from Gyazo](https://i.gyazo.com/661f016b1226c89becc2e5e0af82a984.png)](https://gyazo.com/661f016b1226c89becc2e5e0af82a984)

  ex.)[ 対応するクラス：基本型 ] = Integer：int, Boolean：boolean, Character：char etc.
  
[![Image from Gyazo](https://i.gyazo.com/e86771c5196232dcec3e786923b9fa65.png)](https://gyazo.com/e86771c5196232dcec3e786923b9fa65)

### 使い方「WorkSpace > Sample1_15_1~4.java」
#### < add >

[![Image from Gyazo](https://i.gyazo.com/c8104c14e21d8100dec1a23e7d921566.png)](https://gyazo.com/c8104c14e21d8100dec1a23e7d921566)

#### < remove >

[![Image from Gyazo](https://i.gyazo.com/2cc78620da9bfd8fa3ba634884e6a9bc.png)](https://gyazo.com/2cc78620da9bfd8fa3ba634884e6a9bc)

[![Image from Gyazo](https://i.gyazo.com/08de04c7d57a5d396b9025a413e080e3.png)](https://gyazo.com/08de04c7d57a5d396b9025a413e080e3)

※要素1が削除されたら、それ以降の要素は前に詰める。

#### < size() >

[![Image from Gyazo](https://i.gyazo.com/efaa1b2420c566783c00997d528036c5.png)](https://gyazo.com/efaa1b2420c566783c00997d528036c5)

※「numberList.size()」は「.length」的な使い方
