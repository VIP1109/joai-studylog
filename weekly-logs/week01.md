# Week 01 — Python基礎

## やったこと
- Atcoder 212~216のA問題（5問分解いた）

## 詰まったこと・解決方法
- a,b = map(int,input().split())のようにやるとatcoderの入力を取ることができる
- stringを合成の方法がわからなかった -> f"{string} なんか" で合わせる。f"{string : .2f}"とかで小数点第2位までみたいにできる

## 気づき・学び
- 型の名前はいらない
- split()という関数は()の中身で分ける
- a**b = a^b
- a%b = a mod b
- a/b -> float
- a//b -> int
- 配列[a:b]と書くことでidxがa以上b未満のところを抜き出す
- 配列[-1]で末尾を参照
- 配列.append(x)でxを末尾に追加
- 配列.extend(a)で配列aを末尾に追加
- dictはc++でのmap
- dictでの要素の取得はget()でとれる。get(代表,値がない場合)のようにすることでerrorを防げる
- dict.keys()はdictの中に含まれているkey
- dict.value()はdictの中に含まれている要素
- dict.items()はdictの中に含まれている{key,要素}
- 配列のidxと値を同時に取得->enumerate()
- enumerate(配列,start = a)でidx=aから始める
- 2つの配列を合成->zip()
- if() : このよう : が後ろにいる({}の代わり)(()はなくてもいい)
- else if は elif
- for 値 in range(a) 0からa-1まで
- for 値 in range(a,b) aからb-1まで
- for 値 in range(a,b,c) aからb-1までc刻みで
- while 条件式 : で書く
- def 関数名(引数) : で関数定義(それ以外はc++と同じ)
- lambda 代表値 : 代表値に関する処理でラムダ式
- map(関数,関数の引数となる配列)を取ることで楽に書くことができる
- filter(関数,関数の引数となる配列)を取ることで条件を満たさないやつを自動的に消す
- reduce(関数,関数の引数となる配列)で再帰的に前の処理結果を用いることで楽に書くことができる
- exit(0)を最後に書いたほうがCE出ずに済む
### ABCを解いてての気づき
- string -> str
- !ok -> not ok
- a && b -> a and b
- a || b -> a or b
- 空の配列 -> 配列 = []
- pair,tuple -> (要素1,要素2,要素3,...)
- 配列のソート -> 配列.sort()
- 配列の逆順 -> 配列.reverse()
- 浮動小数点誤差に注意する
- 縦に入力する場合は[配列の型 ex) str = '']*要素数

## Python独自の省略方法
### 配列[代表値 forループ]の書き方
result = []<br>
for i in range(1,11):<br>
&emsp;result.append(i**2)<br>
result = [x^2 for x in range(1,11)]

## 来週やること


## 参考リンク
- [Python入門 AtCoder Programming Guide for beginners (APG4bPython)] https://atcoder.jp/contests/APG4bPython/tasks/APG4bPython_f
- [Pythonの標準入力input()の個人的まとめ] https://qiita.com/naoya_ok/items/f33a6ab2ff77154a7121
- [Pythonの関数型プログラミング: map, filter, reduce, lambdaの効果的な使用法] https://qiita.com/Tadataka_Takahashi/items/c5ba5739e7c6e97e8725
