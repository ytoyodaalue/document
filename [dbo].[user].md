# user

## テーブル情報

| 項目                           | 値                                                                                                   |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------|
| システム名                     | etudes-stg.database                                                                                  |
| サブシステム名                 |                                                                                                      |
| スキーマ名                     | dbo                                                                                                  |
| 物理テーブル名                 | user                                                                                                 |
| 論理テーブル名                 |                                                                                                      |
| 作成者                         | y.toyoda                                                                                             |
| 作成日                         | 2024/07/17                                                                                           |
| RDBMS                          | Microsoft SQL Server 12.0.5564                                                                       |



## カラム情報

| No. | 論理名                         | 物理名                         | データ型                       | Not Null | デフォルト           | 備考                           |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|:---------|:---------------------|:-------------------------------|
|   1 | 識別子ID                       | id                             | uniqueidentifier               | Yes (PK) | newid()              |                                |
|   2 | 会社ID                         | company_id                     | uniqueidentifier               | Yes      |                      |                                |
|   3 | テナントID                     | tenant_id                      | uniqueidentifier               | Yes      |                      |                                |
|   4 | ログインID                     | login_id                       | varchar(255)                   | Yes      |                      | <br>                           |
|   5 | パスワード                     | password                       | varchar(255)                   |          |                      |                                |
|   6 | 名前                           | name                           | nvarchar(500)                  |          |                      |                                |
|   7 | ミドルネーム                   | middle_name                    | nvarchar(500)                  |          |                      |                                |
|   8 | 名字                           | family_name                    | nvarchar(500)                  |          |                      |                                |
|   9 | メールアドレス1                | email                          | varchar(255)                   |          |                      |                                |
|  10 | メールアドレス2                | email_2                        | varchar(255)                   |          |                      |                                |
|  11 | ユーザIDのステータス           | status                         | int                            |          | 1                    | 0: 無効、1: 公開、2: 連携      |
|  12 | 利用しない                     | admin_flag                     | int                            |          |                      |                                |
|  13 | 利用しない                     | login_type                     | int                            |          |                      |                                |
|  14 | 言語                           | language_type                  | int                            |          |                      |                                |
|  15 | 入社年月日                     | company_joining_date           | date                           |          |                      |                                |
|  16 | 入社年数                       | company_joined_years           | int                            |          |                      |                                |
|  17 | 入社月数                       | company_joined_months          | int                            |          |                      |                                |
|  18 | ユーザIDの有効期限             | id_expire_date                 | date                           |          |                      |                                |
|  19 | 利用しない                     | login_expire_date              | date                           |          |                      |                                |
|  20 | 国籍                           | nationality                    | varchar(50)                    |          |                      |                                |
|  21 | 生年月日                       | birthday                       | date                           |          |                      |                                |
|  22 | 年齢                           | age                            | int                            |          |                      |                                |
|  23 | 年齢（月数）                   | age_month                      | int                            |          |                      |                                |
|  24 | プロフィール                   | profile                        | nvarchar(max)                  |          |                      |                                |
|  25 | 備考                           | remark                         | nvarchar(max)                  |          |                      |                                |
|  26 | 画像のURL                      | image_link                     | varchar(255)                   |          |                      |                                |
|  27 | 性別                           | gender                         | tinyint                        |          |                      |                                |
|  28 | 勤務先郵便番号                 | company_post_code              | varchar(50)                    |          |                      |                                |
|  29 | 勤務先都道府県                 | company_prefecture             | nvarchar(255)                  |          |                      |                                |
|  30 | 勤務先住所                     | company_address                | nvarchar(255)                  |          |                      |                                |
|  31 | 勤務先電話番号1                | company_phone_1                | varchar(50)                    |          |                      |                                |
|  32 | 勤務先電話番号2                | company_phone_2                | varchar(50)                    |          |                      |                                |
|  33 | 自宅郵便番号                   | home_post_code                 | varchar(50)                    |          |                      |                                |
|  34 | 自宅都道府県                   | home_prefecture                | nvarchar(255)                  |          |                      |                                |
|  35 | 自宅住所                       | home_address                   | nvarchar(255)                  |          |                      |                                |
|  36 | 自宅電話番号1                  | home_phone_1                   | varchar(50)                    |          |                      |                                |
|  37 | 自宅電話番号2                  | home_phone_2                   | varchar(50)                    |          |                      |                                |
|  38 | 初期ログインフラグ             | first_login_flag               | tinyint                        |          | 0                    | 1: 初期ログイン、0: 初期ログインではない |
|  39 | 最終ログイン日時               | last_login_date_time           | datetime                       |          |                      |                                |
|  40 | パスワード再設定用のセキュリティストリング | security_string                | varchar(255)                   |          |                      |                                |
|  41 | パスワード再設定URL期限        | init_pass_expire_date_time     | datetime                       |          |                      |                                |
|  42 | 論理削除フラグ                 | delete_flag                    | tinyint                        |          | 0                    | 0: 削除しない、1: 削除         |
|  43 | 作成日時                       | created                        | datetime                       |          |                      |                                |
|  44 | 最終更新日時                   | modified                       | datetime                       |          |                      |                                |
|  45 | 名字（かな）                   | family_name_kana               | nvarchar(50)                   |          |                      |                                |
|  46 | ミドルネーム（かな）           | middle_name_kana               | nvarchar(50)                   |          |                      |                                |
|  47 | 名前（かな）                   | name_kana                      | nvarchar(50)                   |          |                      |                                |
|  48 | 名字（ローマ字）               | family_name_romaji             | nvarchar(150)                  |          |                      |                                |
|  49 | ミドルネーム（ローマ字）       | middle_name_romaji             | nvarchar(150)                  |          |                      |                                |
|  50 | 名前（ローマ字）               | name_kana_romaji               | nvarchar(150)                  |          |                      |                                |
|  51 | 採用区分コード                 | employment_code                | nvarchar(50)                   |          |                      |                                |
|  52 | 利用しない                     | competent_flag                 | int                            |          |                      |                                |
|  53 | 出向・転籍先会社名称           | transfer_company_name          | nvarchar(250)                  |          |                      |                                |
|  54 | 利用しない                     | training_flag                  | int                            |          |                      |                                |
|  55 | 利用しない                     | training_user_id               | nvarchar(250)                  |          |                      |                                |
|  56 | 留学経験有無フラグ             | is_abroad_study                | tinyint                        |          | 0                    |                                |
|  57 | TOEIC合計得点                  | toeic_total                    | int                            |          |                      |                                |
|  58 | TOEIC Listening得点            | toeic_listening                | int                            |          |                      |                                |
|  59 | TOEIC Reading得点              | toeic_reading                  | int                            |          |                      |                                |
|  60 | TOEIC受験日                    | toeic_exam_date                | datetime                       |          |                      |                                |
|  61 | 社員種別                       | user_type                      | tinyint                        | Yes      | 1                    | 1:社内　2:社外                 |
|  62 | 作成者ID                       | created_user_id                | uniqueidentifier               |          |                      |                                |
|  63 | 作成者のタイプ                 | created_user_type              | tinyint                        |          |                      |                                |
|  64 | 最終更新者ID                   | last_change_user_id            | uniqueidentifier               |          |                      |                                |
|  65 | 最終更新者タイプ               | edit_user_type                 | tinyint                        |          |                      | 1: スーパユーザ、2: テナント管理、3: 社管理者 |
|  66 | 無効された日時                 | user_inactive_datetime         | datetime                       |          |                      |                                |
|  67 | 認証コード                     | authentication_code            | varchar(50)                    |          |                      |                                |
|  68 | 認証コード作成時間             | authentication_code_created    | datetime                       |          |                      |                                |
|  69 | メール送信日時                 | send_time                      | datetime                       |          |                      |                                |
|  70 |                                | isSendMail                     | tinyint                        |          |                      |                                |
|  71 | サービス種別（現在）           | service_type                   | tinyint                        |          | 0                    | 0:一般、1:受け放題             |
|  72 | サービス種別（翌月予定）       | next_service_type              | tinyint                        |          | 0                    | 0:一般、1:受け放題             |
|  73 | 課金対象フラグ                 | billing_type                   | tinyint                        |          | 0                    | 0:請求対象、1:請求対象でない   |
|  74 | ステータス（翌月予定）         | next_status                    | tinyint                        |          | 1                    | 0:無効、1:有効                 |
|  75 | 検索用ログインID（小文字に変換した計算列カラム） | search_login_id                | varchar(510)                   |          |                      |                                |
|  76 | 検索用フルネーム（苗字＋名前を小文字に変換した計算列カラム） | search_fullname                | nvarchar(1001)                 |          |                      |                                |
|  77 | 承認者を指定した時のapiキー    | approval_key                   | nvarchar(500)                  |          |                      |                                |
|  78 | 月内有効受け放題サービス種別   | ukehoudai_count_flag           | tinyint                        |          | 0                    | 0:一般、1:受け放題  月内に1度でも受け放題になったら「１」月初にバッチでリフレッシュ |
|  79 | 月内有効ステータス             | status_count_flag              | tinyint                        |          | 0                    | 0: 無効、1: 有効  月内に1度でも有効になったら「１」月初にバッチでリフレッシュ |
|  80 | ユーザIDの有効期限From         | id_expire_date_from            | date                           |          |                      |                                |
|  81 | ユーザIDの有効期限To           | id_expire_date_to              | date                           |          |                      |                                |



