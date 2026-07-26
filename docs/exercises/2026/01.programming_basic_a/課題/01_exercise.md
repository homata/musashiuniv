# 課題

----
Python基礎

## 問題文
ある箱のwidth(幅)、depth(奥行き)、height(高さ)を引数として、その箱の体積が1000以上であればTrue, 1000未満であればFalseを出力する関数を実装してください。単位は全て省略とします。

以下が想定される出力です

```python
width = 10
depth = 20
height = 35
print(homework(width, depth, height))

---------
True
```

提出するときは、以下の点に注意してください。適宜例題(次のセクションにあります)を参考にしてください。Omnicampusには例題の回答を提出する欄はありません。
>- 以下の関数`homework`の`!!WRITE ME!!`に処理を書いてください。(**「`!!WRITE ME!!`」は消して、記入してください。**)
>- 実際の提出は記述された`homework`関数全てになり、**提出はOmnicampus内の宿題の欄から今週の課題を選択後、提出内容に関数を貼り付けてから[Pythonコード提出]を押してください。**
>- 関数は1つにまとめてください。

```
# !!WRITE ME!!に処理を記入する（このセルのhomework関数のみを提出することに注意）
def homework(width, depth, height):

    !!WRITE ME!!

    return my_result
```

--------------------------
Pythonによる科学計算（NumPy）


## 問題文
整数値を値にもつNumpyの1次元配列を引数として、5の倍数かつ2で割って1余る数を要素として持つ配列を出力する関数を実装してください。

以下が想定される出力です

```python
a = np.array([1, 5, 10, 3, 4, 25, 30])
print(homework(a))
np.array([5, 25])
```

提出するときは、以下の点に注意してください。 なお、提出するのは、homework関数の定義2の内容のみになります。

1.  ライブラリのインポート
2.  「5の倍数」かつ「2で割って1余る数」を要素として持つ配列を出力するhomework関数
3.  Numpyの1次元配列の定義
4.  homework関数の出力をprintなどで確認

>- 以下の関数`homework`の`!!WRITE ME!!`に処理を書いてください。(**「`!!WRITE ME!!`」は消して、記入してください。**)
>- 実際の提出は記述された`homework`関数全てになり、**提出はOmnicampus内の宿題の欄から今週の課題を選択後、提出内容に関数を貼り付けてから[Pythonコード提出]を押してください。**
>- 返り値は数値型の配列です。
>- 関数は1つにまとめてください。

```
# 1. ライブラリのインポート
import numpy as np
```

```
# 2. homework関数の定義
# !!WRITE ME!!に処理を記入する（homework関数を提出することに注意）
def homework(a):
    !!WRITE ME!!
    return my_result
```

```
# 3. Numpyの1次元配列の定義
a = np.array([1, 5, 10, 3, 4, 25, 30])
```

```
# 4. homework関数の出力をprintなどで確認
print(homework(a))
```


----
Pythonによるデータ加工処理の基礎（Pandas）

## 問題文
下記の「#common」で始まるセルの中で指定されたリンク先にあるデータ（ワインの品質）が分析対象になります。

このデータを読み込み、カラムの`volatile acidity`について$n$等分（$n$はデータ数を越えず、分位数に同一の値が存在しない自然数。データ数が$n$で割り切れるとは限らず、この場合の処理は`Pandas.qcut`の処理に準じます。）にグループ分けします。次にそれぞれのグループのデータのうち、カラムの`quality`の値が`5`であるものについて、それらの`alcohol`の平均値を算出してください。さらに、ここで算出した各グループの`alcohol`の平均値の中で、1番小さい値を返り値とするような関数を作成してください。

提出するときは、以下の点に注意してください。  
>- 以下の関数`homework`の`!!WRITE ME!!`に処理を書いてください。(**「`!!WRITE ME!!`」は消して、記入してください。**)
>- 実際の提出は記述された`homework`関数全てになり、**提出はOmnicampus内の宿題の欄から今週の課題を選択後、提出内容に関数を貼り付けてから[Pythonコード提出]を押してください。**
>- 返り値が数値型になるようにしてください。
>- 関数は1つにまとめてください。


以下は共通の前処理になります。第4回のドライブにあるデータ（winequality-red.csv）を各自でダウンロードし、各自のMy Driveのディレクトリに格納し、データを読み込む形式にしています。

以下の説明などを参考にして各自の環境で適宜変更してください。

次のコードセルでGoogle Driveをマウントした後、ご自身の環境に合わせて、url_winequality_data = "  "を変更します。Colabの左サイドバーで見ることができます

1.   最初のセルを実行した後、Colabのファイルブラウザをたどって、対象ファイルのところで右クリック「パスをコピー」を実行
2.   次のセルのurl_winequality_data = "  " にコピーされたパスをペースト
3.   

```
from google.colab import drive
drive.mount('/content/drive')
```

```
# common
import numpy as np
import pandas as pd
from pandas import DataFrame
```

```
# googleドライブから読み込む(自分の環境に合わせて要修正)
url_winequality_data = "/content/drive/MyDrive/Colab Notebooks/winequality-red.csv"
```

```
# working place. everything
def homework(url_winequality_data, n):
    !!WRITE ME!!
    return my_result
```

**謝辞**：以下のデータセットの利用に関して  
http://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/winequality-red.csv

引用元：Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [[http://archive.ics.uci.edu/ml](http://archive.ics.uci.edu/ml)]. Irvine, CA: University of California, School of Information and Computer Science.

P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis.
Modeling wine preferences by data mining from physicochemical properties. In Decision Support Systems, Elsevier, 47(4):547-553, 2009.


----
Pythonによるデータ可視化の基礎（Matplotlib）_確率統計_宿題あり


```
from google.colab import drive
drive.mount('/content/drive')
```

```
# common
import pandas as pd
import numpy as np

# googleドライブから読み込む(自分の環境に合わせて要修正)
file_url = "/content/drive/MyDrive/Colab Notebooks/week5/Online Retail.xlsx"
online_retail_data = pd.ExcelFile(file_url)
```

```
# Omnicampusに提出するのはこのセル内のhomework関数のみ
def homework(target_online_retail_data_tb, n):
    !!WRITE ME!!
    return my_result
```

```
# Matplotlibで可視化してみる

import matplotlib.pyplot as plt

N = 10
data = homework(target_online_retail_data_tb, N)

fig, ax1 = plt.subplots(figsize=(6,4))

# セグメント数で横軸を決める
data_num = len(data)

# 累積和
cum_per = np.cumsum(data)

# 棒グラフ
ax1.bar(range(data_num), data)
ax1.set_xticks(range(data_num))

# 折れ線グラフ
ax2 = ax1.twinx()
ax2.plot(range(data_num), cum_per, c="k", marker="o")
ax2.set_ylim([0, 1])
ax2.grid(True, which='both', axis='y')
```

```
謝辞：以下のデータセットの利用に関して
https://archive.ics.uci.edu/ml/machine-learning-databases/00352/Online%20Retail.xlsx

引用元：Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

Daqing Chen, Sai Liang Sain, and Kun Guo, Data mining for the online retail industry: A case study of RFM model-based customer segmentation using data mining, Journal of Database Marketing and Customer Strategy Management, Vol. 19, No. 3, pp. 197â€“208, 2012 (Published online before print: 27 August 2012. doi: 10.1057/dbm.2012.17).
```


