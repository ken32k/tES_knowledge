# 检索与筛选方法

制定日期：2026-10-28。当前状态：站点访问阻塞，不能宣称完成系统检索或得到相关研究总数。

## 1. 核心问题

在 AD 相关小鼠模型中，经颅交流电刺激实验使用了哪些模型、评价和行为任务、成像／细胞分子检测、电极及设备？结果的技术可复现性与因果解释如何？

## 2. 拟检索来源

- PubMed：发现原始研究和综述，核对 PMID 与摘要。
- PMC／Europe PMC：读取公开全文及补充材料。
- 出版社、模型资源或设备文件：在必要时补查明确缺失的方法；产品资料不能代替原实验报告。
- 已纳入研究的前后向引用：查找早期工作、阴性研究和方法来源。

不以仅有 40 Hz、gamma 或 Alzheimer 关键词作为纳入依据。

## 3. 检索式

先宽检索，再按方法逐篇筛选；新近研究可能尚无完整 MeSH 标引，不能只依赖 Mice[MeSH]。

```text
("transcranial alternating current stimulation" OR tACS)
AND (Alzheimer* OR amyloid OR tauopathy)
AND (mouse OR mice OR murine)

(tACS OR "alternating current stimulation")
AND (5xFAD OR "5×FAD" OR "APP/PS1" OR APPPS1 OR "APP-PS1"
     OR "3xTg-AD" OR "AppNL-G-F" OR "AppNL-F" OR PS19 OR P301S)
```

检索扩展：gamma entrainment、40 Hz、模型全名与可能的术语变体。扩展命中仍需确认是电流 tACS，而非感觉或光遗传。

2026-10-28 实际尝试：

| 查询 | 站点 | 结果 |
| --- | --- | --- |
| `"transcranial alternating current" Alzheimer mice` | PubMed | HTTPS 代理 403，未取得检索结果 |
| `"tACS" "5xFAD"` | PubMed | 同上 |
| `"tACS" "APP/PS1"` | PubMed | 同上 |
| `"alternating current stimulation" "tau" "mouse"` | PubMed | 同上 |
| `"transcranial alternating" "Alzheimer" "rat"`，用于辨别相邻物种 | PubMed | 同上 |
| `tACS Alzheimer mouse` | Europe PMC REST | HTTPS 代理 403，未取得检索结果 |

在环境确认 ready 后重试，仍为 403。失败请求不是“零篇命中”。

## 4. 纳入与相邻证据

核心：原始实验，小鼠，明确 AD 相关模型，方法支持经颅交流电刺激，至少可核查部分五维信息。

相邻证据：大鼠、正常／老龄野生型、其他 tauopathy、人体、感觉 gamma、光遗传、植入刺激、非正弦／混合波形，按实际类别单列。综述只用于追溯，不作为独立动物实验计数。

对“AD-like”诱导模型，单独记录诱导机制与局限，不能与遗传模型自动合并。对作者称 tACS 但实际接触脑表面的实验，保留原称与实际方法两个字段。

## 5. 核验层级

- `FULL_TEXT_VERIFIED`：已读方法与结果；补充材料是否核查另列。
- `ABSTRACT_VERIFIED`：只确认摘要，不填摘要未提供的方法参数。
- `SECONDARY_CITATION_ONLY`：仅从已读来源追溯的文献，不当作原始全文已读。
- `NOT_RETRIEVED`：未取得内容，不能写成原文未报告。

主证据表的 `NR` 只能用于已核查相应材料后仍未报告的字段；`NOT_VERIFIED` 表示尚未核查。相互矛盾的信息记录为 `CONFLICT` 并附位置，不能择一填成确定值。

## 6. 下一轮提取与比较

先核实物种、模型和刺激分类，再提取月龄／性别、组别、检测动物数、电极与设备；随后提取结果和指标解释。每行附原文位置，区分主要终点、探索性指标、组内与组间结果。

比较按模型与病期、刺激状态、接触层级、回流、波形和电流定义分层。对同 mA 和同目标脑内剂量的研究分别解释，不直接合并。

## 7. 当前外部前提

运行环境仍拒绝访问 `pubmed.ncbi.nlm.nih.gov`、`pmc.ncbi.nlm.nih.gov` 和 `www.ebi.ac.uk`。读取到的配置草稿已包含这些域名，当前未新增或覆盖其他网络规则。

需要通过环境设置使已有科学文献访问配置实际生效，再重试。草稿保存不等于应用或发布成功；若配置已发布但请求仍被拒绝，则需继续检查运行实例的网络访问，而非重复添加同一域名或索取凭据。公开文献查询不需要 GitHub token 或论文网站账号。
