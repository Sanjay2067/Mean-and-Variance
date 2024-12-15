#  Mean and variance of a discrete  distribution


# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![Screenshot 2024-12-15 111240](https://github.com/user-attachments/assets/c53b85ce-9fbc-446f-a830-9d69c1453bd1)


The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![Screenshot 2024-12-15 111252](https://github.com/user-attachments/assets/536939ca-7b71-4865-8448-e91768c72ffa)



# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
  ![Screenshot 2024-12-15 111149](https://github.com/user-attachments/assets/52e5da5f-f307-47fc-888d-d74777d7a5e3)


4. Find  
   
     ![Screenshot 2024-12-15 111159](https://github.com/user-attachments/assets/1924b4a2-cb8d-42e6-8a71-0c043f020ae1)


5.  Calculate variance using 
  
      ![Screenshot 2024-12-15 111206](https://github.com/user-attachments/assets/86b50a27-63e3-48d0-9ec6-09fd7fac83df)



# Experiment :

![Screenshot 2024-12-15 111220](https://github.com/user-attachments/assets/e198464f-1b8c-4a84-ad7a-057ba7eb4002)


# Program :
Developed by : MAGENDRA SANJAY S
Register number : 24900652

import numpy as np
L=[int(i) for i in input().split()]
N=len(L); M=max(L) 
x=list();f=list()
for i in range (M+1):
    c = 0
    for j in range(N):
        if L[j]==i:
            c=c+1
    f.append(c)
    x.append(i)
sf=np.sum(f)
p=list()
for i in range(M+1):
    p.append(f[i]/sf) 
mean=np.inner(x,p)
EX2=np.inner(np.square(x),p)
var=EX2-mean**2 
SD=np.sqrt(var)
print("The Mean arrival rate is %.3f "%mean)
print("The Variance of arrival from feeder is %.3f "%var) 
print("The Standard deviation of arrival from feeder is %.3F "%SD)

# Output : 
![Screenshot 2024-12-15 111817](https://github.com/user-attachments/assets/e5cccea4-b032-4307-acc2-c1795bd4e49d)

# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.

