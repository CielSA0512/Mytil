# VSCODEでJAVAを始める方法

## 〇環境構築
### ① JDKをインストールするために、以下のURLにアクセスする。

https://www.oracle.com/java/technologies/downloads/#jdk22-windows

※Windowsであれば「x64 Installer」を選択してインストーラをダウンロードする。

※ダウンロードファイルに下記の内容が表示されればオッケー！（verは人により異なる）
[![Image from Gyazo](https://i.gyazo.com/c9a0ee700168e117cbf60ed0c4a426ad.png)](https://gyazo.com/c9a0ee700168e117cbf60ed0c4a426ad)

### ② ダウンロード完了後、インストーラーの指示に従って進めていく。

※この際、「JDKインストール確認方法」を参考に、JDKのverを確認しておく。
[![Image from Gyazo](https://i.gyazo.com/dfac9ca71c40d022a6d412a5e1120372.png)](https://gyazo.com/dfac9ca71c40d022a6d412a5e1120372)
上記画像の場合は、「jdk-22.0.1」

※インストーラーの指示に従っていく過程で、保存先を指定できるので、デスクトップに「jdk-22.0.1」とフォルダーを作成してそこに保存するようにしておく。

### ③「jdk-22.0.1」を「windows10(C:) → Program Files → Java」内に移動させる。
[![Image from Gyazo](https://i.gyazo.com/890ac1c4c604fc16c16b7a94a4b65fdc.png)](https://gyazo.com/890ac1c4c604fc16c16b7a94a4b65fdc)

### ④「javaの実行環境の作成方法」を参考に、PATHを通す作業を行う。

### ⑤「vscodeでjavaを始める方法」を参考に、拡張機能の導入と「settings.json」に下記の内容を追記
  [![Image from Gyazo](https://i.gyazo.com/e9d209309d44a625056487a90ba1fbd6.png)](https://gyazo.com/e9d209309d44a625056487a90ba1fbd6)

### ⑥ vscodeを再起動

## 〇参考資料
「vscodeでjavaを始める方法」：https://teramaguro.hatenablog.com/entry/2021/12/28/042743

「JDKインストール確認方法」：https://youtu.be/LS0o7mKg_Qg?si=mV4Svb0upd0AW-6x　
（8:08~）

「javaの実行環境の作成方法」：

https://www.fit.ac.jp/~m-ishihara/Lectures/JavaProgramming1/howToSetupOnWin10new/howToSetup.html

の「2. JDKのbinフォルダにPATHを通す」まで
