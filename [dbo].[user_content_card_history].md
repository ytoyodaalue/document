# ユーザの受講履歴 (user_content_card_history)

## テーブル情報

| 項目                           | 値                                                                                                   |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------|
| システム名                     | etudes-stg.database                                                                                  |
| サブシステム名                 |                                                                                                      |
| スキーマ名                     | dbo                                                                                                  |
| 物理テーブル名                 | user_content_card_history                                                                            |
| 論理テーブル名                 | ユーザの受講履歴                                                                                     |
| 作成者                         | y.toyoda                                                                                             |
| 作成日                         | 2024/07/17                                                                                           |
| RDBMS                          | Microsoft SQL Server 12.0.5564                                                                       |



## カラム情報

| No. | 論理名                         | 物理名                         | データ型                       | Not Null | デフォルト           | 備考                           |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|:---------|:---------------------|:-------------------------------|
|   1 | 識別子ID                       | id                             | uniqueidentifier               | Yes (PK) | newid()              |                                |
|   2 | セットカードID                 | setcard_id                     | uniqueidentifier               |          |                      |                                |
|   3 | ユーザID                       | user_id                        | uniqueidentifier               |          |                      |                                |
|   4 | 学習ステータス                 | study_status                   | tinyint                        |          |                      | 1: 未受講、2: 受講中、3: 受講完了 |
|   5 | 進捗率                         | progress                       | float(53)                      |          |                      |                                |
|   6 | 総合計学習時間                 | total_learn_period             | int                            |          |                      | ※ 秒数                        |
|   7 | 最終見た動画位置               | last_position                  | int                            |          |                      |                                |
|   8 | 最終点数（テストの場合）       | last_total_point               | float(53)                      |          |                      |                                |
|   9 | 最終満点（テストの場合）       | last_full_point                | float(53)                      |          |                      |                                |
|  10 | 最終学習日時                   | last_learn_date                | datetime                       |          |                      |                                |
|  11 | 所要時間                       | last_learn_period              | int                            |          |                      |                                |
|  12 | 作成日時                       | created                        | datetime                       |          |                      |                                |
|  13 | 最終変更日時                   | modified                       | datetime                       |          |                      |                                |
|  14 | テナントID                     | tenant_id                      | uniqueidentifier               |          |                      |                                |
|  15 | 会社ID                         | company_id                     | uniqueidentifier               |          |                      |                                |
|  16 | 進捗学習時間                   | progress_learn_period          | int                            |          |                      | ※ 秒数                        |
|  17 | 申込履歴ID                     | user_course_register_id        | uniqueidentifier               |          |                      |                                |
|  18 |                                | real_progress                  | float(53)                      |          |                      |                                |
|  19 |                                | duration                       | nvarchar(max)                  |          |                      |                                |
|  20 |                                | test_count                     | int                            |          |                      |                                |
|  21 | 差戻申請フラグ                 | sashimodoshi_flag              | tinyint                        |          | 0                    | 1:申請中、2:差戻済             |



## インデックス情報

| No. | インデックス名                 | カラムリスト                             | ユニーク   | オプション                     | 
|----:|:-------------------------------|:-----------------------------------------|:-----------|:-------------------------------|
|   1 | PK_user_content_card_history_backup | id                                       | Yes        |                                |
|   2 | AK_userId_setcardId            | user_id,setcard_id                       | Yes        |                                |



## 制約情報

| No. | 制約名                         | 種類                           | 制約定義                       |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|
|   1 | PK_user_content_card_history_backup | PRIMARY KEY                    | id                             |
|   2 | AK_userId_setcardId            | UNIQUE                         | user_id,setcard_id             |



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
|   1 | name                           | user_content_card_history                                                                            |
|   2 | object_id                      | 1483152329                                                                                           |
|   3 | principal_id                   |                                                                                                      |
|   4 | schema_id                      | 1                                                                                                    |
|   5 | parent_object_id               | 0                                                                                                    |
|   6 | type                           | U                                                                                                    |
|   7 | type_desc                      | USER_TABLE                                                                                           |
|   8 | create_date                    | 2021/05/24 10:59:53                                                                                  |
|   9 | modify_date                    | 2021/08/02 6:54:56                                                                                   |
|  10 | is_ms_shipped                  | False                                                                                                |
|  11 | is_published                   | False                                                                                                |
|  12 | is_schema_published            | False                                                                                                |
|  13 | lob_data_space_id              | 1                                                                                                    |
|  14 | filestream_data_space_id       |                                                                                                      |
|  15 | max_column_id_used             | 22                                                                                                   |
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
|  49 | MS_Description                 | ユーザの受講履歴                                                                                     |


