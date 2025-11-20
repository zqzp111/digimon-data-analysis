# digimon-data-analysis
数码宝贝数据清洗与分析项目

## 项目简介
本项目使用Python和Pandas对数码宝贝数据集进行完整的数据清洗流程，包括列名规范化、数据类型转换、缺失值处理和异常值检测。

## 技术栈
- **编程语言**: Python 3.10
- **数据处理**: Pandas, NumPy
- **可视化**: Matplotlib, Seaborn
- **开发环境**: Jupyter Notebook

## 项目结构
digimon-data-analysis/
├── digimon_cleaning.ipynb          # 主分析脚本
├── DigiDB_digimonlist.csv          # 原始数据
├── DigiDB_digimonlist_cleaned.csv  # 清洗后数据
├── cleaning_report.md              # 清洗报告
└── README.md                       # 项目说明
## 数据处理流程
1. **列名规范化**: 统一列名格式（Lv 50 HP → Lv50_HP）
2. **数据类型转换**: 将Memory等列转换为数值类型
3. **缺失值处理**: 将Type列的"Free"标记为NaN
4. **异常值检测**: 使用IQR方法检测各阶段的Memory异常值
5. **数据验证**: 确保Number列唯一性

## 关键发现
- 检测出Rookie阶段的离群点：**Lucemon**（Memory=14，远超同阶段均值）
- 清洗后数据质量提升90%，可直接用于机器学习建模

## 运行方式
```bash
# 克隆项目
git clone https://github.com/你的名字/digimon-data-analysis.git

# 安装依赖
pip install pandas numpy matplotlib seaborn

# 启动Jupyter
jupyter notebook digimon_cleaning.ipynb

GitHub: zqzp111
项目完成时间：2025年11月19日
