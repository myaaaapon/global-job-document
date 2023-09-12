以下要件定義・DB設計・API設計・画面設計についてまとめています。

---

# 要件定義
- `工数目安：2h`
- `ファイル：特になし`

- 非会員
    - ユーザーを新規作成できる。
    - `共通` 全ての求人リストを見ることができる。
    - 指定項目（金額）を見る事ができない。
    - 指定URLへ飛ぶことができない。

- 会員
    - ユーザー情報を更新できる。
    - ユーザー情報を閲覧できる。
    - `共通` 全ての求人リストを見ることができる。
    - 指定項目（金額）を見る事ができる。
    - 指定URLへ飛ぶことができる。

---

# DB設計
- `工数目安：6h`
- ファイル：[Fhase1_ER.pdf](https://github.com/myaaaapon/global-job-document/blob/main/Fhase1_ER.pdf)
- 使用ツール：lucidchart

---

# API設計
- `工数目安：6h`
- ファイル：[Fhase1_API.yml](https://github.com/myaaaapon/global-job-document/blob/main/Fhase1_API.yml)
- 使用ツール：Swagger

---

# 画面設計
- `[工数目安]：6ページ=7.5h`
- ファイル：[Fhase1_UI.pdf](https://github.com/myaaaapon/global-job-document/blob/main/Fhase1_UI.pdf)
- 使用ツール：figma

- `[2h]` HOMEページ
    - `[2h]` HOMEページ `完`

- `[1.5h]` ユーザーページ
    - `[0.5h]` ユーザー登録 `完`
    - `[0.5h]` マイページ（表示） `完`
    - `[0.5h]` マイページ（編集） `完`

- `[4h]` 案件ページ
    - `[2h]` 案件検索ページ `完`
    - `[2h]` 案件詳細ページ `完`

---

# 技術選定
- `工数目安：4h`
- 個人開発のため以下を軸に選定。
    - ① `金銭面のデメリット` が少ないこと。
    - ② 後から `スケールアップ/ダウン` できる事。
    - ③アプリの要となる `スクレイピング` ができる事。

### 選定した技術
- サーバー
    - [Xserver VPS](https://vps.xserver.ne.jp/)
        - 900円/月で2GB(1年契約時)→料金青天井なクラウド利用時の金銭面のデメリットを解消。
        - 24時間体制のサポート。
        - 後からスケールアップ/ダウン可能。
        - アプリイメージで手軽に環境構築可能（Laravel、LAMP等のイメージ有）。
        - cron設定可能。
- Database
    - [PlanetScale](https://planetscale.com/)
        - 1ヶ月に10億行の読み取り、1ヶ月に1,000万行の書き込み無料。
        - ブランチ切り替え可能。
        - 日毎にバックアップ可能。
        - 東京リージョンを選択可能。
- 言語とフレームワーク
    - `バックエンド` Laravel + PHP
        - PHPでのスクレイピング経験があり、応用できると感じたため。
        - 使い慣れたフレームワークであるため。
    - `フロントエンド` TypeScript + Next.js + React
- 外部API
    - [DeepL API](https://www.deepl.com/ja/docs-api)
        - 外国語記事の翻訳に活用。
        - [精度等の複数の理由](https://takeda-no-nao.net/programming/api/translation-api-services/) により選定。
        - サービスの要なので品質を重視。
- ドメイン
    - [お名前.com](https://www.onamae.com/)
        - サイト名にも通ずるが、綴りを間違えにくいかつサービス名を端的に表す名前にしたい。
        - 候補1 `cros-so.com` 由来 海をこえて（クロスオーシャン）検索できる。
        - 証明書は [Let's Encrypt](https://letsencrypt.org/ja/) で無料に。
- プログラム
    -  [こちらの記事](https://qiita.com/tak001/items/951cee065d7c20e17a0e) を参考にChatGPTにレビューしてもらう。
    - バックエンドのフォルダ構成はクリーンアーキテクチャに則る。

---
