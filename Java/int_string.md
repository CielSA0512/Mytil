# 〇変数について
## 変数の定義方法
・変数を扱う際に「データ型 変数名」で定義する必要がある。
[![Image from Gyazo](https://i.gyazo.com/b5bc8c1043cc9d0a484c0afd6dd4d7a2.png)](https://gyazo.com/b5bc8c1043cc9d0a484c0afd6dd4d7a2)

## データ型の種類
- int型・・・数値
- String型・・・文字列 　※StringのSは大文字にすること！
- double型・・・小数点

## 変数名の注意点
#### 良い例
- date・・・〇英単語を用いる
- userName・・・〇2語以上の場合は大文字で区切る（キャメルケース）

#### 悪い例
- 1name・・・×数字開始
- first_name・・・アンダーバー（スネークケース）
- namae・・・△ローマ字
- 名前・・・△日本語

## 使い方 (※今回は、「Java/int_string」直下に「int_string.java」を作成)
[![Image from Gyazo](https://i.gyazo.com/bb1f65e317e9438a8dd5bed774c453f6.png)](https://gyazo.com/bb1f65e317e9438a8dd5bed774c453f6)

#### ①「データ型　変数名;」で定義する（順番は必ず順守）ex.)数値型：「int number」 文字列型：「String text」

#### ②定義後、変数に値を入れる"代入"を行う。「変数名 = 値;」

#### ③出力する（どの工程の最後にも必ず「;」をいれること！） 

# 〇変数の初期化
・「データ型　変数名　＝　値」とすることで、一行にまとめることができるようになる。
[![Image from Gyazo](https://i.gyazo.com/3ac8c783f7b59c4c3e2467efca7fdca3.png)](https://gyazo.com/3ac8c783f7b59c4c3e2467efca7fdca3)

# 〇変数の更新
・「変数名　＝　値」とすることで、「データ型　変数名　＝　値」で決めた値を更新することができる。

※値を更新するときは、「データ型」を定義する必要はなし

[![Image from Gyazo](https://i.gyazo.com/aec96d4729a7b6ced4e9e22fe5b62ef0.png)](https://gyazo.com/aec96d4729a7b6ced4e9e22fe5b62ef0)

# 〇変数の自己代入
・「値　＝　値　＋　任意の値」で値を更新することができる

[![Image from Gyazo](https://i.gyazo.com/79a1ab29570f339748a4efab1319af62.png)](https://gyazo.com/79a1ab29570f339748a4efab1319af62)

※自己代入の省略の仕方

- x = x + 10; → x += 10;

- x = x - 10; → x -= 10;
  
※値が1の時だけさらに省略して書ける！
- x = x + 1; → x += 1; → x ++;

- x = x - 1; → x -= 1; → x --;
