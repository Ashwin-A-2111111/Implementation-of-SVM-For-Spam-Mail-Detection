# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the packages.
2.Analyse the data.
3.Use modelselection and Countvectorizer to preditct the values.
4.Find the accuracy and display the result. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: MITHUN G
RegisterNumber: 212223080030
import chardet
file='/content/spam (1).csv'
with open(file, 'rb') as rawdata:
     print('Result output')
    result = chardet.detect(rawdata.read(10000))
result

import pandas as pd
data=pd.read_csv("/content/spam (1).csv",encoding="windows-1252")

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)


from sklearn.feature_extraction.text import CountVectorizer 
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)

y_pred=svc.predict(x_test)
print("y_pred")
y_pred


from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
print("accuracy")
accuracy
*/
```

## Output:

data.head()

![image](https://github.com/user-attachments/assets/23c90250-687e-4754-9426-da99fecbfa23)


data.info()

![image](https://github.com/user-attachments/assets/9b1e8883-453e-49ef-a3cc-93993f20e283)

data.isnull().sum()

![image](https://github.com/user-attachments/assets/e5c8fe47-a1ab-4e23-816f-6b4a5a36af6b)

y_pred

![image](https://github.com/user-attachments/assets/71ee53da-3479-4c2a-9d78-9c2431f69b13)

Accuracy

![image](https://github.com/user-attachments/assets/94b11567-9067-4fa0-ae07-d01eb2075a4b)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
