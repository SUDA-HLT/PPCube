# Statistics

本目录对 PPCube-Dense 中发布的人物、属性和关系相关数据统计和记录。

## `source_statistics.csv`

每行表示一个数据来源的总体数量。

| 字段 | 含义、取值与示例 |
| --- | --- |
| `source` | 数据来源。取值包括 `WD`、`DB`、`WP`、`YAGO`、`ZHDB`、`ZHWP`，例如 `WD` 表示 Wikidata。 |
| `person_count` | 人物节点记录数。取值为整数，例如 `99998`。 |
| `attribute_count` | 人物属性记录数。取值为整数，例如 `1040886`。 |
| `relation_count` | 有方向的人际关系记录数。取值为整数，例如 `381244`。 |
| `attributes_per_person` | 平均每个人物拥有的属性记录数。取值为 `attribute_count / person_count` 的计算结果，例如 `10.4091`。 |
| `relations_per_person` | 平均每个人物发出的人际关系数。取值为 `relation_count / person_count` 的计算结果，例如 `3.8125`。 |

## `attribute_statistics.csv`

每行表示某个来源中一种属性的数量。

| 字段 | 含义、取值与示例 |
| --- | --- |
| `source` | 数据来源。取值与 `source_statistics.csv` 的 `source` 相同，例如 `WD`。 |
| `attribute_id` | PPCube 属性 ID。取值对应 `../schema/attribute_types.csv` 的 `attribute_id`，例如 `AID_0008`。 |
| `attribute_label` | 属性名称。取值对应 `../schema/attribute_types.csv` 的 `attribute_label`，例如 `dateOfBirth`。 |
| `triple_count` | 当前来源中该属性的记录数。取值为整数，例如 `12345`。 |

## `relation_statistics.csv`

每行表示某个来源中一种关系的数量。

| 字段 | 含义、取值与示例 |
| --- | --- |
| `source` | 数据来源。取值与 `source_statistics.csv` 的 `source` 相同，例如 `WD`。 |
| `relation_id` | PPCube 关系 ID。取值对应 `../schema/relation_types.csv` 的 `relation_id`，例如 `RID_0002`。 |
| `relation_label` | 关系名称。取值对应 `../schema/relation_types.csv` 的 `relation_label`，例如 `father`。 |
| `triple_count` | 当前来源中该关系的记录数。取值为整数，例如 `12345`。 |
