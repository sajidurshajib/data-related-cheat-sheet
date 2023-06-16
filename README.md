## Pandas cheat-sheet

Import data set.
   
``` df = pd.read_csv('./your_data.csv') ```

Output dataset

``` df.to_csv('Output.csv') ```

Show top and bottom 5 rows.

``` df.head() ```

Show first 10 rows.

``` df.head(10) ```

Create dataframe.

```
tempdict = {'col1': [1,2,3], 'col2': [4,5,6],'col3': [7,8,9]}
data_frame = pd.DataFrame.from_dict(tempdict)
data_frame.head() 
```

Show bottom 5 rows (You can put rows number like head(10))

``` df.tail() ```

Show column names and dtype.

``` df.columns ```

Show dtypes.

``` df.dtypes ```

Data summary.

``` df.describe() ```

Summary for non-float and integer values.

``` df.describe(include='object') ```

view single column.

``` df.['Your column name'] ```

Multi column view.

``` df.[['col1', 'col2']] ```

Unique value from a column.

``` df.colName.unique() ```

Filtering column value.

``` df[df['colName']=='value'] ```

iloc - Index location 

``` df.iloc[5] ```

iloc[row, column] 

``` df.iloc[5,0] ```
or 
``` df.iloc[5,-1] ```

iloc range.

``` df.iloc[3:10] ```


loc - search index (loc can go with multiple columns)

``` df.loc[1] ```


Get null value.

``` df.isnull() ```

Drop a column.

``` ch.drop('Category', axis=1) ```

Apply condition.

``` df['binary'] = df['Category'].apply(lambda x: 1 if x=='ham' else 0) ```



## Numpy cheat-sheet

Some useful methods - 
``` np.random.rand(), np.zeros(), np.full(), np.ones() ```

Create numpy array 

``` np.array([[2,3],[4,5]]) ```

Some read related attribute 

``` 
data.shape
data.size
data.dtype
```

Data slicing

``` data[0:2] ```

Array data reverse

``` data[-1] ```

Basic math

```
np.add(list1, list2)
np.subtract(list1, list2)
np.divide(list1, list2)
np.multiply(list1, list2)
np.dot(list1, list2)
```

Stat Functions

```
np.sqrt(25)
np.abs(-2)
np.power(2,3)
np.log(25)
np.exp([2,3]) 
np.min(list)
np.max(list)
```

Some other functions

```
np.reshape((2,2,2))
np.append(zeros, [3,4])
np.insert(zeros, 2, 1)
```

Delete

``` np.delete(data, o, axis=1) ```

Save

``` np.save('new array', data)```

Load

``` test = np.load('new array.npy')```
