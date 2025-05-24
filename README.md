Implementation-of-SVM-For-Spam-Mail-Detection
AIM:
To write a program to implement the SVM For Spam Mail Detection.

Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Jupyter notebook
Algorithm
1.Import the packages. 
2.Analyse the data. 
3.Use modelselection and Countvectorizer to preditct the values. 4.Find the accuracy and display the result.

Program:
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: ASHWIN A
RegisterNumber: 212223080007

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

Output:
data.head()

![17480745992147976126833012708046](https://github.com/user-attachments/assets/c4d51c00-cdee-48f6-94b2-905b96591a98)

data.info()
![17480746493951612327551566617339](https://github.com/user-attachments/assets/6457d2bb-5187-47ef-9abc-2c1c43b6ff76)

data.isnull().sum()
![1748074668962465689522310028840](https://github.com/user-attachments/assets/a64ab39b-b4ed-4ec6-aa62-006453cca095)

y_pred
![17480746949105617523271902099207](https://github.com/user-attachments/assets/08334fe0-e3cd-47c9-8b82-3a89d3dab443)

Accuracy
![17480747144125562368960462851934](https://github.com/user-attachments/assets/c0e776b5-0143-4079-a7f4-a61c6cbf1c2d)

Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
