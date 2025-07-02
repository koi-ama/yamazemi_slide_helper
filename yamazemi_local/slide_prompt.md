# Marp 原稿生成指示書 — Excel WS 2024

---

# Excel WS 2024

## Yamazemi Seminar

---

# 班分け

## ※ 現時点で未定のため空白

---

# 本日のアウトライン

1. 目的と位置付け
2. 事前学習の総復習
3. 解説・レクチャー
4. ワーク（15min）
5. Excel 図表作成 WS（60min）

---

# 事前学習の内容

以下の 7 つの課題ファイルを事前配布済み。（番号付きリストを使用して番号とタイトルを列挙する。）

* データ入力・セルの書式設定
* ワークシートの操作
* オブジェクトの操作
* ワークシートの印刷、ヘッダー・フッター
* 計算式・関数の入力 / 関数の基本操作
* 関数の応用操作（関数を利用した集計、条件付き論理）
* データベース機能

---

# 目的と位置付け

* **長期的目的**：社会で通用する Excel スキルの習得
* **短期的目的**：三田論・卒論で適切な図表を作成できるようにする

※ ここは昨年度 PPT の同名スライドを踏襲。テキストを簡潔に。必要であれば図やロゴを追加。

---

# グラフの種類と使用例

昨年度 PPT の画像を同ディレクトリに保存し、

* 相関散布図: **graph\_scatter\_sleep\_vs\_work.png**
* 相関散布図: **graph\_scatter\_sleep\_vs\_housework.png**

の 2 枚を貼り付ける。

```markdown
![center](graph_scatter_sleep_vs_work.png)

![center](graph_scatter_sleep_vs_housework.png)
```

---

# これまでの失敗例

* **失敗例画像**: **fail\_scatter\_raw\.png**
* **対策イメージ**: **fix\_binned\_means.png**

```markdown
![center](fail_scatter_raw.png)

![center](fix_binned_means.png)
```

---

# レクチャー（10min）

* 論文の流れと Excel 活用ポイント

  1. データ説明 — 基本統計量
  2. 予備的分析 — 散布図、回帰線
* 関数チートシート

  * 平均: """AVERAGE(range)"""
  * 条件付き平均: """AVERAGEIFS(avg\_range, crit\_range, crit)"""
  * 分散: """STDEV.S(range)"""
  * ダミー生成: """IF(condition, 1, 0)"""

> コード例はバッククォートあるいはインラインコードを活用して記述すること。

---

# ワーク（15min）

> ここでは "section\_4.md"（既に別ファイルで作成済）と同じ内容をそのまま貼り付けること。
>
> * ただし関数例は """ で囲む点に注意。

*(ワークスライド詳述は省略し、ファイルを読み込ませる運用でも可)*

---

# 当日課題 — データ準備

* 配布データ: **rawdata.xlsx**, **Questionnaire.xlsx**
* ダウンロード場所: OneDrive ▶ WS ▶ Excel ▶ 2024
* 課題シート: Excel図表WS課題シート.pdf

```markdown
<div class="box yellow">
  <h3>注</h3>
  <ul>
    <li>欠損値は 888, 999 表記。集計時は必ず除外。</li>
    <li>質問票コードは Questionnaire.xlsx を参照。</li>
  </ul>
</div>
```

---

# 当日課題 — 基本統計量

* **方法 1 (手計算)**

  * """AVERAGE""", """STDEV.S""", """AVERAGEIFS"""
  * オートフィルで効率化。

- **方法 2 (分析ツールキット)**

  * ファイル→オプション→アドイン→分析ツール。
  * 統計情報に✔を入れて実行。

---

# 当日課題 — 図表課題

**図 4‑1**
情報摂取量 × 感染予防行動, 年齢別平均
(関数 = """AVERAGEIFS""")

**図 4‑2**
情報摂取量 × 感染予防行動, 性別×年齢別平均
(関数 = """AVERAGEIFS""")

---

---

## 生成時の注意

1. **フロントマター**はスライド冒頭に記述：

   ```yaml
   ---
   marp: true
   theme: yamazemi-celeste
   paginate: true
   ---
   ```
2. 関数や数式はバッククォートではなく **"""** で囲むこと。
3. 各セクションは 1 スライド 1 トピック (必要に応じて twoColumns クラス使用)。
4. 画像ファイルは md と同ディレクトリに配置し、示したファイル名でリンク。
5. 目次ページには `.toc-active` で現在地を強調。
