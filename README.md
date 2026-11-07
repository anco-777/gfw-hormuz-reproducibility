# 海运区域船舶活动研究数据与分析代码

本仓库保存全球27个海运研究区的 Sentinel-1 SAR 船舶活动研究材料。当前已归档原公开网页的 **2026年10月24日固定版本**，包含分析代码、衍生数据、表格、空间边界、原始输入文件清单与时序核查结果。

## 下载

| 文件 | 内容 | 字节数 |
| --- | --- | ---: |
| [GFW_SAR_Reproducibility_20261024.zip](GFW_SAR_Reproducibility_20261024.zip) | 完整复现包，70个文件 | 607161 |
| [GFW_SAR_Code_20261024.zip](GFW_SAR_Code_20261024.zip) | 单独的分析代码包 | 47513 |
| [GFW_SAR_Derived_Data_20261024.zip](GFW_SAR_Derived_Data_20261024.zip) | 单独的衍生数据包 | 562733 |
| [original_release_20261024.json](original_release_20261024.json) | 原网页版本清单，保留原始来源地址与校验值 | — |

通常只需下载完整复现包并解压。若分别下载代码包和数据包，应解压到同一目录。三个压缩包均已从本仓库回读，SHA256与原公开网页公布值一致；ZIP完整性检查通过。

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

2026年10月24日固定版本用于保存原网页已发布材料，不能等同于后续修订稿的全部配套文件。后续稿件涉及的 `Reproducibility_Checked_20261027/`、`Source_Data/`、`ci_reproduction/` 尚未上传至本仓库；在这些文件补齐之前，不应将本仓库描述为最新版稿件的完整复现交付。

本文不重复分发约92.87 GiB的GFW原始CSV。原始数据需从GFW取得对应快照，并遵守其获取条件和使用条款。仓库中的原始文件清单用于定位输入数据，不包含这些原始CSV本身。

## 压缩包校验值

```text
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
