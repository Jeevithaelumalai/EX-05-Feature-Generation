# EX-05-Feature-Generation


## AIM :
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation :
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM :
### STEP 1 :
Read the given Data
### STEP 2 :
Clean the Data Set using Data Cleaning Process
### STEP 3 :
Apply Feature Generation techniques to all the feature of the data set
### STEP 4 :
Save the data to the file


# PROGRAM :
```
Program Developed: Jeevitha.E
Register number:212222230054
```
# CODE :
# Encoding Data.csv :
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
# Data.csv :
```
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
# Titanic_dataset.csv :
```
df2 = pd.read_csv("titanic_dataset.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Sex'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])
df2
```
# OUTPUT :
# Encoding Data.csv :
# df.head() :
![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/f1d9f200-18d6-4a64-9c60-9b2e4fca0264)

# Ordinal encoder :

![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/e7c5d245-e703-4854-a825-83a72efe1f9a)


# Label encoder :
![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/95a104f1-3559-4fbb-89b0-b70c1db26508)

# binary encoder():
![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/0519f4a3-8fa7-42d4-b856-c4efe4f223e9)

![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/9180bebc-de0c-4b0a-b1e2-7ef083c3166b)

# data.csv :
# df.head():
![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/4883cf5a-3a9e-4d29-9f00-3efa6a0dca64)

# Ordinal Encoder :
![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/4c578bd4-7863-44c0-98ef-a83bfa9fff4e)

![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/c04a28bf-0212-4cac-850b-6450d66a910a)

# label encoder :
![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/6a03f7a1-a983-4a5b-b266-676cdc7d045e)

# binary encoder ():
![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/d70f9b56-7a89-4722-8fee-df0e1ad2c5c3)

![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/d4f04b97-8c60-4ee4-93dd-1a0cc4483ab9)

# titanic_dataset.csv :
# df.head :
![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/80a958d3-6018-489f-b70a-05d71a70edf1)

# Binary encoder ():
![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/0862fcde-40a4-49d3-a764-768782579ea4)

![image](https://github.com/Jeevithaelumalai/EX-05-Feature-Generation/assets/118708245/2d4a04da-d34a-4c3c-adbb-d2ba00170223)

# RESULT:
The Feature Generation process was performed and saved the data to a file.
