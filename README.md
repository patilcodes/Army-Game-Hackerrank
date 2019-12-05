
#!/bin/python3

import os
import sys

#
# Complete the gameWithCells function below.
#
def gameWithCells(n, m):
    if n%2!=0 and m%2==0:
        a=(n+1)*m
        return a//4
    elif n%2==0 and m%2!=0:
        a=n*(m+1)
        return a//4
    elif n%2!=0 and m%2!=0:
        a=(n+1)*(m+1)
        return a//4
    else:
        return (m*n)//4
    


if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    nm = input().split()

    n = int(nm[0])

    m = int(nm[1])

    result = gameWithCells(n, m)

    fptr.write(str(result) + '\n')

    fptr.close()
