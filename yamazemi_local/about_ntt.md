---
marp: true
theme: yamazemi-celeste
paginate: true
style: |
  :root {
    --base-font-size: 24px; /* グローバルなフォントサイズを設定 */
  }

  /* テーブル内の文字サイズを小さく */
  table, th, td {
    font-size: 18px;
  }

  .mermaid svg {
    max-width: 70vh;
    max-height: 50vh; /* 例: スライドの60%まで */
    width: auto;
    height: auto;
  }

---

<!-- _class: title -->
# Marp カスタムCSSデモ
## `yamazemi-celeste` テーマの使用例

---

<!-- _class: toc -->
# 目次

1. <span class="toc-active">テーマの基本機能</span>
2. Markdown標準要素
3. 図表（Mermaid）の使用例

---

<!-- _class: subTitle -->
# 1. テーマの基本機能
## このセクションでは、テーマの基本的な機能と使用方法を紹介します。

 1. 基本的なスライドの使い方
 2. フォントサイズの変更
 3. 2カラムレイアウト
 4. 特殊ページ
 5. 数式表示
 6. ボックスコンポーネント
 7. 矢印インジケーター
 8. タグ表示
 9. インラインスタイル要素
10. 画像スタイリング
11. コードブロック

---

# 1.1 基本的なスライド

<!-- _class: twoColumns -->
<div>
これは標準的なスライドのデモです。

`#` で指定したタイトル名は左上に、ページ番号は右上と右下に自動で表示されます。
見出しの大きさは以下の通りです。

<pre style="max-height: 200px; overflow-y: auto;">
## H2 見出し
H2見出しを使用した小見出しです。

### H3 見出し
H3見出しの表示例です。

#### H4 見出し
H4見出しの表示例です。

##### H5 見出し
H5見出しの表示例です。

###### H6 見出し
H6見出しの表示例です。

</pre>
</div>

<div>

## H2 見出し
H2見出しを使用した小見出しです。

### H3 見出し
H3見出しの表示例です。

#### H4 見出し
H4見出しの表示例です。

##### H5 見出し
H5見出しの表示例です。

###### H6 見出し
H6見出しの表示例です。
</div>

---

<!-- _class: text-sm -->
# 1.2 フォントサイズの変更（小）

<!-- _class: text-sm -->
このスライドは `text-sm` クラスを使用しているため、フォントサイズが小さくなっています。
スライド全体のフォントサイズを変更するには、スライドの区切り部分に 

`<!-- _class: text-sm -->` のようにクラスを指定します。

## 使用可能なサイズクラス
- `text-xs`: 非常に小さいテキスト (18px)
- `text-sm`: 小さいテキスト (21px)
- `text-md`: 標準サイズ (24px)
- `text-lg`: 大きいテキスト (28px)
- `text-xl`: 非常に大きいテキスト (32px)

---

<!-- _class: twoColumns text-lg -->
# 1.3 フォントサイズの変更（大）

<div>
このスライドは `text-lg` クラスを使用しているため、フォントサイズが大きくなっています。

## 部分的なサイズ変更

  ```
  同じスライド内でも<span class="text-xs">小さいテキスト</span>や<span class="text-xl">大きいテキスト</span>を混在させることができます。
  
  ```
</div>

<div>

## 部分的なサイズ変更

同じスライド内でも<span class="text-xs">小さいテキスト</span>や<span class="text-xl">大きいテキスト</span>を混在させることができます。
</div>

---

<!-- _class: twoColumns -->
# 1.4 2カラムレイアウト

<div>
  <h2>左カラム</h2>
  <p>これは2カラムレイアウトの左側です。垂直線で区切られています。</p>
  <ul>
    <li>項目 A</li>
    <li>項目 B</li>
  </ul>
</div>
<div>
  <h2>右カラム</h2>
  <p>これは右カラムです。左カラムの内容と並んで表示されます。</p>
  <p>ここでは<code>インラインコード</code>も使えます。</p>
</div>

---

<!-- _class: subTitle -->
# 1.5 サブタイトルページの例
## セクション区切りなどに使用する特殊なページです。

---

<!-- _class: grayPage -->
# 1.6 グレーページバリアント

このスライドは`grayPage`クラスを使用しています。
ヘッダーやアクセントカラーがセカンダリーカラーに変更されます。

## グレーページのH2
グレーページ専用のコンテンツです。

