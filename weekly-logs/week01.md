# Week 01 — Python基礎/NumPy基礎

## やったこと
- Atcoder 212~216のA,B問題（10問分解いた）

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
- exit(0)を最後に書いたほうがCE出ずに済む<br><br>
- np.array()の中身は[]で必ず挟む -> 2次元とかを表す場合は[[1,2],[2,3]]みたいな感じ
- np.zeros(行列の大きさ,型) -> (3,4)の場合3*4型行列ができる。型ははdtype=dp.int32みたいに指定
- np.ones(行列の大きさ,型) -> zeros()の初期値が1の場合
- np.arange(初項,末項,公差,型) -> 等差数列を作る
- np.linpace(初項,末項,項数,末項を配列に含めるか,公差を表示するか,軸)　-> 公差を自動で計算してくれるがいいとこ
- a[from:to,from:to...] -> 配列のtoからfrom未満を抜き出す。列ベクトル,行ベクトル...と続いていく（スライス）
- a.shape -> 行列の大きさを返す
- a.reshape(大きさ) -> 大きさ型行列にする
- a.dot(行列1,行列2...) -> 行列同士をかける
- a.dtype -> 行列の型を返す
- a.astype() -> 行列の型を変更
- np.average(行列,軸,重り,返り値,縮小するかどうか) -> 重りは平均への影響のしやすさ。返り値=Trueだと(平均,おもみの合計)を返す。keepdimsは次元を残したまま。
- np.mean(行列,軸,型,返り値用の配列,縮小するかどうか,平均値に含める要素かを表した行列) -> 返り値用の配列はメモリー省略したいとき。行列[条件]と書くことで使う要素を指定することができる
- np.std(行列,軸,型,返り値用の配列,ddof,縮小するかどうか,標準偏差の計算に含める要素かを表した行列) -> ddof=0なら母標準偏差, ddof=1なら標本標準偏差
- np.(a)min(行列,軸,返り値用の配列,縮小するかどうか,初期の最小値,最小値に含めるかを表した配列)
- np.(a)max(行列,軸,返り値用の配列,縮小するかどうか,初期の最大値,最小値に含めるかを表した配列)
- np.sum(行列,軸,型,返り値用の配列,縮小するかどうか,合計の初期値,合計に含めるかを表した配列)
- np.argmax(行列,軸,返り値用の配列,縮小するかどうか) -> 多次元配列の中の最大値の要素を持つインデックスを返す
- np.sort(行列,軸,ソートの種類,ソートする領域) -> ‘quicksort’‘mergesort’‘heapsort’の3つから選ぶ。ソート結果を返す
- np.argsort(行列,軸,ソートの種類,ソートする領域) -> ‘quicksort’‘mergesort’‘heapsort’の3つから選ぶ。ソート結果の配列のidxを返す
- np.where(条件,[x,y]) -> np.where(配列が満たす条件)で条件を満たすidx。配列[np.where(配列が満たす条件)で条件を満たす要素が返される。np.where(条件,[x,y])で[x,y]で構成された新たな配列を作る。
- np.meshgrid(1次元配列,初期値,sparce,copy) -> 1次元配列から2次元のグリッドを製作する。sparceは特定の方向しか持たない行列を返すか、すべて埋まっている密な行列を返すかの違い。copyはメモリのコピーを作るかどうか。

- csvファイルを読むときはpandasのread_csv(ディレクトリ)(r'C:\PythonAI\dataset\...)とかく
- df.head() -> データの先頭を表示する
- df.shape -> データの大きさ
- df.dtypes -> 各データの種類
- df.describe -> データの最初と最後を表示する
- df.isnull().sum() -> 各データの種類の欠損値(値無し)を計算する
- df["Age"].mean()/df.groupby("Survived")["Age"]mean() -> dfの["データ名"].何とかでそのデータの種類に対して処理をすることができる。df.groupby("データ名")["データ名"] -> 最初のgroupby()でこれをもとに[""]これを分けるという意味。分母で今回は2つに分かれるが、リストとして管理をしてあげて勝手に配列として計算してくれる。mean()は平均値
- df[df["Sex"]=="female"] -> df[条件]で条件を満たすデータのみを抽出できる。df["データ名"]でデータ列に対して処理をすることができる。=="文字列"でそれがdf["データ名"]の中の"文字列"となっているところだけを抽出する。
- df["Age"].fillna(df["Age"].median()) -> .fillna(欠損値に対しての処理)。df["データ名"].meadian()はあるデータ列の中央値
- df["新しい配列"]=今の配列を用いた処理 -> 新しい配列を自動的に追加することができる
- df.drop(columns=["Cabin", "Ticket"]) -> df.drop(データ名)で消すデータ列を指定できる。columns=[データ名,データ名...]みたいにすることで複数の配列をまとめて保存することができる
- データの処理をした後保存するためにdf=をすることを忘れない
- matplotlib.pyplot as plt -> グラフの描写をすることができる
- plt.xlable("名前"),plt.ylable("名前") -> グラフのx,y軸の名前を追加することがきる
- plt.title("名前") -> グラフの名前を決めることができる
- plt.plot(データ,データ) -> 折れ線グラフ
- plt.scatter(データ,データ) -> 散布図
- plt.bar(カテゴリー,データ) -> 棒グラフ
- plt.hist(データ,区切り数) -> ヒストグラム
- plt.boxplot(データ) -> 箱ひげ図
- plt.pie(データ数,カテゴリー,%表示) -> 円グラフ
- plt.contour(x座標用のデータ,y座標用のデータ,各座標の高さ) -> 等高線図
- plt.imshow(データ,cmap,etc) -> ヒートマップ。カラーマップは以下のURL参照
- plt.colorbar() -> ヒートマップで使った色を表示する
- plt.show() -> グラフの表示
titanicのデータ表示
- df.dropna(subset["データ名"]) -> 欠損値を排除する
- df["データ名"][条件] -> データの中の条件を満たすやつのみを自動的に抜き取る
- plt.hist([データ1,データ2,...],bins,color=[データ1,データ2,...],label=[]) -> みたいに複数のデータは[]でくくることで一気にまとめて表示することができる
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
- 縦に入力する場合は[配列の型 ex) str = '']*要素数で初期化

## Python独自の省略方法
### 配列[代表値 forループ]の書き方
result = []<br>
for i in range(1,11):<br>
&emsp;result.append(i**2)<br>
result = [x^2 for x in range(1,11)]

## 来週やること
- 2週目の内容を始める

## 参考リンク
- [Python入門 AtCoder Programming Guide for beginners (APG4bPython)] https://atcoder.jp/contests/APG4bPython/tasks/APG4bPython_f
- [Pythonの標準入力input()の個人的まとめ] https://qiita.com/naoya_ok/items/f33a6ab2ff77154a7121
- [Pythonの関数型プログラミング: map, filter, reduce, lambdaの効果的な使用法] https://qiita.com/Tadataka_Takahashi/items/c5ba5739e7c6e97e8725
- [第14回「Matplotlibの使い方」] https://www.pythonic-exam.com/archives/8956
- [Matplotlibで画像を表示するimshowの初歩] https://qiita.com/hirowatari-s/items/e51cf26d093fbefa5598
- [Choosing Colormaps in Matplotlib] https://matplotlib.org/3.1.0/tutorials/colors/colormaps.html
