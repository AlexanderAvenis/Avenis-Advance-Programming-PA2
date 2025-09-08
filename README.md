# Avenis-Advance-Programming-PA2

# NORMALIZATION PROBLEM
**Instruction:** 
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation.

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and .std() calls

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy

**Code:**
```python
# generate array and takes mean and standard deviation
X = np.random.random((5,5))   
mean = X.mean()               
sd = X.std()                  

# Normalization
normalized = (X - mean) / sd  

# print outputs
print(f''' 
ndarray:
{X}

mean: {mean}

standard deviation: {sd}

normalized:
{normalized}
''')

# Saves the normalized array to a file
np.save('X_normalized.npy', normalized)
```
1. Randomly generate a dataset with **X = np.random.random((5,5))**.

2. Find its mean with **X.mean()** and standard deviation with **sd = X.std()**.

3. Apply the normalization using the formula; **normalized = (X - mean) / sd**.

4. Save the result to a .npy file with **np.save('X_normalized.npy', normalized)**.


# DIVISIBLE BY 3 PROBLEM: 
**Instruction:** 
Create the following 10 x 10 ndarray.
which are the squares of the first 100 positive integers. From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

**Code:**
```python
# create 10x10 array
array = np.arange(1,101,1)**2
array = array.reshape(10,10)

# determine elements divisible by 3
div_by_3 = []
for row in array:
    for number in row:
        if number % 3 == 0:
            div_by_3.append(int(number))
        else:
            pass

# print outputs
print(f'''

array:
{array}

elements divisible by 3:
{div_by_3}
''')

# save outputs
np.save('div_by_3.npy', div_by_3)
```
1. Generate squares of numbers from 1 to 100 with **array = np.arange(1,101,1)**2**.

2. Reshape this array to fit the 10x10 format 2D array with **array = array.reshape(10,10)**.

3. Use a nested loop that goes through a each element of each row in the array to check element and check divisibility by 3 by using the modulus operation.

4. Save the result to a .npy file with **np.save('div_by_3.npy', div_by_3)**




