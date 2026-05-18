# 心臟病預測模型 Heart Disease Prediction

## 專案簡介
本專案使用 Cleveland Heart Disease Dataset，透過機器學習預測病人是否患有心臟病。
作為生物科學系背景的研究者，本專案結合了生理學知識與資料科學方法，
不只追求模型準確率，更著重於結果的臨床意義解讀。

## 資料集
- 來源：Kaggle - Cleveland Heart Disease Dataset
- 資料筆數：303筆病人紀錄
- 特徵數量：13個生理指標
- 目標變數：是否患有心臟病（0=沒有，1=有）

## 環境需求
- Python 3.14
- pandas
- numpy
- matplotlib
- scikit-learn

## 執行方式
1. 下載此專案
2. 安裝套件：`pip install pandas numpy matplotlib scikit-learn`
3. 開啟 `heart_disease.ipynb` 執行

## 模型比較結果

| 模型 | 準確率 |
|------|--------|
| Logistic Regression | 88.52% 🥇 |
| Random Forest | 86.89% 🥈 |
| Decision Tree | 75.41% |
| SVM | 67.21% |
| KNN | 65.57% |

## 重要發現

### 1. 最具預測力的特徵
根據 Random Forest 的特徵重要性分析，影響心臟病最關鍵的因素依序為：
- **胸痛類型（cp）**：心臟病最直接的臨床症狀
- **最大心跳速率（thalach）**：反映心臟代償功能
- **ST段下降（oldpeak）**：心肌缺血的經典心電圖指標
- **血管數量（ca）**：冠狀動脈阻塞程度的直接指標

### 2. 為什麼選擇 Logistic Regression？
比較5種模型後，Logistic Regression 表現最佳（88.52%）。
這與資料集的特性吻合：各特徵與目標變數之間存在接近線性的關係。

### 3. 醫療情境下的模型評估
在醫療預測中，準確率並非唯一指標。根據混淆矩陣分析：
- **3人** 實際有病但被預測為沒病（False Negative）
- 這類錯誤在臨床上最為危險，因為病人可能因此延誤治療
- 未來改進方向：調整模型閾值，優先降低 False Negative

## 作者
- 生物科學系背景，對生醫資料分析有濃厚興趣
- 曾以第二作者發表生理學相關論文
- GitHub: [你的GitHub連結]