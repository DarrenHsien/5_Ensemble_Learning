# 5_Ensemble_Learning
三個臭皮匠勝過一個諸葛亮-集成學習器的大學習器


1.Voting Classifier投票學習器

	-可集成不同的學習器組合集成投票做最後的預測
	
	-voting
	
		-hard : 票票等值
		
		-票票不等值(需給予不等值的加權)


2.Bagging Classifier裝袋學習器

	-Bagging = Boostrap Aggregating
	
		對訓練數據集進行隨機取樣(取後放回)，並使用取樣後的數據子集，訓練每一個個體預測器
	
	-學習器

		-皆為同一種學習器，預設為decision tree

	-n_estimators : 要使用幾個弱學習器集成訓練

	-oob_score : 是否使用未被抽重的訓練數據集當成測試數據集(~1/3)
		
		


3.RandomForest Classifier隨機森林學習器
	
	-擁有兩個隨機性
	
		-Bagging : 對訓練數據集進行隨機取樣(取後放回)，並使用取樣後的數據子集，訓練每一個個體預測器
		
		-Random Selected Features : 對訓練的資料隨機提取部分的特徵予以訓練
		
	-學習器

		-皆為同一種學習器 : decision tree
	
	-n_estimators : 要使用幾個弱學習器集成訓練

	-oob_score : 是否使用未被抽重的訓練數據集當成測試數據集(~1/3)
	

4.AdaBoost Classifer自適應強化學習器

-擁有兩個自適應

	-每一筆資料都擁有一個權重(被挑選用來訓練弱學器們的機會),隨機選取k筆訓練，當某些資料預測結果與實際不符則加重該筆資料權重，讓他在下一次被選重的機會加重,重複上述動作N次，就會產生N個弱學習器

	-經過訓練之後，N個學習器上每個也有一個權重，是依據他們的準確度去分配權重，用來作後續投票加權的評分
	
	-學習器

		-皆為同一種學習器 : decision tree
	
	-n_estimators : 要使用幾個弱學習器集成訓練
	



