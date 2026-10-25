# 电极形状报告的文献图片：来源与许可

补充日期：2026-10-25（Asia/Shanghai）。使用位置：[电极形状报告](../../tes-electrode-shapes.zh-CN.md)。

本目录的三张图片来自以下两篇文献，保留原图字节，未裁切、改绘、翻译图内文字、重新着色或叠加标注。中文解释位于 Markdown 图注中。图片许可与仓库文字分开，不因收入本仓库而改变。

## 1. Villamar 等（2013）的实物图

Villamar MF, Volz MS, Bikson M, Datta A, DaSilva AF, Fregni F. **Technique and considerations in the use of 4×1 ring high-definition transcranial direct current stimulation (HD-tDCS).** *Journal of Visualized Experiments*. 2013;(77):e50309. DOI：[10.3791/50309](https://doi.org/10.3791/50309)。

- [PMC 原文](https://pmc.ncbi.nlm.nih.gov/articles/PMC3735368/)
- [全文 XML 与原文许可声明](https://www.ebi.ac.uk/europepmc/webservices/rest/PMC3735368/fullTextXML)
- [文件来源：Europe PMC 官方附件 ZIP](https://www.ebi.ac.uk/europepmc/webservices/rest/PMC3735368/supplementaryFiles)
- 版权声明：**Copyright © 2013, Journal of Visualized Experiments**。
- 原文许可：**Creative Commons Attribution-NonCommercial-NoDerivs 3.0 Unported（CC BY-NC-ND 3.0）**，见[许可条款](https://creativecommons.org/licenses/by-nc-nd/3.0/)。

该图片用于本研究笔记的非商业说明，保留来源和许可。商业使用或改绘需另行取得相应授权。原文 Figure 7 图注未另列第三方转载来源；此处未选取文中标为“Modified from”等其他研究的图。不能仅因 PMC 可以阅读就认定允许转载。

<a id="villamar-fig07"></a>

### 原文 Figure 7：4×1 HD 实物配置

- 本地文件：[villamar-2013-fig07-hd-setup.jpg](villamar-2013-fig07-hd-setup.jpg)
- 附件原始文件名：`jove-77-50309-6.jpg`。
- 原图标题：*Sample 4x1 HD-tDCS setup.*
- 报告用途：展示五个带外壳组件的实际安装，区分实体结构和 4×1 布局。
- 不能据此推断：导体和皮肤足迹的具体形状、接触阻抗，或某形状优于另一形状。

## 2. Van Hoornweder 等（2024）的模型图

Van Hoornweder S, Cappozzo V, De Herde L, et al. **Head and shoulders—The impact of an extended head model on the simulation and optimization of transcranial electric stimulation.** *Imaging Neuroscience*. 2024;2:imag-2-00379. DOI：[10.1162/imag_a_00379](https://doi.org/10.1162/imag_a_00379)。

- [出版社原文](https://direct.mit.edu/imag/article/doi/10.1162/imag_a_00379/125235/Head-and-shoulders-The-impact-of-an-extended-head)
- [PMC 原文](https://pmc.ncbi.nlm.nih.gov/articles/PMC12315774/)
- [全文 XML 与原文许可声明](https://www.ebi.ac.uk/europepmc/webservices/rest/PMC12315774/fullTextXML)
- [文件来源：Europe PMC 官方附件 ZIP](https://www.ebi.ac.uk/europepmc/webservices/rest/PMC12315774/supplementaryFiles)
- 版权声明：**© 2024 The Authors**。
- 原文许可：**Creative Commons Attribution 4.0 International（CC BY 4.0）**，见[许可条款](https://creativecommons.org/licenses/by/4.0/)。

原文 Figure 1、3 图注未另列第三方图像转载来源；此处保留原样，并注明文献与许可。

<a id="ernie-fig01"></a>

### 原文 Figure 1：模型、布局与优化设计

- 本地文件：[van-hoornweder-2024-fig01-extended-model.jpg](van-hoornweder-2024-fig01-extended-model.jpg)
- 附件原始文件名：`imag_a_00379_fig1.jpg`。
- 内容：A 为扩展模型组织，B 比较截断与扩展模型的电极表示，C 显示优化设计与候选电极位置。
- 报告用途：说明电极几何应放入完整的组织与回路中评价。
- 边界：不是等面积方形与圆形的比较。C 面板将左小脑列入避让区，与正文对优化 1 的描述不一致；复现约束需核对原始代码，见[论文精读](../../ernie-extended-paper-analysis.zh-CN.md)。

<a id="ernie-fig03"></a>

### 原文 Figure 3：不同优化目标与候选位置

- 本地文件：[van-hoornweder-2024-fig03-optimization.jpg](van-hoornweder-2024-fig03-optimization.jpg)
- 附件原始文件名：`imag_a_00379_fig3.jpg`。
- 内容：上排为扩展候选位置，下排为标准 EEG 10–20 候选位置，均在扩展模型内计算；从左至右为聚焦并避让、聚焦、最大化强度。
- 报告用途：说明强度、聚焦性和非目标区约束的权衡。
- 边界：第三列色标上限不同；不是材料、形状或 tACS 频率的单因素试验。

## 3. 文件完整性与获取说明

图片均从官方附件包提取，并核对对应 ZIP 条目的 CRC 和解压后大小。Villamar 图片来自包中已完整读取的条目；该包包含大型视频，其余内容未全部下载。Ernie 附件包完整读取。没有使用残缺的图片条目，也没有把视频加入仓库。

本地三个 JPEG 文件共 381,862 字节，均保留原件内容。以下 SHA-256 清单用于核对文件一致性：

- [SHA256SUMS](SHA256SUMS)
