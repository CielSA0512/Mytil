# Javaとは
- オブジェクト指向プログラミング言語のひとつ
- 大規模システム、Webアプリケーション、スマートフォンアプリなどで使用されている。
- Javaの実行環境は、実行時にすべてのクラスファイルを一度に読み込むのではなく、必要に応じてクラスファイルをロードする
- JVM[^1]を活用することで、プラットフォーム[^2]に依存せず、JVM上でJavaを動かせる

[JVMとは](https://www.sejuku.net/blog/19871)

> JVMがあればJavaプログラムを解釈し、対象のOSで実行可能な形式のコードに変換して動かせる
[![Image from Gyazo](https://i.gyazo.com/4a4d15522d5c5249b9bcede9672a406f.png)](https://gyazo.com/4a4d15522d5c5249b9bcede9672a406f)

[Java JDKをUbuntuにインストールする方法](https://qiita.com/studio_meowtoon/items/4d11e94a2389758759cd)

# Javaを実行する手順
①Javaソースコードファイル「ファイル名.java」を作成し、プログラムを記述する

②ターミナルで「javac ファイル名.java」を実行し、コンパイルする

③②を実行すると「.class」のバイトコードファイルができるので、これをターミナルで実行

[![Image from Gyazo](https://i.gyazo.com/b3eeb69b1296bda3d6db551d76a41d52.png)](https://gyazo.com/b3eeb69b1296bda3d6db551d76a41d52)

※実行方法は「java ファイル名(.classは省く)」

※①でプログラムを書き換えたら、②、③の手順で実行すること！

# 〇用語解説
### コンパイル
- コンパイラ[^3]がプログラミング言語で書かれたソースコードを解析し、機械語やバイナリコード[^4]などのオブジェクトコード[^5]に変換する**作業**のこと
- ターミナル上では「javac ファイル名.java」でコンパイルを実行
  [![Image from Gyazo](https://i.gyazo.com/e1ef123764bee7e7aab4f78361d9f1e0.png)](https://gyazo.com/e1ef123764bee7e7aab4f78361d9f1e0)

### ソースコードファイル
人間が理解できる文字列で記述されたファイルのこと

[^1]:JVM(Java Virtual Machine)の略で、Javaプログラムを動かすために必要なソフトウェア。
[^2]:Windows, macOS, Linuxなどを指す 
[^3]:コンピュータの自動プログラミングに使うプログラムの一種
[^4]:0,1で構成された文字列
[^5]:コンピュータが直接実行できる機械語に変換したプログラムコード
