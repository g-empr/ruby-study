# Ruby基礎
[公式サイト](https://www.ruby-lang.org/ja/)やrbenvで実行環境を導入する。
## オブジェクトの表示
```Ruby
print("Hello World!.")
```
`"Hello World!.\n"`の部分が文字列オブジェクト。  
## メソッドの表示
```Ruby
print("Hello World!.")
```
`print`の部分をメソッドと呼び、`()`内部を引数と呼ぶ。
## \
文字列オブジェクト内で改行したいとき、`\n`を用いる。
```Ruby
print("Hello \nWorld!.")
```
`\`にはその他にも演算子に使われる記号などを文字列として出力したい場合に、対象となる記号の前に記述して使うことがある。(エスケープ文字)
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