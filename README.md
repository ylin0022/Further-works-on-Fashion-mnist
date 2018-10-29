README--ML and DL for Fashion-mnist
-------------
#### Programming Language  
Python 3.7  
Jupyter Notebook  
Pytorch 0.4.1(only for Try_Resnet.ipynb)  
 
|Hardware|specifications|
|:---:|:---:|  
|Processor|Intel(R) Core(TM) i7-8550U @ 1.80GHz (4 Cores)|  
|Momory|16.0GB 2400MHz DDR4|
|Storage|256GB SSD + 2TB HDD|

#### Instructions
* This submission contains all the notebook files we used, including fine-tuning parameters and 10-fold cross-validation for comparison.   
* mnist_reader.py is downloaded from https://github.com/zalandoresearch/fashion-mnist with an easy function to read data from files.  
* We mainly used 4 methods including fine-tuning parameters:  
1.DT % RF.ipynb  
2.SVM.ipynb  
3.MLPC.ipynb  
* After choosing the best parameters, we have 4 separate files using 10-fold cross-validation and corresponding analysis such as confusion matrix and ROC curve for each method:  
1.DT 10 CV.ipynb  
2.RF 10 CV.ipynb  
3.SVM 10 CV.ipynb  
4.MLPC 10 CV.ipynb  

  **In this part we used parallel for 10-fold CV and recorded the different execution time.**
* And one reference method--ResNet was mainly used for discussion and future work: 
Try_Resnet.ipynb

##### Tips to know:
* Just follow the blocks in each notebook file if you want to retry the codes because we built a clear structure for each one.  
* Please mark for the main 4 methods, and regard Resnet as a discussion and comparison method because we are still working on it.

-------------
**Speed of classifiers with 10-fold CV**  
|Classifier|Time with parallel processing(s)|Time without parallel processing(s)|  
|:---:|:---:|:---:|  
|SVM|460|1153.7|  
|MLPC|187|398|  
|Decision Tree|60|151|  
|Random Forest|344|855 

-------------
**Performance of classifiers with 10-fold CV(parallel processing)**  
|Classifier|Accuracy|Training time(s)|Predicting time(s)|Total time(s)|  
|:---:|:---:|:---:|:---:|:---:|  
|SVM|89.5%|407.82|52.18|460|  
|MLPC|87.7%|170.18|2.82|173|  
|Decision Tree|81.1%|59.8|0.2|60|  
|Random Forest|88.5%|343.14|0.86|344|  

-------------
--------Created by Yucong and Yang on 2018/10/29