---

# 1.7 数式表示

KaTeXを使用した数式のレンダリングのデモです。

$$
L = \frac{1}{2} \rho v^2 S C_L
$$

上記は揚力の計算式です。

---

# 1.8 ボックスコンポーネント

<div class="box">
  <h2>基本ボックス</h2>
  <p>これは基本的なボックスコンポーネントです。背景色と左ボーダーが特徴です。</p>
</div>

---

# 1.9 カラーボックス

<div class="box blue">
  <h2>青色ボックス</h2>
  <p>これは<strong>青色</strong>のボックスです。情報の表示に適しています。</p>
</div>

<br>

<div class="box green">
  <h2>緑色ボックス</h2>
  <p>これは<strong>緑色</strong>のボックスです。成功メッセージなどに使用します。</p>
</div>

---

# 1.10 その他のカラーボックス

<div class="box yellow">
  <h2>黄色ボックス</h2>
  <p>これは<strong>黄色</strong>のボックスです。警告メッセージに適しています。</p>
</div>

<br>

<div class="box red">
  <h2>赤色ボックス</h2>
  <p>これは<strong>赤色</strong>のボックスです。エラーや重要な警告に使用します。</p>
</div>

---

# 1.11 矢印インジケーター

## 下向き矢印
<div class="downarrow"></div>
<p>上記はCSSで描画された下向き矢印です。</p>

<br>

## 上向き矢印
<div class="uparrow"></div>
<p>上記はCSSで描画された上向き矢印です。</p>

---

# 1.12 タグ表示

タグコンポーネントの表示例です。

<span class="tag main">メインタグ</span>
<span class="tag accent">アクセントタグ</span>

<p>これらのタグはキーワードやカテゴリーの強調に使用できます。</p>

---

# 1.13 インラインスタイル要素

## コードとマーク
このスライドでは<code>インラインコード</code>のスタイリングを示しています。
また、<mark>マークタグ</mark>を使用したテキストの強調表示も可能です。

## 箇条書きリスト
<ul>
  <li>リストの最初の項目</li>
  <li><code>コード</code>を含む2番目の項目</li>
  <li><mark>重要</mark>な3番目の項目</li>
</ul>

---

# 1.14 画像スタイリング

## ボーダー付き画像
この画像はalt属性に"border"を含むため、ボーダーが表示されます。
<img src="https://via.placeholder.com/300x150?text=Border+Image" alt="placeholder image border" width="300">

## 中央寄せ画像
この画像はalt属性に"center"を含むため、中央寄せになります。
<img src="https://via.placeholder.com/400x100?text=Centered+Image" alt="placeholder image center" width="400">

---

# 1.15 コードブロック (`pre`)

プリフォーマット済みコードブロックの表示例です。

<pre>
<code>
// コメント例
function 挨拶(名前) {
  return "こんにちは、" + 名前 + "さん！";
}

console.log(挨拶("世界"));
</code>
</pre>
<p>フォントは "Source Code Pro" が使用されています。</p>

---

<!-- _class: toc -->
# 目次

1. テーマの基本機能
2. <span class="toc-active">Markdown標準要素</span>
3. 図表（Mermaid）の使用例

---

<!-- _class: subTitle -->
# 2. Markdown標準要素
## このセクションでは、Markdownの標準機能の使用方法を紹介します。

 1. テーブル
 2. リスト
 3. 引用

---

# 2.1 テーブル

## 表（テーブル）

| 見出し1 | 見出し2 | 見出し3 |
|---------|---------|---------|
| セルA   | セルB   | セルC   |
| 1       | 2       | 3       |
| 〇      | ×      | △      |

---

# 2.2 リスト

## 箇条書きリスト
<ul>
  <li>りんご</li>
  <li>みかん</li>
  <li>バナナ</li>
</ul>

## 番号付きリスト
<ol>
  <li>一番目</li>
  <li>二番目</li>
  <li>三番目</li>
</ol>

---

# 2.3 引用

> これは引用文の例です。

---

<!-- _class: toc -->
# 目次

1. テーマの基本機能
2. Markdown標準要素
3. <span class="toc-active">図表（Mermaid）の使用例</span>

---

<!-- _class: subTitle -->
# 3. 図表（Mermaid）の使用例
## このセクションでは、Mermaidを使用した各種図表の作成方法を紹介します。

 1. フローチャート
 2. シーケンス図
 3. クラス図
 4. 状態遷移図
 5. ガントチャート
 6. 円グラフ
 7. エンティティ関係図
 8. ユーザージャーニー

