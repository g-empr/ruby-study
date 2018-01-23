# 目次
1. **[Ruby基礎](#ruby基礎)**
2. **[](#)**
3. **[](#)**
4. **[](#)**
5. **[](#)**
6. **[](#)**
7. **[](#)**
8. **[](#)**
9. **[](#)**

# Ruby基礎
予め[公式サイト](https://www.ruby-lang.org/ja/)やrbenvで実行環境を導入しておく。
## オブジェクトの表示
```Ruby
print("Hello World!.")
```
`"Hello World!.\n"`の部分が **文字列オブジェクト** 。  
## メソッドの表示
```Ruby
print("Hello World!.")
```
`print`の部分を **メソッド** と呼び、`()`内部を **引数** と呼ぶ。
## \
文字列オブジェクト内で改行したいとき、`\n`を用いる。
```Ruby
print("Hello \nWorld!.")
```
`\`にはその他にも演算子に使われる記号などを文字列として出力したい場合に、対象となる記号の前に記述して使うことがある。( **エスケープ文字** )
```Ruby
print("Hello \\n!") # => Hello \n!
```
## 「""」と「''」
文字列オブジェクトとして認識させるために`""`と`''`のふたつが使用できる。  
ただし、`''`を使用すると内容に含まれる特殊文字が解釈されずにそのまま出力される。
```Ruby
print('Hello \n\n\n World!') # => Hello \n\n\n World!
```
## メソッドの呼び出し
`print`メソッドは以下のようにも書くことができる。
```Ruby
print "Hello World!"
```
複数の文字列オブジェクトを連結させる場合は以下のようにオブジェクトの区切りに`,`を書く。
```Ruby
print "Hello ", "World!" # => Hello World!
```
文字列の出力は`print`メソッド以外にも`puts`メソッドがある。  
こちらは文字列オブジェクトの末尾で必ず改行するようになる。
```Ruby
puts "Hello World!"
```
その他に`p`メソッドというものもある。  
文字列を括る`""`もまとめて出力表示するようになる。
```Ruby
p "Hello World!"
p Hello World!
```
## 変数
```Ruby
moji = "もじ"
name = 'なまえ'
number = 9999
```
変数を使えば複雑なプログラムに修正が発生しても手間を掛けずに書き換えることができる。
```Ruby
x = 10
y = 20
z = 30
a = (x*y + y*z +z*x)*2
b = x * y * z
print "表面積 = ", a, "\n"
print "体積 = ", b
```
## コメント
プログラム内でのコメントは以下のように書く。
一行コメントと複数行コメントがある。
```Ruby
# ここにコメントを書く
```
または
```Ruby
=begin
ここに
コメントを
書く
=end
```
## 制御構造
Rubyプログラムの制御構造は以下のようなものがある。
- 逐次処理：プログラムの先頭から順に処理を実行する
- 条件判断：各条件に合致する場合、それぞれの処理を実行する
- 繰り返し（ループ）：特定の条件に合致する場合、処理を繰り返す
- 例外処理：いずれかの例外が発生した場合に処理を実行する
　  
　  
  
以降は各セクションにて記述する。