# セットカードテーブル (setcard)

## テーブル情報

| 項目                           | 値                                                                                                   |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------|
| システム名                     | etudes-stg.database                                                                                  |
| サブシステム名                 |                                                                                                      |
| スキーマ名                     | dbo                                                                                                  |
| 物理テーブル名                 | setcard                                                                                              |
| 論理テーブル名                 | セットカードテーブル                                                                                 |
| 作成者                         | y.toyoda                                                                                             |
| 作成日                         | 2024/07/17                                                                                           |
| RDBMS                          | Microsoft SQL Server 12.0.5564                                                                       |



## カラム情報

| No. | 論理名                         | 物理名                         | データ型                       | Not Null | デフォルト           | 備考                           |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|:---------|:---------------------|:-------------------------------|
|   1 | セットカードID                 | setcard_id                     | uniqueidentifier               | Yes (PK) | newid()              |                                |
|   2 | 会社ID                         | company_id                     | uniqueidentifier               |          |                      |                                |
|   3 | セットカード名                 | setcard_name                   | nvarchar(255)                  |          |                      |                                |
|   4 | セットカードコード             | setcard_code                   | varchar(255)                   |          |                      |                                |
|   5 | セットカード説明文             | setcard_description            | nvarchar(max)                  |          |                      |                                |
|   6 | セットカード画像ファイル名     | setcard_image_file_name        | nvarchar(255)                  |          |                      |                                |
|   7 | セットカード画像ファイルサイズ | setcard_image_file_size        | real                           |          |                      |                                |
|   8 | セットカード画像ファイルURL    | setcard_image_url              | varchar(500)                   |          |                      |                                |
|   9 | セットカードタイプ             | setcard_type                   | tinyint                        |          |                      | 1: 動画、2: テスト、3: アンケート、4: 集合研修、5: スライド、6: SCORM、8: テストセット、9: アンケートセット、10: 集合研修セット、11: URLカード、12: ダウンロードカード、13:提出物カード |
|  10 | 採点タイプ                     | scoring_type                   | tinyint                        |          |                      | 1: まとめて採点、2: 一問一答   |
|  11 | セットカードのカード数         | number_card                    | smallint                       |          |                      |                                |
|  12 | テスト時間                     | test_time                      | int                            |          |                      |                                |
|  13 | 完了条件タイプ                 | complete_require_type          | int                            |          |                      | 0: true-false、1: パーセント、2: ポイント |
|  14 | 完了ポイント設定               | complete_point                 | int                            |          |                      |                                |
|  15 | 合格テキスト                   | pass_text                      | nvarchar(500)                  |          |                      |                                |
|  16 | 不合格テキスト                 | not_pass_text                  | nvarchar(500)                  |          |                      |                                |
|  17 | 不合格画像url                  | not_pass_image_url             | varchar(500)                   |          |                      |                                |
|  18 | 合格画像url                    | pass_image_url                 | varchar(500)                   |          |                      |                                |
|  19 | カード順番ランダムフラグ       | random_flag                    | tinyint                        |          |                      | 0: ランダムでない、1: ランダム |
|  20 | セットカードスタータス         | setcard_status                 | tinyint                        |          |                      | 0: 非公開、1: 公開、2: 公開（エンコード中）、3: 非公開（エンコード中） |
|  21 | 全設問同一ページフラグ         | all_card_page_flag             | tinyint                        |          | 0                    | 1: 全設問同一ページ、1: １ページ１問 |
|  22 | 集合研修セットの中のカード構造タイプ | seminar_card_and_or            | tinyint                        |          |                      | 1: ANDタイプ、2: ORタイプ      |
|  23 | 作成されたユーザID             | created_user_id                | uniqueidentifier               |          |                      |                                |
|  24 | 作成したユーザタイプ           | created_user_type              | tinyint                        |          |                      | 1: スーパー管理者、2: テナント管理者、3: 会社管理者 |
|  25 | 最終更新者ID                   | last_change_user_id            | uniqueidentifier               |          |                      |                                |
|  26 | 最終更新者タイプ               | edit_user_type                 | tinyint                        |          |                      | 1: スーパー管理者、2: テナント管理者、3: 会社管理者 |
|  27 | 削除フラグ                     | delete_flag                    | tinyint                        |          | 0                    | 0: 削除していない、1:削除済    |
|  28 | 作成日時                       | created                        | datetime                       |          |                      |                                |
|  29 | 最終更新日時                   | modified                       | datetime                       |          |                      |                                |
|  30 | 共有元セットカードID           | origin_setcard_id              | uniqueidentifier               |          |                      |                                |
|  31 | 共有ステータス                 | share_status                   | tinyint                        |          | 0                    | 0: オリジナル、1: 閲覧のみ、2: 編集可、4: 複製閲覧、5: 複製編集 |
|  32 | テナントID                     | tenant_id                      | uniqueidentifier               |          |                      |                                |
|  33 |                                | test_count                     | int                            |          |                      |                                |
|  34 | テストセットの採点結果表示     | scoring_display                | tinyint                        |          | 1                    | 0: 受講生に表示しない、1:受講生に表示する |
|  35 | APIのkey                       | api_key                        | varchar(255)                   |          | NULL                 |                                |
|  36 | AIコメント生成フラグ           | feedback_option                | tinyint                        |          | NULL                 |                                |
|  37 | 最後の学習フラグ               | final_learn_flag               | tinyint                        |          | NULL                 |                                |
|  38 | APIのエンドポイント            | api_url                        | nvarchar(max)                  |          | NULL                 |                                |
|  39 | エンコードステータス           | video_status                   | tinyint                        | Yes      | 0                    | 0未処理､1:アップロード済み、2:エンコード中、3:エンコード完了、4:アップロードエラー、5:バッチ開始エラー、6:エンコードエラー |
|  40 | プロンプトテンプレート１       | prompt1                        | nvarchar(max)                  |          | NULL                 |                                |
|  41 | プロンプトテンプレート２       | prompt2                        | nvarchar(max)                  |          | NULL                 |                                |
|  42 | 言語モデルのカテゴリ番号       | llm_type                       | varchar(255)                   |          | NULL                 |                                |



