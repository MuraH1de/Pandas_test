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

## Pandasの欠損地処理メソッド

|:-----------|:--------------------------------|:--------------------|
| 削除        | df.dronpa()                    | 欠損地の行の削除      |
| 補完        | df.fillna(method='ffill')      | 1つ前方の値で補完     |
|            | df.fillna(method='bfill')       | 1つ後方の値で補完    |
|            | df.fillna(0)                    | 0などの任意の値で補完 |
|            | df.fillna(df.mean())            | 平均値で補完          |
|            | df.fillna(df.median())          | 中央値で補完          |
|            | df.fillna(df.mode().iloc[0,:])  | 最頻値で補完          |
| 判定        | df.isnull()                    | 欠損値かどうかの判定   |





