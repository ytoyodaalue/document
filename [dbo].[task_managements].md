# タスク管理テーブル (task_managements)

## テーブル情報

| 項目                           | 値                                                                                                   |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------|
| システム名                     | etudes-stg.database                                                                                  |
| サブシステム名                 |                                                                                                      |
| スキーマ名                     | dbo                                                                                                  |
| 物理テーブル名                 | task_managements                                                                                     |
| 論理テーブル名                 | タスク管理テーブル                                                                                   |
| 作成者                         | y.toyoda                                                                                             |
| 作成日                         | 2024/07/17                                                                                           |
| RDBMS                          | Microsoft SQL Server 12.0.5564                                                                       |



## カラム情報

| No. | 論理名                         | 物理名                         | データ型                       | Not Null | デフォルト           | 備考                           |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|:---------|:---------------------|:-------------------------------|
|   1 |                                | id                             | uniqueidentifier               | Yes (PK) | newid()              |                                |
|   2 |                                | company_id                     | uniqueidentifier               | Yes      |                      |                                |
|   3 |                                | user_id                        | uniqueidentifier               | Yes      |                      |                                |
|   4 |                                | queue_name                     | varchar(255)                   |          |                      |                                |
|   5 |                                | lang                           | varchar(8)                     |          |                      |                                |
|   6 |                                | extension                      | varchar(8)                     |          |                      |                                |
|   7 |                                | filename                       | nvarchar(255)                  |          |                      |                                |
|   8 |                                | conditions_json                | nvarchar(max)                  |          |                      |                                |
|   9 | 手動メールで日時指定があるときはkeyが保存される | extras_json                    | nvarchar(max)                  |          |                      |                                |
|  10 |                                | start_time                     | datetime                       |          |                      |                                |
|  11 |                                | finish_time                    | datetime                       |          |                      |                                |
|  12 |                                | progress                       | int                            | Yes      | 0                    |                                |
|  13 |                                | results_json                   | nvarchar(max)                  |          |                      |                                |
|  14 |                                | delete_flag                    | tinyint                        | Yes      | 0                    |                                |
|  15 |                                | created                        | datetime                       | Yes      | getdate()            |                                |
|  16 |                                | modified                       | datetime                       |          |                      |                                |
|  17 | タイプ                         | task_management_type_id        | int                            | Yes      | 1                    | 1:ダウンロード、2:アップロード、3:その他タスク処理 |
|  18 |                                | tenant_id                      | uniqueidentifier               |          |                      |                                |
|  19 | バッチステータス               | status                         | int                            |          |                      | 0: 未処理、1: 受付、2: 処理中、3: 完了、4: エラー終了、5: 中止済 |
|  20 | インポートファイルURL          | import_file_url                | varchar(max)                   |          |                      |                                |
|  21 | エクスポートファイルURL        | export_file_url                | varchar(max)                   |          |                      |                                |
|  22 | メモ                           | remark                         | nvarchar(max)                  |          |                      |                                |



## インデックス情報

| No. | インデックス名                 | カラムリスト                             | ユニーク   | オプション                     | 
|----:|:-------------------------------|:-----------------------------------------|:-----------|:-------------------------------|
|   1 | PK__task_man__3213E83FB6CD932F | id                                       | Yes        |                                |



## 制約情報

| No. | 制約名                         | 種類                           | 制約定義                       |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|
|   1 | PK__task_man__3213E83FB6CD932F | PRIMARY KEY                    | id                             |



## 外部キー情報

| No. | 外部キー名                     | カラムリスト                             | 参照先                         | 参照先カラムリスト                       | ON DELETE    | ON UPDATE    |
|----:|:-------------------------------|:-----------------------------------------|:-------------------------------|:-----------------------------------------|:-------------|:-------------|
|   1 | fk_task_management_type_id     | task_management_type_id                  | dbo.task_management_types      | id                                       |              |              |



## 外部キー情報(PK側)

| No. | 外部キー名                     | カラムリスト                             | 参照元                         | 参照元カラムリスト                       | ON DELETE    | ON UPDATE    |
|----:|:-------------------------------|:-----------------------------------------|:-------------------------------|:-----------------------------------------|:-------------|:-------------|



## トリガー情報

| No. | トリガー名                     | イベント                                 | タイミング           | 条件                           |
|----:|:-------------------------------|:-----------------------------------------|:---------------------|:-------------------------------|



## RDBMS固有の情報

| No. | プロパティ名                   | プロパティ値                                                                                         |
|----:|:-------------------------------|:-----------------------------------------------------------------------------------------------------|
|   1 | name                           | task_managements                                                                                     |
|   2 | object_id                      | 1003150619                                                                                           |
|   3 | principal_id                   |                                                                                                      |
|   4 | schema_id                      | 1                                                                                                    |
|   5 | parent_object_id               | 0                                                                                                    |
|   6 | type                           | U                                                                                                    |
|   7 | type_desc                      | USER_TABLE                                                                                           |
|   8 | create_date                    | 2021/05/24 10:59:52                                                                                  |
|   9 | modify_date                    | 2023/09/28 7:40:42                                                                                   |
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
|  49 | MS_Description                 | タスク管理テーブル                                                                                   |