## インデックス情報

| No. | インデックス名                 | カラムリスト                             | ユニーク   | オプション                     | 
|----:|:-------------------------------|:-----------------------------------------|:-----------|:-------------------------------|
|   1 | PK_user                        | id                                       | Yes        |                                |
|   2 | idx_user_tenant_id             | tenant_id                                |            |                                |
|   3 | nci_wi_user_19228E7C1D986358310FCBF110CAAACE | delete_flag,company_id,tenant_id,status,admin_flag,birthday,company_address,company_joining_date,company_phone_1,company_phone_2,company_post_code,company_prefecture,created,created_user_id,created_user_type,edit_user_type,email,email_2,family_name,family_name_kana,first_login_flag,gender,home_address,home_phone_1,home_phone_2,home_post_code,home_prefecture,id_expire_date,image_link,init_pass_expire_date_time,language_type,last_change_user_id,last_login_date_time,login_id,login_type,middle_name,middle_name_kana,modified,name,name_kana,nationality,password,profile,remark,security_string |            |                                |
|   4 | IDX_user_searchloginid         | search_login_id                          |            |                                |



## 制約情報

| No. | 制約名                         | 種類                           | 制約定義                       |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|
|   1 | PK_user                        | PRIMARY KEY                    | id                             |



## 外部キー情報

