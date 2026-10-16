# DIC-2 Multiple Linear Regression Explorer

AIoT 物聯網數據分析與應用 · DIC-2：Kaggle 50 Startups & Boston Housing

純前端網頁（HTML / CSS / JavaScript + Chart.js），依 CRISP-DM 流程進行多元線性迴歸與特徵選擇分析。

## 功能
- **下拉選單切換兩個 Problem**：50 Startups（預測 Profit）、Boston Housing（預測 MEDV）
- **任意 Dataset**：輸入 CSV raw URL 或上傳 CSV 檔，可選 target 欄位
- 5 種特徵選擇方法：Lasso、Forward SFS、RFE、ElasticNet、Exhaustive Search，比較 k = 1…p 的 test RMSE / R²
- OLS 係數、標準誤、t 檢定、p-value、95% CI、VIF、F 檢定
- 即時預測器、Actual vs Predicted、殘差圖、離群值診斷

## 結果（train/test = 80/20，seed = 42）
| Problem | 最佳 k | 選入特徵 | Test RMSE | Test R² |
|---|---|---|---|---|
| 50 Startups | 2 | R&D Spend, Marketing Spend | 9,304.12 | 0.9464 |
| Boston Housing | 11 | 去除 indus、age | 4.067 | 0.7458 |

## 資料來源
- 50 Startups：https://raw.githubusercontent.com/Avik-Jain/100-Days-Of-ML-Code/master/datasets/50_Startups.csv
- Boston Housing：https://raw.githubusercontent.com/selva86/datasets/master/BostonHousing.csv
