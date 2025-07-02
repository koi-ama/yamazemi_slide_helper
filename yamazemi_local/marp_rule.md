# Marp スライド作成ルール（yamazemi-celeste テーマ）

---

## 1. 基本設定

- **フロントマター**
  - 先頭に必ず以下を記述：
    ```yaml
    ---
    marp: true
    theme: yamazemi-celeste
    paginate: true
    ---
    ```
  - `style:` でグローバルなCSS変数（例: `--base-font-size`）も指定可能。

- **テーマ指定**
  - `theme: yamazemi-celeste` を必ず指定。
  - テーマCSSは `theme/theme.css` を参照。

---

## 2. スライド区切り

- スライドは `---` で区切る。
- 1スライド1トピックが原則。

---

## 3. クラス指定とページバリエーション

- スライド先頭に `<!-- _class: クラス名 -->` でクラスを付与。
- 主なクラス：
  - `title`：タイトルページ
  - `subTitle`：セクション区切り
  - `toc`：目次ページ
  - `twoColumns`：2カラムレイアウト
  - `grayPage`：グレーバリアント
  - `text-xs`/`text-sm`/`text-md`/`text-lg`/`text-xl`：フォントサイズ変更
  - `final`：最終ページ
- 複数クラスはスペース区切りで併用可（例: `<!-- _class: twoColumns text-lg -->`）。

---

## 4. 目次ページ

- クラス `toc` を付与。
- 例：
  ```markdown
  <!-- _class: toc -->
  # 目次
  1. <span class="toc-active">セクション1</span>
  2. セクション2
  ```
- 現在地は `.toc-active` で強調。

---

## 5. タイトル・サブタイトルページ

- `title` クラス：
  - 1枚目に推奨。
  - ロゴが自動挿入。
  - 例：
    ```markdown
    <!-- _class: title -->
    # タイトル
    ## サブタイトル
    ```
- `subTitle` クラス：
  - セクション区切りに。
  - **各セクションの最初の小項目紹介ページ（セクション冒頭の1ページ目）でのみ使用する。**
  - スライドの背景がグレーになる。
  - 例：
    ```markdown
    <!-- _class: subTitle -->
    # セクションタイトル
    ## 補足説明
    ```

---

## 6. フォントサイズ

- スライド全体：クラスで指定（例: `text-sm`）。
- 部分的：`<span class="text-xs">小</span>` のようにspanで指定。
- サイズ一覧：
  - `text-xs`（18px）
  - `text-sm`（21px）
  - `text-md`（24px, デフォルト）
  - `text-lg`（28px）
  - `text-xl`（32px）

---

## 7. 2カラムレイアウト

- クラス `twoColumns` を付与。
- `<div>...</div><div>...</div>` で左右を分ける。
- 例：
  ```markdown
  <!-- _class: twoColumns -->
  # 2カラム例
  <div>
    左カラム内容
  </div>
  <div>
    右カラム内容
  </div>
  ```

---

## 8. ボックス・カラーボックス

- `<div class="box">...</div>` で囲む。
- 色指定：`box blue`/`box green`/`box yellow`/`box red`
- 例：
  ```html
  <div class="box blue">
    <h2>青色ボックス</h2>
    <p>内容</p>
  </div>
  ```

---

## 9. タグ・インジケーター

- タグ：`<span class="tag main">メイン</span>`、`<span class="tag accent">アクセント</span>`
- 矢印：`<div class="downarrow"></div>`、`<div class="uparrow"></div>`

---

## 10. 画像

- 通常：`![altテキスト](URL)`
- ボーダー付き：altに`border`を含める
- 中央寄せ：altに`center`を含める
- 例：
  ```markdown
  ![center border](https://...)
  ```

---

## 11. コードブロック

- ```で囲む、または`<pre><code>...</code></pre>`
- フォントは"Source Code Pro"。
- 例：
  ```
  ```js
  function hello() {
    return "Hello!";
  }
  ```
  ```

---

## 12. 数式

- KaTeX記法で`$$ ... $$`で囲む。
- 例：
  ```markdown
  $$
  L = \frac{1}{2} \rho v^2 S C_L
  $$
  ```

---

## 13. Mermaid 図表

- `<pre class="mermaid"> ... </pre>` で囲む。
- サポート図表：フローチャート、シーケンス図、クラス図、状態遷移図、ガントチャート、円グラフ、ER図、ユーザージャーニー
- 例：
  ```html
  <pre class="mermaid">
  flowchart LR
    A --> B
  </pre>
  ```

---

## 14. テーブル・リスト・引用

- Markdown標準記法でOK。
- テーブルは`|`区切り。
- リストは`-`または`*`、番号付きは`1.`
- 引用は`>`。

---

## 15. ファイナルページ

- クラス`final`を付与。
- ロゴが中央に表示。
- 例：
  ```markdown
  <!-- _class: final -->
  <div class="final-logo"></div>
  # ご清聴ありがとうございました
  ```

---

## 16. その他注意点

- セクションごとに目次ページを挿入すると親切。
- クラスやカスタム要素は`theme/theme.css`の定義に従う。
- HTMLタグはMarpでサポートされる範囲で使用。
- スライド枚数が多い場合は適宜分割。

---

## 17. 参考

- テーマCSS: `theme/theme.css`
- サンプル: `about_ntt.md`
