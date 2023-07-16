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
- ファイル：[ER_Fhase1.pdf](https://github.com/myaaaapon/global-job-portal-document/blob/main/ER_Fhase1.pdf)

---

# API設計
- `工数目安：6h`
- ファイル：[swagger.yml](https://github.com/myaaaapon/global-job-portal-document/blob/main/swagger.yml)

---

# 画面設計
- `[工数目安]：6ページ=7.5h`
- ファイル：[UI_Fhase1.pdf](https://github.com/myaaaapon/global-job-portal-document/blob/main/UI_Fhase1.pdf)

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

