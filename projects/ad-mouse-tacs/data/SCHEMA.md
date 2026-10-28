# 主证据表字段说明

[studies.csv](studies.csv) 每行对应一个可区分的实验／刺激方案；同一论文的多个模型或明显不同方案可用同一 `study_id` 加不同 `experiment_id`。不能将同行的不同检测样本量默认相同。

当前仅有表头。没有经原文确认的可纳入实验行，不代表相关文献不存在。

## 1. 缺失值

- `NOT_VERIFIED`：尚未读取相应原文／补充材料。
- `NR`：核查对应材料后，未见报告；须写明已核查范围。
- `NA`：该字段不适用，说明原因。
- `CONFLICT`：不同部分矛盾，保留数值及位置，不猜测。

新增数据时避免空白含义不明；不要用 0 代替未报告。

## 2. 字段分组

| 字段 | 含义 |
| --- | --- |
| `study_id, experiment_id, title, year, doi, pmid, pmcid` | 文献与实验标识；年份和标题以可核查来源为准 |
| `source_level, inclusion_status, species` | 原文核验层级、核心／相邻／待定分类及物种 |
| `model_full_name, strain_id, genotype, background, age_at_start, age_at_endpoint, sex` | 用户关注的模型种类与病理阶段；不将 APP/PS1 简称当作完整品系 |
| `animals_per_group, endpoint_sample_sizes, groups, randomization, blinding` | 动物数、各检测动物子集及设计；视野／切片／细胞数不替代动物数 |
| `waveform, frequency_hz, current_reported, current_definition, dc_offset` | 波形、频率、原文电流及其峰值／峰峰值／RMS 定义；不自行推测 |
| `session_duration, number_of_sessions, session_interval, animal_state, anesthesia` | 时程与清醒／束缚／麻醉状态；包括原文单位 |
| `stim_electrode_site, return_electrode_site, contact_surface` | 电极定位、回流和头皮／颅骨／硬膜外等接触层级 |
| `shape, dimensions, material, coupling, fixation` | 导体与实际接触组件；必要时分别说明，不混淆面积 |
| `stimulator_brand_model, output_validation, impedance_reported, field_model` | 品牌型号、实际输出、接触检测、场模型／测量；缺失不能补猜 |
| `primary_endpoint, target_engagement` | 作者声明的主要终点与生理靶点参与证据；未声明时不事后指定 |
| `behavioral_tests, behavioral_controls` | 行为任务、具体指标、时间，以及运动／感觉／应激控制 |
| `imaging, cell_molecular, measurement_timepoints` | 成像、脑区、细胞分子检测、取材及随访时间 |
| `adverse_observations, results, limitations` | 不适／损伤观察、方向及统计、设计和解释局限；区分未报告与明确阴性 |
| `methods_location, verification_notes` | 章节、页码、图表、补充材料与矛盾／未核查之处 |

## 3. 筛选日志

[screening-log.csv](screening-log.csv) 用于保存背景、排除和待核查线索。初始记录来自本地已保存的 Altomare 等（2023）全文及本仓库既有 Benussi 摘要核验；其中两篇 gamma 小鼠背景研究只有二手引用核验，不能将其模型或设备写入主证据表。
