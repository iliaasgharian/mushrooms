# Mushroom Dataset Gini Index Calculator



###### This Python script calculates the Gini for each binary column in the Mushroom dataset relative to the class label.



This script reads the mushroom.csv dataset, converts all binary categorical features to binary numeric values ​​(0 and 1), and calculates the Gini for each feature.



### Requirements

- Python 3.x

- NumPy library

- You can install NumPy using pip if it’s not installed: 

```python 

pip install numpy

```

### How to use

- Place your mushrooms.csv file in the same directory as the script and run the code



This script assumes that the first column of mushroom.csv contains Y and the other columns contain X.



### How it works

- Reading the Dataset

```python 

data=np.genfromtxt("mushrooms.csv",delimiter=",",dtype=None)[1:]

```

Reads CSV file using NumPy and skips header row using [1:].



### Convert binary columns to 0 and 1

```python 

d=data.T

for i in d:

    m=set(i)

    if len(m)==2:

        s1=(list(m)[0])

        s2=(list(m)[1])

        i[i==s1]=1

        i[i==s2]=0 

s=d.T

```

- Converts all binary categorical features into 0 and 1. 

### Gini Function

```python 

def gini(x,y):

    .

    .

    .

    return weight

```

- Takes column x and column y.

- Converts data to a NumPy array based on x and y.

- Calculates the Gini.

- And finally it returns the weighted average value.

### split Function
- This function sends each binary column to the Gini function, takes the Gini, and adds it to the list. Finally, it prints the lowest Gini value.
- Check for Binary Features :
```python 
if len(set(m[i])) == 2:
```
- Compute Gini Impurity
```python 
gini(m[i], y)
```

- Sends the binary columns along with column Y to the Gini function( `def gini(x,y)` ) and prints the weighted average value and column index.