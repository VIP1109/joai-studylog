# Week 01 — Python基礎

## やったこと
- Atcoder 212~216のA問題（5問分解いた）

## 詰まったこと・解決方法
- a,b = map(int,input().split())のようにやるとatcoderの入力を取ることができる
- stringを合成の方法がわからなかった -> f"{string} なんか" で合わせる。f"{string : .2f}"とかで小数点第2位までみたいにできる

## 気づき・学び
- 型の名前はいらない
- a**b = a^b
- a%b = a mod b
- a/b -> float
- a//b -> int
- 配列[a:b]と書くことでidxがa以上b未満のところを抜き出す
- 配列[-1]で末尾を参照
- 配列.append(x)でxを末尾に追加
- 配列.extend(a)で配列aを末尾に追加
- dictはc++でのmap
- dictでの要素の取得はget()でとれる。get(代表, 値がない場合)のようにすることでerrorを防げる
- dict.keys()はdictの中に含まれているkey
- dict.value()はdictの中に含まれている要素
- dict.items()はdictの中に含まれている{key,要素}
- 配列のidxと値を同時に取得->enumerate()
- enumerate(配列,start = a)でidx=aから始める
- 2つの配列を合成->zip()
- split()という関数は()の中身で分ける
- else if は elifなのと if() : このよう : が後ろにいる
- exit(0)を最後に書いたほうがCE出ずに済む

## Python独自の省略方法
result = []
for i in range(1,11):
    result.append(i**2)
result = [x**2 for x in range(1,11)]
-> 配列[代表値 forループ]の書き方

## 来週やること


## 参考リンク
- [Python入門 AtCoder Programming Guide for beginners (APG4bPython)] https://atcoder.jp/contests/APG4bPython/tasks/APG4bPython_f
