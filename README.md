# 『Pythonで学ぶ効果検証入門』サポートページ

本リポジトリは、オーム社から発売中の『[pythonで学ぶ効果検証入門](hogehoge)』のサポートのためのページです。
ソースコードやデータの配布を行っています。


## アップデート情報
TBA

## ファイルやコード、環境について
### ファイルおよびコードについて
書籍で用いたデータおよびコードを下記の通り配布を行っております。

<details>
<summary>ファイル一覧</summary>

- data/: 本書で分析に使用するデータファイルを格納するフォルダです。
  - lenta_dataset.csv: 後述するLentaデータセットを本書の分析用途に合わせて整形したファイルです。
  - ch2_logdata.csv: 2章で行う分析用に著者側で人工的に作成したデータファイルです。
  - ch3_cluster_trial.csv: 3章で行うクラスター分析用に著者側で人工的に作成したデータファイルです。
  - ch3_noncompliance_abtest.csv: 3章で行うNon-compliance分析用に著者側で人工的に作成したデータファイルです。
  - ch3_stratified_trial.csv: 3章で行う層化A/Bテスト分析用に著者側で人工的に作成したデータファイルです。
  - ch4_organ_donations_full.csv: 4章で行うDID分析用に後述する臓器提供登録率データセットを本書の分析用途に合わせて整形したファイルです。
  - ch4_organ_donations_short.csv: 4章で行うDID分析用に後述する臓器提供登録率データセットを本書の分析用途に合わせて整形したファイルです。
  - ch5_coupon.csv: 5章で行う分析用に著者側で人工的に作成したデータファイルです。
  - ch5_coupon_v2.csv: 5章で行う分析用に著者側で人工的に作成したデータファイルです。
- notebooks/: 本書で分析に用いたJupyter Notebookファイルを格納するフォルダです。
  - chapter0_dataset.ipynb: 上述の著者側で人工的に作成したデータの作成用ファイルです。
  - chapter2.ipynb: 書籍の第2章で解説した分析に対応します。
  - chapter3_abtest_detail.ipynb: 書籍の第3章で解説した分析に対応します。
  - chapter4_did.ipynb: 書籍の第4章で解説した分析に対応します。
  - chapter5_rdd.ipynb: 書籍の第5章で解説した分析に対応します。
- pyproject.toml: プロジェクトの依存関係を管理するための設定ファイルです。
- poetry.lock: プロジェクトの依存関係のバージョンを固定するためのロックファイルです。
</details>

これらの各種データおよびコードの解説は書籍をご覧ください。

## Colabの利用について
本書ではPythonの環境として、Colabを推奨しています。
その使用方法について本レポジトリの[Colab.ipynb](https://github.com/HirotakeIto/intro_to_impact_evaluation_with_python/blob/main/notebooks/Colab.ipynb)にて解説を行っていますので、必要な方はご参照ください。


### 環境
このプロジェクトは以下の環境で動作確認を行っています。
- Python 3.8.5
- pandas >= 2.00
- numpy 1.22.2
- scipy 1.8.0
- matplotlib 3.5.1
- statsmodels 0.14.1
- seaborn 0.12.2
- jupyterlab 4.0.6
- ipython 8.0.1
- linearmodels 4.0.0
- tqdm 4.66.1
- rdrobust 1.2.1
- rddensity 2.4.1

# 本書で使用させていただいたデータセット

* [lentaデータセット](https://www.uplift-modeling.com/en/latest/api/datasets/fetch_lenta.html）)
  * 本書では、[skliftライブラリ](https://www.uplift-modeling.com/)によって提供されているLenta データセットを使用しました。
  * このデータセットは、ロシアのスーパーマーケットチェーン Lenta の顧客行動データを含んでおり、アップリフトモデリングの研究に広く利用されています。
* [臓器提供登録率データセット](https://github.com/NickCH-K/causaldata/tree/main/Python/causaldata/organ_donations)
  * 本書では、次の論文で用いられている臓器提供登録率についてのデータセットを使用しました。
      * [Kessler, J.B. and Roth, A.E., 2014. Don't take 'no' for an answer: An experiment with actual organ donor registrations. National Bureau of Economic Research working paper No. 20378.](https://www.nber.org/papers/w20378).
  * またそのデータダウンロードにあたっては[causaldataライブラリ](https://github.com/NickCH-K/causaldata)を利用しています。

# よくある質問
**Q**：書籍中で使われているコードと本レポジトリで使われているコードに微妙な差があります。

**A**：書籍で示したコードは分かりやすさを重視し、一部実際に実行しているコードと異なる表記をしているところがあります。一方でそれは処理結果に影響を与えるようなものではないため、本レポジトリのコードを正例として利用いただければ幸いです。
