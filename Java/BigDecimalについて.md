## 〇BigDecmalとは
- 誤差が生じないように正確に計算するためのAPI。インポート文は以下
     #### 「 import java.math.BigDecimal ; 」
- 四捨五入などの丸め処理の方法や桁数を指定するためにも使う。
- BigDecimalは通常の数の計算とは異なり、divideやaddのような特殊なメソッドを用いる。「/」や「+」は使えない。

    詳しくは、[Oracle社　JavaSE21 & JDK21 API仕様](https://docs.oracle.com/javase/jp/21/docs/api/) 　をチェック

#### <double型の計算>
[![Image from Gyazo](https://i.gyazo.com/371dd2c86c62a7bc30947e71cb672517.png)](https://gyazo.com/371dd2c86c62a7bc30947e71cb672517)
[![Image from Gyazo](https://i.gyazo.com/7c2bab20a1c25752f34dca8dd7b81095.png)](https://gyazo.com/7c2bab20a1c25752f34dca8dd7b81095)

#### <BigDecimal型の計算>
[![Image from Gyazo](https://i.gyazo.com/6d9c4a334ce9782e91b80e22eae5fd5a.png)](https://gyazo.com/6d9c4a334ce9782e91b80e22eae5fd5a)
[![Image from Gyazo](https://i.gyazo.com/b82c545ba3d833400057f2b7eea103e0.png)](https://gyazo.com/b82c545ba3d833400057f2b7eea103e0)

#### ※丸め計算（ex.銀行丸め）
第N桁で丸める場合、以下のようなもの
- 第N桁で丸める場合第N桁が偶数なら5以下は切り捨て。それ以外は切り上げ。
- 第N桁が奇数なら5未満は切り捨て。それ以外は切り上げ。

## 〇BigDecimalの計算方法

#### <足し算「add」・引き算「subtract」・掛け算「multiply」>
[![Image from Gyazo](https://i.gyazo.com/508f25b99e1b9f358a47f8461cba0aa2.png)](https://gyazo.com/508f25b99e1b9f358a47f8461cba0aa2)

#### <割り算「divide」（小数点以下の計算も含めて）>
[![Image from Gyazo](https://i.gyazo.com/9b5a660dfd8f60b9aae879ab6f0c3165.png)](https://gyazo.com/9b5a660dfd8f60b9aae879ab6f0c3165)

## 〇BigDecimalの値の比較方法「compareToメソッド」
#### <compareToメソッドの仕様>
[![Image from Gyazo](https://i.gyazo.com/80c7864a74862459907c79321ecf4822.png)](https://gyazo.com/80c7864a74862459907c79321ecf4822)

#### <compareToメソッドの使い方>
[![Image from Gyazo](https://i.gyazo.com/a3a730c4f04df0d11a836e6ef8f8c0f2.png)](https://gyazo.com/a3a730c4f04df0d11a836e6ef8f8c0f2)

## 〇参考文献
[Java入門」BigDecimalの大小をcompareToで比較する方法](https://www.sejuku.net/blog/21589?utm_source=blog&utm_medium=blog&utm_campaign=blog__25564)
