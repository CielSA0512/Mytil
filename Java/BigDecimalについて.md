## 〇BigDecmalとは
- doubleやfloatデータ型では誤差が生じる計算の場合に、意図しない結果を得てしまうことがあるため、「銀行丸め」などの勘定系の正確な値計算をしたいときに用いるAPI。
- BigDecimalは通常の数の計算とは異なり、divideやaddのような特殊なメソッドを用いる。「/」や「+」は使えない。

#### <double型の計算>
[![Image from Gyazo](https://i.gyazo.com/371dd2c86c62a7bc30947e71cb672517.png)](https://gyazo.com/371dd2c86c62a7bc30947e71cb672517)

#### <BigDecimal型の計算>
[![Image from Gyazo](https://i.gyazo.com/6d9c4a334ce9782e91b80e22eae5fd5a.png)](https://gyazo.com/6d9c4a334ce9782e91b80e22eae5fd5a)

#### ※銀行丸め
第N桁で丸める場合、以下のようなもの
- 第N桁で丸める場合第N桁が偶数なら5以下は切り捨て。それ以外は切り上げ。
- 第N桁が奇数なら5未満は切り捨て。それ以外は切り上げ。



    
