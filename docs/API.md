# 数据接口文档

## 概述
本文档定义前后端数据交互的JSON格式规范。所有JSON文件存放在 `backend/data/output/` 目录。

## 1. 时间序列趋势数据
**文件名**: `price_trend.json`

```json
{
  "months": ["2023-01", "2023-02", "2023-03", "..."],
  "prices": [55000, 54800, 54500, "..."],
  "mom_change": [0, -0.36, -0.55, "..."],
  "yoy_change": [null, null, null, "..."]
}
```

**字段说明**:
- `months`: 月份数组（格式：YYYY-MM）
- `prices`: 对应月份的平均房价（单位：元/㎡）
- `mom_change`: 环比涨跌幅（%）
- `yoy_change`: 同比涨跌幅（%，前12个月为null）

---

## 2. 行政区对比数据
**文件名**: `district_comparison.json`

```json
{
  "districts": ["海淀", "朝阳", "东城", "西城", "..."],
  "avg_prices": [75000, 65000, 70000, 68000, "..."],
  "price_changes": [-1.2, -0.8, -1.5, -0.9, "..."]
}
```

---

## 3. 环线分析数据
**文件名**: `ring_analysis.json`

```json
{
  "rings": ["2环内", "2-3环", "3-4环", "4-5环", "5-6环", "6环外"],
  "prices": [85000, 70000, 55000, 40000, 35000, 25000]
}
```

---

## 4. 特征重要性数据
**文件名**: `feature_importance.json`

```json
{
  "features": ["区域", "环线", "月份趋势", "政策因素", "季节性"],
  "importance": [0.35, 0.25, 0.15, 0.12, 0.13],
  "model": "RandomForest"
}
```

---

## 注意事项
- 所有JSON文件统一使用UTF-8编码
- 数字类型不要用字符串
- 时间格式统一为 `YYYY-MM`
