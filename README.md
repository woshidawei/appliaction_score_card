预测贷款用户是否会逾期。（status是标签：0表示未逾期，1表示逾期。）

**Step1** - 构建逻辑回归模型进行预测（在构建部分数据需要进行缺失值处理和数据类型转换，如果不能处理，可以直接暴力删除）    Finance1 - Baseline.ipynb

**Step2** - 构建SVM和决策树模型进行预测    Finance1 - Baseline.ipynb

**Step3** - 构建xgboost和lightgbm模型进行预测    Finance1 - Baseline.ipynb

**Step4（模型评估）** - 记录五个模型关于accuracy、precision，recall和f1-score、auc、roc的评分表格，画出auc和roc曲线图

**Step5（特征工程1 - 数据预处理）** - 数据类型转换, 无用特征删除, 缺失值处理（尝试不同的填充看效果）及数据探索  Finance2.1 - DataPreprocessing.ipynb

**Step6（模型调优）** - 使用网格搜索对模型进行调优, 并采用五折交叉验证的方式进行模型评估  Finance3 - ModelAdjustPara.ipynb

**Step7（模型融合）** - 对Task6调优后的模型, 进行模型融合。例如, 用目前评分最高的模型作为基准模型, 和其他模型进行stacking模型融合, 得到最终模型和评分。  Finance4 - ModelFusion.ipynb

**Step8（特征工程2 - 特征选择）** - 分别用IV值和随机森林挑选特征，再构建模型，进行模型评估  Finance2.2 - FeatureSelection.ipynb

**Step9** - 利用给定数据, 调参融合得到结果。 Finance5 - Final.ipynb