# セットカードとカードの関係テーブル (setcard_card)

## テーブル情報

| 項目                           | 値                                                                                                   |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------|
| システム名                     | etudes-stg.database                                                                                  |
| サブシステム名                 |                                                                                                      |
| スキーマ名                     | dbo                                                                                                  |
| 物理テーブル名                 | setcard_card                                                                                         |
| 論理テーブル名                 | セットカードとカードの関係テーブル                                                                   |
| 作成者                         | y.toyoda                                                                                             |
| 作成日                         | 2024/07/17                                                                                           |
| RDBMS                          | Microsoft SQL Server 12.0.5564                                                                       |



## カラム情報

| No. | 論理名                         | 物理名                         | データ型                       | Not Null | デフォルト           | 備考                           |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|:---------|:---------------------|:-------------------------------|
|   1 | セットカードカードID           | setcard_card_id                | uniqueidentifier               | Yes (PK) | newid()              |                                |
|   2 | セットカードID                 | setcard_id                     | uniqueidentifier               | Yes      |                      |                                |
|   3 | カードID                       | card_id                        | uniqueidentifier               | Yes      |                      |                                |
|   4 | 子カード種別                   | type                           | int                            |          | 1                    |  1:単体カード、2: セットカード （集合研修の場合、セットカードの中にセットカードも入れる） |
|   5 | セット内に子カードの配点       | point                          | float(53)                      |          |                      |                                |
|   6 | セット内に子カードの表示順     | order_num                      | int                            |          |                      |                                |
|   7 | 作成日時                       | created                        | datetime                       |          |                      |                                |
|   8 | 最終更新日時                   | modified                       | datetime                       |          |                      |                                |
|   9 | 論理削除フラグ                 | delete_flag                    | bit                            |          | 0                    | 0: 有効、1: 削除               |
|  10 | 共有元セットカードカードID     | origin_setcard_card_id         | uniqueidentifier               |          |                      | セットカードカードID           |
|  11 | 共有ステータス                 | share_status                   | tinyint                        |          | 0                    | 0: オリジナル、1: 閲覧のみ、2: 編集可、4: 複製閲覧、5: 複製編集 |
|  12 | 会社ID                         | company_id                     | uniqueidentifier               |          |                      |                                |
|  13 | テナントID                     | tenant_id                      | uniqueidentifier               |          |                      |                                |



## インデックス情報

| No. | インデックス名                 | カラムリスト                             | ユニーク   | オプション                     | 
|----:|:-------------------------------|:-----------------------------------------|:-----------|:-------------------------------|
|   1 | PK_card_setcard                | setcard_card_id                          | Yes        |                                |
|   2 | IDX_card_id                    | card_id                                  |            |                                |
|   3 | IDX_company_id                 | company_id                               |            |                                |
|   4 | IDX_setcard_id                 | setcard_id                               |            |                                |
|   5 | nci_wi_setcard_card_65A414E93D45BBC769EC7308D0AE4963 | setcard_id,card_id,created,modified,order_num,point,type |            |                                |



## 制約情報

| No. | 制約名                         | 種類                           | 制約定義                       |
|----:|:-------------------------------|:-------------------------------|:-------------------------------|
|   1 | PK_card_setcard                | PRIMARY KEY                    | setcard_card_id                |



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
|   1 | name                           | setcard_card                                                                                         |
|   2 | object_id                      | 603149194                                                                                            |
|   3 | principal_id                   |                                                                                                      |
|   4 | schema_id                      | 1                                                                                                    |
|   5 | parent_object_id               | 0                                                                                                    |
|   6 | type                           | U                                                                                                    |
|   7 | type_desc                      | USER_TABLE                                                                                           |
|   8 | create_date                    | 2021/05/24 10:59:52                                                                                  |
|   9 | modify_date                    | 2021/05/24 11:23:42                                                                                  |
|  10 | is_ms_shipped                  | False                                                                                                |
|  11 | is_published                   | False                                                                                                |
|  12 | is_schema_published            | False                                                                                                |
|  13 | lob_data_space_id              | 0                                                                                                    |
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
|  49 | MS_Description                 | セットカードとカードの関係テーブル                                                                   |


