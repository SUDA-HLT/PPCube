# PPCube-Dense Data

本目录包含人物节点、人物属性和人际关系三类 CSV 数据。

## `person_nodes.csv`

| 字段 | 含义、取值与示例 |
| --- | --- |
| `entity_id` | PPCube 人物 ID。取值为 `PID_` 加 12 位数字，例如 `PID_000000000001`。 |
| `entity_title` | 人物在原数据源中的实体标题或键。取值例如 `Q23`、`George_Washington`、`乔治·华盛顿`。 |
| `name` | 人物的显示名称。取值例如 `George Washington`。 |
| `pageUrl` | 人物在原数据源中的页面地址。例如 `https://www.wikidata.org/wiki/Q23`。 |

## `person_attributes_part_*.csv`

人物属性共有 3 个分片。每个分片的字段相同，合并使用时只保留一次表头。

| 字段 | 含义、取值与示例 |
| --- | --- |
| `subject_id` | 拥有该属性的人物 ID。取值对应 `person_nodes.csv` 的 `entity_id`，例如 `PID_000000000001`。 |
| `attribute_id` | PPCube 属性 ID。取值对应 `schema/attribute_types.csv` 的 `attribute_id`，例如 `AID_0008`。 |
| `object_label` | 属性值。取值可以是日期、地点、职业、组织、数字或网址，例如 `1732-02-22`。 |

## `person_relations.csv`

| 字段 | 含义、取值与示例 |
| --- | --- |
| `subject_id` | 关系出发人物的 ID。取值对应 `person_nodes.csv` 的 `entity_id`，例如 `PID_000000000001`。 |
| `relation_id` | PPCube 关系 ID。取值对应 `schema/relation_types.csv` 的 `relation_id`，例如 `RID_0002`。 |
| `object_id` | 关系指向人物的 ID。取值对应 `person_nodes.csv` 的 `entity_id`，例如 `PID_000000000002`。 |

关系方向按 `subject_id → relation_id → object_id` 理解。人物名称可通过 ID 在 `person_nodes.csv` 中查询。
