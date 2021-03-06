# オブジェクト・変数・定数
## オブジェクト
**オブジェクト** とはデータまたはデータのまとまりを指す言葉である。  
オブジェクトの種類には以下のようなものがある。
- 文字列オブジェクト
- 数値オブジェクト
- 配列オブジェクト・ハッシュオブジェクト
- 正規表現オブジェクト
- 時刻オブジェクト
- ファイルオブジェクト
- シンボルオブジェクト
- 範囲オブジェクト
- 例外オブジェクト
## クラス
クラスとはオブジェクトのタイプを表すもののことである。  
オブジェクトが持つ性質は所属するクラスによって決まる。  
  
| オブジェクト | クラス |
----|----
| 数値 | Numeric |
| 文字列 | String |
| 配列 | Array |
| ハッシュ | Hash |
| 正規表現 | Regexp |
| ファイル | File |
| シンボル | Symbol |

## 変数
Rubyには変数の種類がいくつかある。
### ローカル変数
先頭がアルファベットの小文字か`_`で始まる変数。  
変数としてのスコープが狭い。
```Ruby
x = 0
```
### グローバル変数
先頭が`$`で始まる変数。  
変数としてのスコープが広い。
```Ruby
$x = 0
```
### インスタンス変数
先頭が`@`で始まる変数。
```Ruby
@test = 0
```
### クラス変数
先頭が`@@`で始まる変数。
```Ruby
@@test = 0
```
## 定数
変数とは違い、最初の代入以降の代入では警告が表示される。  
先頭がアルファベットの大文字から始まる。
```Ruby
TEST = 0
```
## 予約語
プログラム上では予め意味を持った語句が存在する。  
例えば`do`や`if`など、これらは変数として使用するとエラーとなってしまう。  
これらの特殊なキーワードを **予約語** と呼ぶ。  
- [字句構造 - Ruby 2.5.0 リファレンスマニュアル](https://docs.ruby-lang.org/ja/latest/doc/spec=2flexical.html)
## 多重代入
値の代入は通常ひとつずつ行うが、まとめて代入する方法もある。
```Ruby
a = 1
b = 2
c = 3
```
は
```Ruby
a, b, c = 1, 2, 3
```
と書き換えられる。  
また、受け入れ先の変数の頭に`*`を記述することで、代入しきれなかったオブジェクトがまとめて配列として代入される。
```Ruby
a, b, *c = 1, 2, 3, 4, 5
p [a, b, c] # => [1, 2, [3, 4, 5]]
a, *b, c = 1, 2, 3, 4, 5
p [a, b, c] # => [1, [2, 3, 4], 5]
```
あるふたつの変数の値を入れ換えたいとき、一時変数を用いて入れ換えたりする。
```Ruby
a, b = 0, 1
tmp = a # => aを退避させる
a = b
b = tmp
p [a, b] # => [1, 0]
```
多重代入ではこれを簡単に記述できる。
```Ruby
a, b = 0, 1
a, b = b, a
p [a, b] # => [1, 0]
```
配列の要素を変数に代入するとき、以下のように書く。
```Ruby
array = [1, 2]
a, b = array # 配列の中身がそれぞれ左辺に代入される
p a # => 1
p b # => 2
```
配列の先頭のみ抜き出したい場合は以下のように書く。
```Ruby
array = [1, 2]
a, = array
p a # => 1
```