# aaic-workload-dvc

AAIC WorkloadのDVCリポジトリサンプル実装

## 利用環境構築

本DVCリポジトリからデータ取得するためには、データを取得する端末でDVCの設定、及びAWS`default`認証プロファイルの設定が必要。
以下はDVCのインストール事例。

```Console
$ python3 -m venv ~/lib/pyenv/dvc
$ source ~/lib/pyenv/dvc/bin/activate
(dvc) $ pip install --upgrade pip setuptools
(dvc) $ pip install 'dvc[s3]'
```

## 使い方

`dvc import`は現在エラーになります。

```Console
$ source ~/lib/pyenv/dvc/bin/activate
(dvc) $ dvc list https://github.com/stakizawa/aaic-workload-dvc workloads
(dvc) $ dvc get https://github.com/stakizawa/aaic-workload-dvc workloads/quarter/aaicwl-2018Q1.csv.gz
(dvc) $ dvc import https://github.com/stakizawa/aaic-workload-dvc workloads/quarter/aaicwl-2018Q1.csv.gz
```
