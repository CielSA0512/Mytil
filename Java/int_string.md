# 〇変数について
## 変数の定義方法
・変数を扱う際に「データ型 変数名」で定義する必要がある。
[![Image from Gyazo](https://i.gyazo.com/b5bc8c1043cc9d0a484c0afd6dd4d7a2.png)](https://gyazo.com/b5bc8c1043cc9d0a484c0afd6dd4d7a2)

## データ型の種類
[![Image from Gyazo](https://i.gyazo.com/3b186bc0c6eecdebaf376e823efd1847.png)](https://gyazo.com/3b186bc0c6eecdebaf376e823efd1847)

- var型・・・型推論　※どんな型を推論したかは「System.out.println(((Object)変数名).getClass().getSimpleName());」で調べられる

  ※扱うデータの大きさに関わらず整数はint、小数点数はdouble型が一般的
  
  ※Stringは0文字以上の文字列

## リテラル
[![Image from Gyazo](https://i.gyazo.com/610eaa1f52ef21da5bdefb1e2bde1f1b.png)](https://gyazo.com/610eaa1f52ef21da5bdefb1e2bde1f1b)

　※long型はint型で扱える数値の範囲を超え、long型でしか扱えない数値を変数に入れる場合は末尾に「L」や「l」(どちらでも可)を必ずつける

## エスケープ文字
[![Image from Gyazo](https://i.gyazo.com/04a357899d6fd28d1f6963c4f79cb361.png)](https://gyazo.com/04a357899d6fd28d1f6963c4f79cb361)

[![Image from Gyazo](https://i.gyazo.com/28fc14aed23cef2c70e28b03cebd3796.png)](https://gyazo.com/28fc14aed23cef2c70e28b03cebd3796)

## 変数名の注意点
#### 良い例
- date・・・〇英単語を用いて、1文字目は必ず小文字
- userName・・・〇2語以上の場合は大文字で区切る（キャメルケース）
- first_name・・・アンダーバー（スネークケース） 

　※スネークケースは場合によりけり

#### 悪い例
- 1name・・・×数字開始
- namae・・・△ローマ字
- 名前・・・△日本語
- 予約語・・・×abstract,boolean etc.

## 使い方 (※今回は「Java/int_string」直下に「int_string.java」を作成)
[![Image from Gyazo](https://i.gyazo.com/bb1f65e317e9438a8dd5bed774c453f6.png)](https://gyazo.com/bb1f65e317e9438a8dd5bed774c453f6)

#### ①「データ型　変数名;」で定義する（順番は必ず順守）ex.)数値型：「int number」 文字列型：「String text」

#### ②定義後、変数に値を入れる"代入"を行う。「変数名 = 値;」

#### ③出力する（どの工程の最後にも必ず「;」をいれること！） 

# 〇変数の初期化
・「データ型　変数名　＝　値」とすることで、一行にまとめられる。
[![Image from Gyazo](https://i.gyazo.com/3ac8c783f7b59c4c3e2467efca7fdca3.png)](https://gyazo.com/3ac8c783f7b59c4c3e2467efca7fdca3)

※イメージ図

[![Image from Gyazo](https://i.gyazo.com/c70194e1cf8e8d67602be74a992e8b38.png)](https://gyazo.com/c70194e1cf8e8d67602be74a992e8b38)

# 〇変数の更新
・「変数名　＝　値」とすることで、「データ型　変数名　＝　値」で決めた値を更新することができる。

　※値を更新するときは、「データ型」を定義する必要はなし

[![Image from Gyazo](https://i.gyazo.com/aec96d4729a7b6ced4e9e22fe5b62ef0.png)](https://gyazo.com/aec96d4729a7b6ced4e9e22fe5b62ef0)

# 〇変数の定数化(final)
・「final データ型　定数名＝初期値（固定値）」とすることで、定数として扱える。

　※定数名は必ず半角英数の大文字で記述＆大文字区切り（キャメルケース）を使用。
 　　
    ex.)LIST_PRICE

[![Image from Gyazo](https://i.gyazo.com/40255ff1f487b88935772d36e3364669.png)](https://gyazo.com/40255ff1f487b88935772d36e3364669)

# 〇変数の自己代入
・「値　＝　値　＋　任意の値」で値を更新することができる

[![Image from Gyazo](https://i.gyazo.com/79a1ab29570f339748a4efab1319af62.png)](https://gyazo.com/79a1ab29570f339748a4efab1319af62)

算術演算子一覧
[![Image from Gyazo](https://i.gyazo.com/49ff8a2bce1742b401c50e8514ad7a7d.png)](https://gyazo.com/49ff8a2bce1742b401c50e8514ad7a7d)

※自己代入の省略の仕方

- x = x + 10; → x += 10;

- x = x - 10; → x -= 10;
  
※値が1の時だけさらに省略して書ける！
- x = x + 1; → x += 1; → x ++;
- x = x - 1; → x -= 1; → x --;

※「X++」は式を実行した後に「＋１」を行う（「X--」も同様）
[![Image from Gyazo](https://i.gyazo.com/af40696247d39c7ccbb9b252aa8c3eb7.png)](https://gyazo.com/af40696247d39c7ccbb9b252aa8c3eb7)　[![Image from Gyazo](https://i.gyazo.com/eb92e3a6ce49eda5e501ab677e81126d.png)](https://gyazo.com/eb92e3a6ce49eda5e501ab677e81126d)
