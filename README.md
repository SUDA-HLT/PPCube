# PPCube-Dense V2.0

PPCube-Dense 是人物信息较丰富的子集，保留了属性和关系记录较多的人物，以及与这些人物直接关联的人物。

## 数据规模

- 人物节点记录：99,998 条
- 人物属性记录：1,040,886 条
- 人际关系记录：381,244 条

## 文件

- `data/person_nodes.csv`：人物节点数据文件。
- `data/person_attributes_part_*.csv`：人物属性数据分片，共 3 个文件，各分片表头相同。
- `data/person_relations.csv`：人际关系数据文件。
- `data/README.md`：三张数据表的字段说明。
- `schema/schema.json`：供程序读取的完整属性和关系定义。
- `schema/attribute_types.csv`：便于表格查看的属性 ID、名称、数据类型和含义。
- `schema/relation_types.csv`：便于表格查看的关系 ID、名称、数据类型和含义。
- `statistics/`：来源、属性和关系数量统计，字段见 `statistics/README.md`。
