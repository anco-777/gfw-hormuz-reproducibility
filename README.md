# 海运区域船舶活动研究数据与分析代码

本仓库保存全球27个海运研究区的 Sentinel-1 SAR 船舶活动研究材料。现已同时保存 **后续修订稿配套材料（2026年11月7日整理）** 和原公开网页的 **2026年10月24日固定版本**，包含分析代码、衍生数据、图表源数据、空间边界、原始输入文件清单、置信区间与时序核查材料。

## 下载

| 文件 | 内容 | 字节数 |
| --- | --- | ---: |
| [GFW_SAR_GitHub_Materials_20261107.zip](GFW_SAR_GitHub_Materials_20261107.zip) | 修订稿配套包：201个研究材料文件及3个说明/清单文件 | 4478022 |
| [GFW_SAR_Reproducibility_20261024.zip](GFW_SAR_Reproducibility_20261024.zip) | 完整复现包，70个文件 | 607161 |
| [GFW_SAR_Code_20261024.zip](GFW_SAR_Code_20261024.zip) | 单独的分析代码包 | 47513 |
| [GFW_SAR_Derived_Data_20261024.zip](GFW_SAR_Derived_Data_20261024.zip) | 单独的衍生数据包 | 562733 |
| [original_release_20261024.json](original_release_20261024.json) | 原网页版本清单，保留原始来源地址与校验值 | — |

**复核后续修订稿请先下载 `GFW_SAR_GitHub_Materials_20261107.zip`。** 若需要重现原网页的固定版本，请下载2026年10月24日完整复现包；该版本的代码包和数据包也可分别下载并解压到同一目录。三个旧版压缩包已从本仓库回读，SHA256与原公开网页公布值一致；新版压缩包的Git对象哈希与上传前文件完全一致。四个压缩包均通过ZIP完整性检查。

## 原网页各项材料的位置

以下路径均相对于完整包解压后的 `Reproducibility/` 目录。

| 原网页材料 | 包内路径 |
| --- | --- |
| 使用说明与运行环境 | `README.md`、`requirements_audit.txt`、`requirements_figures.txt` |
| 27区精确坐标 | `data/regions_27.geojson` |
| 坐标参考系说明 | `data/coordinate_reference_system.json` |
| 228个原始文件清单 | `results/completed_raw/raw_input_inventory.csv` |
| 完整时序诊断摘要 | `results/temporal_order/temporal_order_summary.json` |
| 432组时序核查 | `results/temporal_order/all_temporal_order_sensitivities.csv` |
| 时序图 | `results/temporal_order/temporal_order_daily_and_7day.png`、同名PDF |
| 分析与复核代码 | `code/`、`source/original_code/` |
| 逐日统计、AIS分组、历史基准、面积与窗口敏感性 | `data/`、`results/completed_raw/` |
| 论文表格CSV | `tables/` |
| 文件校验清单 | `SHA256SUMS.csv` |

## 版本边界

两个版本分别保留，不混合覆盖。修订稿配套包取自2026年11月6日校对配套材料，整理日期为2026年11月7日；201个研究材料文件保留原字节内容，另附README及文件清单。

| 修订稿配套包内目录 | 用途 | 文件数 |
| --- | --- | ---: |
| `Reproducibility_Checked_20261027/` | 边界、衍生数据、原始文件清单、分析代码与历史核查材料 | 130 |
| `Source_Data/` | 36项图表及补充说明索引、图表数值和显示值CSV | 40 |
| `ci_reproduction/` | 置信区间计算程序、输入与结果 | 31 |

先阅读 `Source_Data/figure_table_index.csv`；索引路径以修订稿配套包根目录为起点。36项索引的文件路径均存在，复算包已有128项SHA256及置信区间18项输入SHA256全部吻合。本次核查针对迁移完整性，没有重新运行92.87 GiB原始CSV分析或统计计算。

代码入口包括 `Reproducibility_Checked_20261027/code/run_completed_raw.py`、`Reproducibility_Checked_20261027/code/verify_temporal_order.py`、`Reproducibility_Checked_20261027/boundary/code/compute_cape_boundary.py` 和 `ci_reproduction/calculate_ci.py`。具体运行方法与依赖见包内README和requirements文件。

配套包中的图表编号和说明保持来源版本，不自动替代后续手工修改的稿件文字。包内 `LEGACY_DOWNLOADS.csv` 和README中的旧版迁移状态记录的是组包时情况；旧版三个压缩包现已单独归档在本仓库，下载入口见上表。

本文不重复分发约92.87 GiB的GFW原始CSV。原始数据需从GFW取得对应快照，并遵守其获取条件和使用条款。仓库中的原始文件清单用于定位输入数据，不包含这些原始CSV本身。

## 压缩包校验值

```text
73bfda65209a6502d87f66cd8c02f434b1d11334dd3c6a20bb102370a3d96a3a  GFW_SAR_GitHub_Materials_20261107.zip
aa0afeb295440edd9bfbeb2469fe58e73b86d91d24ec7450ead02e2229fb246f  GFW_SAR_Reproducibility_20261024.zip
9b8223c3a5bb9cb6a230fd91e1bc25932674883d278f9f40c9e7d48199f125dc  GFW_SAR_Code_20261024.zip
497746eb290381859279bec66708bd8a940d47266a717a59c5a0b501236d0923  GFW_SAR_Derived_Data_20261024.zip
```

## 数据与代码来源

- [原公开下载入口（2026年10月24日固定版本）](https://gfw-hormuz-reproducibility-20261024.bold-wasp-3237.chatgpt.site/)
- [GFW原始数据下载入口](https://globalfishingwatch.org/datasets-and-code/)
- [上游SAR检测研究代码](https://github.com/GlobalFishingWatch/paper-industrial-activity)
- [上游SAR与AIS匹配研究代码](https://github.com/GlobalFishingWatch/paper-longline-ais-sar-matching)

第三方数据、代码及底图保留各自的权利和使用条款。文献DOI、维基百科与其他来源链接仍作为出处引用。本仓库尚未分配DOI。