| No. | 外部キー名                     | カラムリスト                             | 参照先                         | 参照先カラムリスト                       | ON DELETE    | ON UPDATE    |
|----:|:-------------------------------|:-----------------------------------------|:-------------------------------|:-----------------------------------------|:-------------|:-------------|
|   1 | FK_user_company                | company_id                               | dbo.company                    | company_id                               |              |              |



## 外部キー情報(PK側)

| No. | 外部キー名                     | カラムリスト                             | 参照元                         | 参照元カラムリスト                       | ON DELETE    | ON UPDATE    |
|----:|:-------------------------------|:-----------------------------------------|:-------------------------------|:-----------------------------------------|:-------------|:-------------|
|   1 | FK_user_login_history_user     | id                                       | dbo.user_login_history         | user_id                                  |              |              |



## トリガー情報

| No. | トリガー名                     | イベント                                 | タイミング           | 条件                           |
|----:|:-------------------------------|:-----------------------------------------|:---------------------|:-------------------------------|



## RDBMS固有の情報

| No. | プロパティ名                   | プロパティ値                                                                                         |
|----:|:-------------------------------|:-----------------------------------------------------------------------------------------------------|
|   1 | name                           | user                                                                                                 |
|   2 | object_id                      | 1307151702                                                                                           |
|   3 | principal_id                   |                                                                                                      |
|   4 | schema_id                      | 1                                                                                                    |
|   5 | parent_object_id               | 0                                                                                                    |
|   6 | type                           | U                                                                                                    |
|   7 | type_desc                      | USER_TABLE                                                                                           |
|   8 | create_date                    | 2021/05/24 10:59:52                                                                                  |
|   9 | modify_date                    | 2022/07/06 9:22:04                                                                                   |
|  10 | is_ms_shipped                  | False                                                                                                |
|  11 | is_published                   | False                                                                                                |
|  12 | is_schema_published            | False                                                                                                |
|  13 | lob_data_space_id              | 1                                                                                                    |
|  14 | filestream_data_space_id       |                                                                                                      |
|  15 | max_column_id_used             | 98                                                                                                   |
|  16 | lock_on_bulk_load              | False                                                                                                |
|  17 | uses_ansi_nulls                | True                                                                                                 |
|  18 | is_replicated                  | False                                                                                                |
|  19 | has_replication_filter         | False                                                                                                |
|  20 | is_merge_published             | False                                                                                                |
|  21 | is_sync_tran_subscribed        | False                                                                                                |
|  22 | has_unchecked_assembly_data    | False                                                                                                |
|  23 | text_in_row_limit              | 0                                                                                                    |
|  24 | large_value_types_out_of_row   | False                                                                                                |
|  25 | is_tracked_by_cdc              | False                                                                                                |
|  26 | lock_escalation                | 0                                                                                                    |
|  27 | lock_escalation_desc           | TABLE                                                                                                |
|  28 | is_filetable                   | False                                                                                                |
|  29 | is_memory_optimized            | False                                                                                                |
|  30 | durability                     | 0                                                                                                    |
|  31 | durability_desc                | SCHEMA_AND_DATA                                                                                      |
|  32 | temporal_type                  | 0                                                                                                    |
|  33 | temporal_type_desc             | NON_TEMPORAL_TABLE                                                                                   |
|  34 | history_table_id               |                                                                                                      |
|  35 | is_remote_data_archive_enabled | False                                                                                                |
|  36 | is_external                    | False                                                                                                |
|  37 | history_retention_period       |                                                                                                      |
|  38 | history_retention_period_unit  |                                                                                                      |
|  39 | history_retention_period_unit_desc |                                                                                                      |
|  40 | is_node                        | False                                                                                                |
|  41 | is_edge                        | False                                                                                                |
|  42 | data_retention_period          | -1                                                                                                   |
|  43 | data_retention_period_unit     | -1                                                                                                   |
|  44 | data_retention_period_unit_desc | INFINITE                                                                                             |
|  45 | ledger_type                    | 0                                                                                                    |
|  46 | ledger_type_desc               | NON_LEDGER_TABLE                                                                                     |
|  47 | ledger_view_id                 |                                                                                                      |
|  48 | is_dropped_ledger_table        | False                                                                                                |
|  49 | MS_Description                 |                                                                                                      |


