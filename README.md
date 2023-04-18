# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file


# CODE
~~~
# data.csv
import pandas as pd
import seaborn as sbn
df=pd.read_csv("/content/data.csv")
df.info()
df.isnull().sum()from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
df['Ord_2'] = le.fit_transform(df['Ord_2'])
sbn.set(style ="darkgrid")
sbn.countplot(df['Ord_2'])from sklearn.preprocessing import OneHotEncoder
enc = OneHotEncoder()
enc = enc.fit_transform(df[['City']]).toarray()
encoded_colm = pd.DataFrame(enc)
df = pd.concat([df, encoded_colm], axis=1)
df = df.drop(['City'], axis=1)
df.head(10)
df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2'])
df.head(10)
df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1'])
df.head(10)

# encoding.csv
import pandas as pd
import seaborn as sbn
data=pd.read_csv("/content/Encoding Data.csv")
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data['ord_2'] = le.fit_transform(data['ord_2'])
sbn.set(style ="darkgrid")
sbn.countplot(data['ord_2'])
from sklearn.preprocessing import OneHotEncoder
en = OneHotEncoder()
en = en.fit_transform(data[['nom_0']]).toarray()
encoded_colm = pd.DataFrame(en)
data= pd.concat([data, encoded_colm], axis=1)
data= data.drop(['nom_0'], axis=1)
data.head(10)
data = pd.get_dummies(df, prefix=['bin_2'], columns=['bin_2'])
data.head(10)

 # titanic.csv
 import pandas as pd
import seaborn as sbn
dt=pd.read_csv("/content/titanic_dataset.csv")
dt.info()
dt.isnull().sum()
dt['Age']=dt['Age'] . fillna(dt ['Age'].mean())
dt ['Cabin']=dt['Cabin']. fillna(dt['Cabin']. mode() [0])
dt ['Embarked']=dt['Embarked'] . fillna(df ['Embarked'].mode( )[0])
dt.isnull().sum( )
from sklearn.preprocessing import LabelEncoder
lc = LabelEncoder()
df['Sex'] = lc.fit_transform(df['Sex'])
sbn.set(style ="darkgrid")
sbn.countplot(df['Sex'])
from sklearn.preprocessing import OneHotEncoder
enc= OneHotEncoder()
enc= enc.fit_transform(dt[['Name']]).toarray()
encoded_colm = pd.DataFrame(enc)
dt= pd.concat([dt, encoded_colm], axis=1)
dt= dt.drop(['Name'], axis=1)
dt.head(10)
dt = pd.get_dummies(dt, prefix=['Ticket'] ,columns=['Ticket'])
df.head(10)
dt = pd.get_dummies(dt, prefix=['Embarked'] ,columns=['Embarked'])
df.head(10)
~~~

# OUPUT
# Data.csv
![image](https://user-images.githubusercontent.com/103166779/195505218-bb3e7b02-c885-4d63-98f3-050782e58fbd.png)

![image](https://user-images.githubusercontent.com/103166779/195505336-b9a53b17-496e-4b15-b089-7bcba3d2fb23.png)

![image](https://user-images.githubusercontent.com/103166779/195505575-dc9e11a8-c85c-404c-ad2b-dbe81642f178.png)

![image](https://user-images.githubusercontent.com/103166779/195505674-724c48aa-03ce-4737-ae44-16e5e40891fa.png)

![image](https://user-images.githubusercontent.com/103166779/195505738-a54b49c4-5679-4b2c-8206-4700119d403c.png)

# Encoding.csv
![image](https://user-images.githubusercontent.com/103166779/195505926-709768cf-6e3b-4026-ab3b-c41354e5b34b.png)

![image](https://user-images.githubusercontent.com/103166779/195506002-84475387-60a7-4e9d-a82a-2d45bfb7626b.png)

![image](https://user-images.githubusercontent.com/103166779/195506088-7046df2d-aa26-40b0-8e3a-ca3aa5c6d407.png)

![image](https://user-images.githubusercontent.com/103166779/195506171-79ec4c89-bd66-4ae5-81e3-53912df3bb49.png)

# Titanic.csv
![image](https://user-images.githubusercontent.com/103166779/195506319-8bd3400e-78b7-4a3a-94ac-7507fcee13ac.png)

![image](https://user-images.githubusercontent.com/103166779/195506415-138dfb67-1807-41f2-8b1d-bcfa28efab67.png)

![image](https://user-images.githubusercontent.com/103166779/195506503-40ccee17-21af-4c63-ba01-56b5d7fcde87.png)

![image](https://user-images.githubusercontent.com/103166779/195506570-4ddbc3b8-a056-46b3-890a-e6dc1fccdaa6.png)

![image](https://user-images.githubusercontent.com/103166779/195506647-7fd7211d-7984-403f-8cb2-5b702f24498f.png)

![image](https://user-images.githubusercontent.com/103166779/195506740-662db2b2-cb43-45e3-b586-f4d875408d7d.png)


# RESULT:
   Thus the program for Feature Generation is executed successfully.


