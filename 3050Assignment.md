```python
import pandas as pd
```


```python
data = pd.read_csv("Desktop/clarku-assignment1/application_record.csv")
```


```python
data1 = pd.read_csv("Desktop/clarku-assignment1/credit_record.csv")
```


```python
df = pd.DataFrame(data)
```


```python
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ID</th>
      <th>CODE_GENDER</th>
      <th>FLAG_OWN_CAR</th>
      <th>FLAG_OWN_REALTY</th>
      <th>CNT_CHILDREN</th>
      <th>AMT_INCOME_TOTAL</th>
      <th>NAME_INCOME_TYPE</th>
      <th>NAME_EDUCATION_TYPE</th>
      <th>NAME_FAMILY_STATUS</th>
      <th>NAME_HOUSING_TYPE</th>
      <th>DAYS_BIRTH</th>
      <th>DAYS_EMPLOYED</th>
      <th>FLAG_MOBIL</th>
      <th>FLAG_WORK_PHONE</th>
      <th>FLAG_PHONE</th>
      <th>FLAG_EMAIL</th>
      <th>OCCUPATION_TYPE</th>
      <th>CNT_FAM_MEMBERS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5008804</td>
      <td>M</td>
      <td>Y</td>
      <td>Y</td>
      <td>0</td>
      <td>427500.0</td>
      <td>Working</td>
      <td>Higher education</td>
      <td>Civil marriage</td>
      <td>Rented apartment</td>
      <td>-12005</td>
      <td>-4542</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5008805</td>
      <td>M</td>
      <td>Y</td>
      <td>Y</td>
      <td>0</td>
      <td>427500.0</td>
      <td>Working</td>
      <td>Higher education</td>
      <td>Civil marriage</td>
      <td>Rented apartment</td>
      <td>-12005</td>
      <td>-4542</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>NaN</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>5008806</td>
      <td>M</td>
      <td>Y</td>
      <td>Y</td>
      <td>0</td>
      <td>112500.0</td>
      <td>Working</td>
      <td>Secondary / secondary special</td>
      <td>Married</td>
      <td>House / apartment</td>
      <td>-21474</td>
      <td>-1134</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>Security staff</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5008808</td>
      <td>F</td>
      <td>N</td>
      <td>Y</td>
      <td>0</td>
      <td>270000.0</td>
      <td>Commercial associate</td>
      <td>Secondary / secondary special</td>
      <td>Single / not married</td>
      <td>House / apartment</td>
      <td>-19110</td>
      <td>-3051</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>Sales staff</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5008809</td>
      <td>F</td>
      <td>N</td>
      <td>Y</td>
      <td>0</td>
      <td>270000.0</td>
      <td>Commercial associate</td>
      <td>Secondary / secondary special</td>
      <td>Single / not married</td>
      <td>House / apartment</td>
      <td>-19110</td>
      <td>-3051</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>Sales staff</td>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ID</th>
      <th>CNT_CHILDREN</th>
      <th>AMT_INCOME_TOTAL</th>
      <th>DAYS_BIRTH</th>
      <th>DAYS_EMPLOYED</th>
      <th>FLAG_MOBIL</th>
      <th>FLAG_WORK_PHONE</th>
      <th>FLAG_PHONE</th>
      <th>FLAG_EMAIL</th>
      <th>CNT_FAM_MEMBERS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>4.385570e+05</td>
      <td>438557.000000</td>
      <td>4.385570e+05</td>
      <td>438557.000000</td>
      <td>438557.000000</td>
      <td>438557.0</td>
      <td>438557.000000</td>
      <td>438557.000000</td>
      <td>438557.000000</td>
      <td>438557.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>6.022176e+06</td>
      <td>0.427390</td>
      <td>1.875243e+05</td>
      <td>-15997.904649</td>
      <td>60563.675328</td>
      <td>1.0</td>
      <td>0.206133</td>
      <td>0.287771</td>
      <td>0.108207</td>
      <td>2.194465</td>
    </tr>
    <tr>
      <th>std</th>
      <td>5.716370e+05</td>
      <td>0.724882</td>
      <td>1.100869e+05</td>
      <td>4185.030007</td>
      <td>138767.799647</td>
      <td>0.0</td>
      <td>0.404527</td>
      <td>0.452724</td>
      <td>0.310642</td>
      <td>0.897207</td>
    </tr>
    <tr>
      <th>min</th>
      <td>5.008804e+06</td>
      <td>0.000000</td>
      <td>2.610000e+04</td>
      <td>-25201.000000</td>
      <td>-17531.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>5.609375e+06</td>
      <td>0.000000</td>
      <td>1.215000e+05</td>
      <td>-19483.000000</td>
      <td>-3103.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>6.047745e+06</td>
      <td>0.000000</td>
      <td>1.607805e+05</td>
      <td>-15630.000000</td>
      <td>-1467.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>6.456971e+06</td>
      <td>1.000000</td>
      <td>2.250000e+05</td>
      <td>-12514.000000</td>
      <td>-371.000000</td>
      <td>1.0</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>7.999952e+06</td>
      <td>19.000000</td>
      <td>6.750000e+06</td>
      <td>-7489.000000</td>
      <td>365243.000000</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>20.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.columns
```




    Index(['ID', 'CODE_GENDER', 'FLAG_OWN_CAR', 'FLAG_OWN_REALTY', 'CNT_CHILDREN',
           'AMT_INCOME_TOTAL', 'NAME_INCOME_TYPE', 'NAME_EDUCATION_TYPE',
           'NAME_FAMILY_STATUS', 'NAME_HOUSING_TYPE', 'DAYS_BIRTH',
           'DAYS_EMPLOYED', 'FLAG_MOBIL', 'FLAG_WORK_PHONE', 'FLAG_PHONE',
           'FLAG_EMAIL', 'OCCUPATION_TYPE', 'CNT_FAM_MEMBERS'],
          dtype='object')




```python
data.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 90085 entries, 0 to 438553
    Data columns (total 18 columns):
     #   Column               Non-Null Count  Dtype  
    ---  ------               --------------  -----  
     0   ID                   90085 non-null  int64  
     1   CODE_GENDER          90085 non-null  object 
     2   FLAG_OWN_CAR         90085 non-null  object 
     3   FLAG_OWN_REALTY      90085 non-null  object 
     4   CNT_CHILDREN         90085 non-null  int64  
     5   AMT_INCOME_TOTAL     90085 non-null  float64
     6   NAME_INCOME_TYPE     90085 non-null  object 
     7   NAME_EDUCATION_TYPE  90085 non-null  object 
     8   NAME_FAMILY_STATUS   90085 non-null  object 
     9   NAME_HOUSING_TYPE    90085 non-null  object 
     10  DAYS_BIRTH           90085 non-null  int64  
     11  DAYS_EMPLOYED        90085 non-null  int64  
     12  FLAG_MOBIL           90085 non-null  int64  
     13  FLAG_WORK_PHONE      90085 non-null  int64  
     14  FLAG_PHONE           90085 non-null  int64  
     15  FLAG_EMAIL           90085 non-null  int64  
     16  OCCUPATION_TYPE      62608 non-null  object 
     17  CNT_FAM_MEMBERS      90085 non-null  float64
    dtypes: float64(2), int64(8), object(8)
    memory usage: 13.1+ MB



```python

```
