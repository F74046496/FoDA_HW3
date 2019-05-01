# FoDA_HW3
FDA_regression_svm_nn
## HW3 Discussion
#### 資訊108 F74046496 郭旻學
### •	How did you preprocess this dataset ?
透過讀檔取得train與test資料後，分別將前一天的close price往下shift 1格，與當日close price進行比對，若有漲幅則在新增的欄位close price inc填true，否則填false。填完後再將下移的前一日close price欄位刪除，並分割close price inc 與其他feature作為x與y的資料。

### •	Which classifier reaches the highest classification accuracy in this dataset ?
在這次的比對中，其實三者的準確率都極為接近甚至近乎相同，我想是因為test data的資料筆數較少，由於我有另外拿2015/1/2~2016/12/29的資料去進行比對，三者的準確率倒是產生了明顯的差別，所以若是今天拿不同的資料進行比對，結果也會產生不同的差異。

### •	How did you improve your classifiers ?
由於這次的資料量不多，所以在NN的solver我選擇適合資料量小的lbfgs作使用，在測試的過程中其準確率也較常高於以adam作為solver的計算結果。
