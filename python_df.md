# Basic Usage

### Extract Data
- Get Col A, B, C from df:
```
df[['A','B','C']]
```
- Get Cols except A but all other Cols from df:
```
df.loc[:, df.columns != 'A']
```
- Need the whole df only when Col A == e:
```
df.loc[df['A'] == e]
```
- Need the whole df only when Col A with some values:
```
df.loc[df['A'].isin(value_list)]
```
- Get the whole row when Col user == '2014':
```
df.loc[df['user'] == '2014']
```


### Change Value
- Replace all NaN with 0 and non-NaN with:
```
newdf = df.notnull().astype('int')
```

### Groupby
will return groupby object fter groupby
- flatten the df: 
```
df.reset_index()
```
