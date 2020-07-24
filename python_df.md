# Basic Usage

### Extract Data
- Get Col A, B, C from df:
```py
df[['A','B','C']]
```
- Get Cols except A but all other Cols from df:
```py
df.loc[:, df.columns != 'A']
```
- Need the whole df only when Col A == e:
```py
df.loc[df['A'] == e]
```
- Need the whole df only when Col A with some values:
```py
df.loc[df['A'].isin(value_list)]
```
- Get the whole row when Col user == '2014':
```py
df.loc[df['user'] == '2014']
```


### Change Value
- Change Column Name:
```py
flattened_df.rename(columns={'coloc_user':'user'}, inplace=True)
```
- Replace all NaN with 0 and non-NaN with:
```py
newdf = df.notnull().astype('int')
```

### Groupby
will return groupby object fter groupby
- flatten the df: 
```py
df.reset_index()
```

### Row Function
row operations
```py
sub_df.apply(lambda row: build_dwell_graph(row), axis = 1)

def build_dwell_graph(row):   # for dwelling data
    start_time = row.start_time
    end_time = row.end_time
    dur_min = row.duration_minutes
    sem_loc = row.sem_loc
    B.add_edge(row.user, sem_loc, start_t=start_time, end_t=end_time, dur=dur_min)
```
assign value:
```py
sub_df['duration_minutes'] = sub_df.apply(lambda row: compute_duration(row), axis = 1)

def compute_duration(row):
    start_time = row.start_time
    end_time = row.end_time
    return ((end_time-start_time)/np.timedelta64(1,'s'))/60
```
