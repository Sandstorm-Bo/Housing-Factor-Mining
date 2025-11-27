# 北京市房价变化分析（2023-2025）

## 项目目标
使用Python进行数据爬取、清洗、分析，并通过Web前端进行可视化展示。


## 项目结构
```
Housing-Factor-Mining/
├── backend/
│   ├── crawler/          # 爬虫代码
│   ├── data_processing/  # 数据清洗分析
│   ├── models/           # 机器学习模型
│   └── data/             # 数据存储
│       ├── raw/
│       ├── cleaned/
│       └── output/
├── frontend/             # 前端代码（Vue/React或纯JS）
├── config/               # 配置文件
├── docs/                 # 文档
└── requirements.txt      # Python依赖
```

## 快速开始

### 后端
```bash
pip install -r requirements.txt
```

### 前端
根据团队选择的技术栈自行初始化

## 核心文档
- [数据接口定义](docs/API.md) - 前后端对接标准

## 注意事项
- 爬虫需遵守robots.txt
- 数据仅供学习使用
