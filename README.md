## EXPERIMENT 2 Numerical Python (NumPy)

## NORMALIZATION PROBLEM
- Create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy

## CODING

import numpy as np

#Create a random 5x5 ndarray and store it in variable x

x = np.random.random((5,5))

#Normalize x using the given formula

z = ( x - np.mean(x) / np.std(x))

#Print the normalized x

print (z)

#Save the normalized ndarray

np.save('X_normalized', z)


## DIVISIBLE BY 3 PROBLEM
- Create a 10 x 10 ndarray, which are the squares of the first 100 positive integers. From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

## CODING
import numpy as np

#Create a 10x10 ndarray with positive integers of 1-100

a = np.arange(1,101).reshape(10,10)

#Square the elements

b = (np.array(a)**2)

#Store all the elements divisible by 3 in variable c

c = (b % 3 == 0)

#In variable d, return the elements that is divisible by 3 from variable b

d = b[c]


#Print a header for the squared elements

print("Squared elements")

#Print the squared values

print(b)

#Add space for aesthetic purposes

print()

#Print a header for the elements divisible by 3

print("Elements divisible by 3: ")

#Print the values divisible by 3

print(d)


#Save the result

np.save("div_by_3.npy", d)

