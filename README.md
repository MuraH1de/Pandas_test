# Pandasについてのメモ

## pandasのデータの読み込み書き込み関数

|            | Read        | Write        |
|:-----------|:------------|:-------------|
| CSV        | read_csv    | to_csv       |
| EXCEL      | read_excel  | to_excel     |
| HTML       | read_html   | to_html      |
| binary     | read_pickle | to_pickle    |


## grouper関数で集計
参考URL
https://hesma2.hatenablog.com/entry/2021/01/22/003526

## Pandasの欠損値処理メソッド

| 目的        | Method        | 説明        |
|:-----------|:--------------------------------|:----------------------|
| 削除       | df.dronpa()                     | 欠損値の行の削除      |
| 補完       | df.fillna(method='ffill')       | 1つ前方の値で補完     |
|            | df.fillna(method='bfill')       | 1つ後方の値で補完     |
|            | df.fillna(0)                    | 0などの任意の値で補完 |
|            | df.fillna(df.mean())            | 平均値で補完          |
|            | df.fillna(df.median())          | 中央値で補完          |
|            | df.fillna(df.mode().iloc[0,:])  | 最頻値で補完          |
| 判定       | df.isnull()                     | 欠損値かどうかの判定  |



## DataFrameの基本統計量を出力するメソッド
### 基本統計量を個別に出力
| Method                | 説明      |
|:----------------------|:----------|
| DataFrame.max()       | 最大値     |
| DataFrame.min()       | 最小値     |
| DataFrame.mean()      | 平均値     |
| DataFrame.median()    | 中央値     |
| DataFrame.mode()      | 最頻値     |
| DataFrame.count()     | 件数       |
| DataFrame.std()       | 標準偏差   |

### 基本統計量をまとめて出力
| Method                | パラメータ | 説明      |
|:----------------------|:----------|:----------|
| DataFrame.describe()  | max       | 最大値     |
|                       | min       | 最小値     |
|                       | mean      | 平均値     |
|                       | std       | 標準偏差   |
|                       | count     | 件数       |
|                       | 25%       | 25%-ile    |
|                       | 50%       | 中央値     |
|                       | 75%       | 75%-ile   |






