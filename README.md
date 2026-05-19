## 北尾早霧・砂川武貴・山田知明『定量的マクロ経済学と数値計算』日本評論社

### Google Colab 版コード

本リポジトリは、北尾早霧・砂川武貴・山田知明『[定量的マクロ経済学と数値計算](https://www.nippyo.co.jp/shop/book/9287.html)』（日本評論社）のサポートコードのうち、**Google Colab 上で実行できる Python 版**を収録しています。

ローカル環境へのインストール不要でブラウザから即座に実行できるため、手軽にコードを試したい方に最適です。

---

### フォルダ構成

```
Colab/
└── chapter4/
    ├── 1_TI_Optimization.ipynb          # 4.1.4節：時間反復法（最適化）
    └── 2_how_to_interpolation_cheb.ipynb # 付録B.1 / 4.2.1節：チェビシェフ多項式近似
```

---

### Notebook の内容

#### `1_TI_Optimization.ipynb`　―　4.1.4節：時間反復法（最適化）

無限期間の成長モデルに対して、時間反復法（TI: Time Iteration）を Python で実装します。`scipy.optimize` を用いて各グリッド点でオイラー方程式を数値的に解きます。

- オイラー方程式の残差関数の定義と `scipy.optimize` による最大化
- TI のループ構造と収束判定（政策関数の変化量）
- VFI との収束速度・精度の比較
- オイラー方程式残差による精度検証

#### `2_how_to_interpolation_cheb.ipynb`　―　付録B.1 / 4.2.1節：チェビシェフ多項式近似

チェビシェフ多項式を用いた関数近似の手法を Python で解説します。等間隔グリッドでは生じるリンギング（Runge 現象）を抑制でき、TI と組み合わせることで高精度な政策関数の近似が実現できます。

- チェビシェフ格子（コサイン格子）の生成と変数変換
- チェビシェフ多項式基底の評価と係数の推定
- 近似次数 $n$ を変えたときの精度変化の確認
- 通常の多項式近似との比較（Runge 現象の可視化）

---

### 実行方法

各 Notebook の上部にある「Open in Colab」バッジをクリックするか、Google Colab（[colab.research.google.com](https://colab.research.google.com/)）からファイルを直接開いてください。

GitHub から直接開く場合は以下の URL を利用できます：

- [4-1: TI_Optimization](https://colab.research.google.com/github/quant-macro-book/Colab/blob/main/chapter4/1_TI_Optimization.ipynb)
- [4-2: how_to_interpolation_cheb](https://colab.research.google.com/github/quant-macro-book/Colab/blob/main/chapter4/2_how_to_interpolation_cheb.ipynb)

---

### 注意

* Colab 上では Python のパッケージ（`numpy`、`scipy`、`matplotlib` 等）がプリインストールされているため、追加のインストール作業は不要です。
* Colab のセッションは一定時間操作がないと切断されます。長時間の計算を行う場合はこまめに保存してください。
* Colab 上で生成した図や計算結果をローカルに保存したい場合は、セッション内でファイルを出力し、左側のファイルパネルからダウンロードしてください。
* ローカル環境で実行したい場合は、各章の `Python/` フォルダに収録された `.ipynb` ファイルと `.py` ファイルをご利用ください。

---

### 関連リンク

- [教科書サポートページ](https://quant-macro-book.github.io/)
- [インストールと環境構築のガイド](https://quant-macro-book.github.io/setup/)（Julia / Python のローカル環境構築）
- [第4章コード（GitHub）](https://github.com/quant-macro-book/chapter4)
