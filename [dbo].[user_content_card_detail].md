# ユーザの受講履歴詳細 (user_content_card_detail)

## テーブル情報

| 項目                           | 値                                                                                                   |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------|
| システム名                     | etudes-stg.database                                                                                  |
| サブシステム名                 |                                                                                                      |
| スキーマ名                     | dbo                                                                                                  |
| 物理テーブル名                 | user_content_card_detail                                                                             |
| 論理テーブル名                 | ユーザの受講履歴詳細                                                                                 |
| 作成者                         | y.toyoda                                                                                             |
| 作成日                         | 2024/07/17                                                                                           |
| RDBMS                          | Microsoft SQL Server 12.0.5564                                                                       |



## カラム情報

| No. | 論理名                         | 物理名                         | データ型                       | Not Null | デフォルト           | 備考                           |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|:---------|:---------------------|:-------------------------------|
|   1 | 識別子ID                       | id                             | uniqueidentifier               | Yes (PK) | newid()              |                                |
|   2 | ユーザの受講履歴ID             | user_content_card_history_id   | uniqueidentifier               |          |                      |                                |
|   3 | 学習日時                       | learn_date                     | datetime                       |          |                      |                                |
|   4 | 学習時間（秒数）               | learn_period                   | int                            |          |                      |                                |
|   5 | 点数                           | total_point                    | float(53)                      |          |                      |                                |
|   6 | 満点                           | full_point                     | float(53)                      |          |                      |                                |
|   7 | 結果フラグ                     | result_flag                    | tinyint                        |          |                      | 0:不合格、1: 合格、2:差戻      |
|   8 | 動画再生位置                   | last_position                  | int                            |          |                      |                                |
|   9 | 作成日時                       | created                        | datetime                       |          |                      |                                |
|  10 | 最終更新日時                   | modified                       | datetime                       |          |                      |                                |
|  11 | テナントID                     | tenant_id                      | uniqueidentifier               |          |                      |                                |
|  12 | 会社ID                         | company_id                     | uniqueidentifier               |          |                      |                                |
|  13 | AIからのFBコメント             | response_content               | ntext                          |          | NULL                 |                                |



## インデックス情報

| No. | インデックス名                 | カラムリスト                             | ユニーク   | オプション                     | 
|----:|:-------------------------------|:-----------------------------------------|:-----------|:-------------------------------|
|   1 | PK_user_content_card_detail    | id                                       | Yes        |                                |
|   2 | nci_wi_user_content_card_detail_948A32A32C4FDD93D5112084E3571209 | user_content_card_history_id             |            |                                |



## 制約情報

| No. | 制約名                         | 種類                           | 制約定義                       |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|
|   1 | PK_user_content_card_detail    | PRIMARY KEY                    | id                             |



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
|   1 | name                           | user_content_card_detail                                                                             |
|   2 | object_id                      | 1419152101                                                                                           |
|   3 | principal_id                   |                                                                                                      |
|   4 | schema_id                      | 1                                                                                                    |
|   5 | parent_object_id               | 0                                                                                                    |
|   6 | type                           | U                                                                                                    |
|   7 | type_desc                      | USER_TABLE                                                                                           |
|   8 | create_date                    | 2021/05/24 10:59:53                                                                                  |
|   9 | modify_date                    | 2024/05/15 3:13:04                                                                                   |
|  10 | is_ms_shipped                  | False                                                                                                |
|  11 | is_published                   | False                                                                                                |
|  12 | is_schema_published            | False                                                                                                |
|  13 | lob_data_space_id              | 1                                                                                                    |
|  14 | filestream_data_space_id       |                                                                                                      |
|  15 | max_column_id_used             | 13                                                                                                   |
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
|  49 | MS_Description                 | ユーザの受講履歴詳細                                                                                 |


