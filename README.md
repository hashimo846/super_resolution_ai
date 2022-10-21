# 超解像AIとは
入力画像の解像度や画質を向上させるAI。

本リポジトリにアップしたモデルは、たった20枚の画像を訓練に使用するだけで、画素数を4倍にする超解像を学習する。

![プレゼンテーション1](https://user-images.githubusercontent.com/89577008/197285430-d9e1c842-feea-40ff-b17a-fb07792bafd4.jpg)

# 使用方法
## 動作環境
* Google Colab
* Python 3.7.13
## スクリプト
* `train.ipynb` : 訓練用のスクリプト ← 実行すると超解像を行う学習モデルの訓練が行われる
* `infer.ipynb` : 推論用のスクリプト ← 実行するとテスト画像フォルダに入っている画像の超解像を行う
## ディレクトリ
* `dataset/images/` : 訓練・検証用の画像データ(計30枚)
* `dataset/test_images/` : テスト用の画像データ(計10枚) ← ここに画像を入れて`infer.ipynb`を実行すると処理される。
* `outputs/train/` : 訓練によって得られた学習済み重みが保存される
* `outputs/infer/` : 元画像(`before_*.jpg`)と超解像して得られた画像(`after_*.jpg`)が保存される
* `outputs/valid/` : 訓練中の学習曲線のグラフが保存される
