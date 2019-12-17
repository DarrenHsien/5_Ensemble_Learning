# 5_Ensemble_Learning
三個臭皮匠勝過一個諸葛亮-集成學習器的大學習器


1.Voting Classifier投票學習器

	-可集成不同的學習器組合集成投票做最後的預測
	
	-voting
	
		-hard : 票票等值
		
		-票票不等值(需給予不等值的加權)


2.Bagging Classifier裝袋學習器

	-Bagging = Boostrap Aggregating
	
		對訓練數據集進行隨機取樣，並使用取樣後的數據子集，訓練每一個個體預測器
	
	-學習器

		-皆為同一種學習器，預設為decision tree

	-n_estimators : 要使用幾個弱學習器集成訓練

	-oob_score : 是否使用未被抽重的訓練數據集當成測試數據集(~1/3)
		
		


3.RandomForest Classifier隨機森林學習器



4.AdaBoost Classifer自適應強化學習器



5.GradientBoost

