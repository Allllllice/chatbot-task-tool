# chatbot-task-tool

前端頁面

1.背景：淺灰藍色
2.大標題（粗體）：任務排程計算器
3.網頁中間有一條分隔線，分隔左右兩邊

4.網頁左方顯示以下可輸入欄位
4-1.任務名稱 
4-2.總計個數
4-3.Valid 比例%
4-4.Tagger 人數
4-5.Validator 人數 
4-6.Tagger 開始日期
4-7.Validator 開始日期 
4-8.Tagger 每日單人產能
4-9.Validator 每日單人產能
4-10.每個Batch數量

格式規則
欄位1可以輸入任意內容
欄位2-5可以輸入數字
欄位6、7為日期格式
欄位8、9、10可以輸入數字

5.以上可輸入欄位下方顯示＂計算＂按鈕。
6.網頁右方區塊標題"左側計算結果"，當計算完成，下方顯示結果
7.結果欄位包含：任務名稱、Tagger需作業天數、Tagger預計完成日、Validator需作業天數、Validator預計完成日、要開幾個Batch


後端計算規則(計算後顯示於結果欄位)
1.任務名稱=輸入欄位的任務名稱，不做計算或改變
2.Tagger需作業天數=總計個數/(Tagger人數*Tagger 每日單人產能)
3.Tagger預計完成日=Tagger 開始日期+Tagger需作業天數(不含假日)
4.Validator需作業天數=(總計個數*Valid 比例%)/(Validator人數*Validator 每日單人產能)
5.Validator預計完成日=Validator 開始日期+Validator需作業天數(不含假日)
6.要開幾個Batch=總計個數/每個Batch數量
