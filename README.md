# Lithium Promo Research 🌍

> 锂电设备国际推广平台调研系统

## 功能

针对锂电设备产品，调研各国推广平台：

**目标国家：** 美国、日本、韩国、俄罗斯、欧洲

**平台类型：**
- 🎪 展会 — InterBattery、The Battery Show、Battery Japan 等
- 🏢 B2B — ThomasNet、EC21、Monozukuri 等
- 📰 媒体 — Batteries News、The Elec、電池タイムス 等

**产品线：**
- 方形电池组装线
- 圆柱电池组装线
- 软包电池组装线
- 切叠一体机
- 注液机

## 特点

- 多引擎搜索 + 评分排序
- 生成 Excel 看板报告（5个Sheet）
- 按国家/平台类型/产品线筛选分析
- 各国推广指南（展会时间、B2B入驻、媒体PR）

## 安装

```bash
clawhub install lithium-promo-research
```

## 使用

```bash
# 完整调研
python scripts/main.py --country KR --type exhibition

# 跳过搜索，直接生成报告
python scripts/main.py --skip-search

# 指定产品线
python scripts/main.py --country US --product "方形电池组装线"
```

## 参数

| 参数 | 说明 | 默认值 |
|------|------|--------|
| --country | 目标国家 (US/JP/KR/RU/EU/ALL) | ALL |
| --type | 平台类型 (exhibition/b2b/media/all) | all |
| --product | 产品线 | 全部 |
| --output | 输出文件名 | promo_report_YYYYMMDD.xlsx |

## 输出

- Excel 报告：`data/reports/promo_report_YYYYMMDD.xlsx`
- 各国指南：`references/us.md`, `jp.md`, `kr.md`, `ru.md`, `eu.md`

## License

MIT