---

# 3.1 フローチャート

<pre class="mermaid">
flowchart LR
    subgraph データ準備
        A[研究テーマの設定] --> B{データの入手可能性}
        B -->|入手可能| C[データ収集]
        B -->|入手不可| D[代替データの検討]
        D --> B
    end
    C --> E[データクリーニング]
    E --> F[記述統計]
    F --> G{モデル選択}
    G -->|線形| H[線形回帰分析]
    G -->|非線形| I[非線形モデル]
    H --> J[結果の解釈]
    I --> J
    J --> K[論文執筆]
    classDef blackText fill:#90CEB7,color:#111,stroke:#333;
    class A blackText;
    style K fill:#EC672F
</pre>

---

# 3.2 シーケンス図

<pre class="mermaid">
sequenceDiagram
    participant R as 研究者
    participant D as データセット
    participant S as 統計ソフト
    participant V as 検証

    R->>D: パネルデータ読み込み
    D->>S: データ変換
    S->>S: 固定効果モデル推定
    S->>V: ハウスマン検定
    V->>R: 検定結果
    R->>S: ランダム効果モデル推定
    S->>R: 推定結果
    R->>R: 結果の解釈
</pre>

---

# 3.3 クラス図

<pre class="mermaid">
classDiagram
    class 計量経済モデル {
        +データセット
        +変数
        +パラメータ
        +推定()
        +検定()
    }
    class 線形モデル {
        +説明変数
        +被説明変数
        +OLS推定()
    }
    class 非線形モデル {
        +非線形関数
        +最尤推定()
    }
    class 時系列モデル {
        +時系列データ
        +ARIMA推定()
    }
    計量経済モデル <|-- 線形モデル
    計量経済モデル <|-- 非線形モデル
    計量経済モデル <|-- 時系列モデル
</pre>

---

# 3.4 状態遷移図

<pre class="mermaid">
stateDiagram-v2
    [*] --> 景気拡大
    景気拡大 --> 景気後退: 転換点
    景気後退 --> 景気拡大: 転換点
    景気後退 --> [*]: 不況
    note right of 景気拡大: 実質GDP成長率 > 0%
    note right of 景気後退: 実質GDP成長率 < 0%
</pre>

---

# 3.5 ガントチャート

<pre class="mermaid">
gantt
    title 夏休みの旅行計画
    dateFormat  YYYY-MM-DD
    tickInterval 1month
    section 準備
    旅行先の選定    :done,    des1, 2024-07-01, 3d
    予算の確認      :done,    des2, 2024-07-04, 2d
    ホテル予約      :active,  des3, 2024-07-06, 2d
    section 旅行当日
    空港到着        :        des4, 2024-08-01, 1d
    観光スポット巡り :        des5, 2024-08-02, 3d
    ショッピング    :        des6, 2024-08-05, 1d

</pre>

---

# 3.6 円グラフ

<pre class="mermaid">
pie title 計量経済学研究分野の分布
    "労働経済学" : 30
    "マクロ経済学" : 25
    "産業組織論" : 20
    "開発経済学" : 15
    "その他" : 10
</pre>

---

# 3.7 エンティティ関係図

<pre class="mermaid">
erDiagram
    企業 ||--o{ 財務データ : 所有
    財務データ ||--o{ 時系列データ : 包含

    企業 {
        string 企業コード
        string 企業名
        string 業種
    }
    財務データ {
        string 企業コード
        date 会計年度
        float 売上高
        float 営業利益
        float 総資産
    }
    時系列データ {
        string 企業コード
        date 日付
        float 株価
        float 取引量
    }
</pre>

---

# 3.8 ユーザージャーニー

<pre class="mermaid">
journey
    title 計量経済学研究プロセス
    section 研究開始
        研究テーマ設定: 5: 研究者
        データ収集: 4: 研究者
    section 分析
        データクリーニング: 3: 研究者
        モデル推定: 4: 研究者
        結果の解釈: 5: 研究者
    section 論文作成
        論文執筆: 4: 研究者
        査読対応: 3: 研究者
        論文発表: 5: 研究者
</pre>

---

<!-- _class: final -->
<div class="final-logo"></div>

# ご清聴ありがとうございました