## インデックス情報

| No. | インデックス名                 | カラムリスト                             | ユニーク   | オプション                     | 
|----:|:-------------------------------|:-----------------------------------------|:-----------|:-------------------------------|
|   1 | PK_setcard                     | setcard_id                               | Yes        |                                |



## 制約情報

| No. | 制約名                         | 種類                           | 制約定義                       |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|
|   1 | PK_setcard                     | PRIMARY KEY                    | setcard_id                     |



## 外部キー情報

| No. | 外部キー名                     | カラムリスト                             | 参照先                         | 参照先カラムリスト                       | ON DELETE    | ON UPDATE    |
|----:|:-------------------------------|:-----------------------------------------|:-------------------------------|:-----------------------------------------|:-------------|:-------------|



## 外部キー情報(PK側)

| No. | 外部キー名                     | カラムリスト                             | 参照元                         | 参照元カラムリスト                       | ON DELETE    | ON UPDATE    |
|----:|:-------------------------------|:-----------------------------------------|:-------------------------------|:-----------------------------------------|:-------------|:-------------|



## トリガー情報

| No. | トリガー名                     | イベント                                 | タイミング           | 条件                           |
|----:|:-------------------------------|:-----------------------------------------|:---------------------|:-------------------------------|



## RDBMS固有の情報

| No. | プロパティ名                   | プロパティ値                                                                                         |
|----:|:-------------------------------|:-----------------------------------------------------------------------------------------------------|
|   1 | name                           | setcard                                                                                              |
|   2 | object_id                      | 571149080                                                                                            |
|   3 | principal_id                   |                                                                                                      |
|   4 | schema_id                      | 1                                                                                                    |
|   5 | parent_object_id               | 0                                                                                                    |
|   6 | type                           | U                                                                                                    |
|   7 | type_desc                      | USER_TABLE                                                                                           |
|   8 | create_date                    | 2021/05/24 10:59:52                                                                                  |
|   9 | modify_date                    | 2024/05/09 8:48:34                                                                                   |
|  10 | is_ms_shipped                  | False                                                                                                |
|  11 | is_published                   | False                                                                                                |
|  12 | is_schema_published            | False                                                                                                |
|  13 | lob_data_space_id              | 1                                                                                                    |
|  14 | filestream_data_space_id       |                                                                                                      |
|  15 | max_column_id_used             | 46                                                                                                   |
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
|  49 | MS_Description                 | セットカードテーブル                                                                                 |


