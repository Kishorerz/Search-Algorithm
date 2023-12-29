## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: kishor kumar B.
RegisterNumber: 23009985
'''
def linearSearch(array,n,k):
    for i in range(n):
        if array[i]==k:
            return i
    return -1
    
array = eval(input())
array.sort()
k=eval(input())
print(array)
n=len(array)# k-item to be seared for
result=linearSearch(array,n,k)# use the function for linear search
if result == -1:
    print('Element not found')
else:
    print('Element found at index: ',result)

# get the length of array and store in the variable n

# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result




```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:kishor kumar B.
RegisterNumber: 23009985
'''
def binarySearchIter(array, k, low, high):
    
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
            
        
    
array = eval(input())
array.sort()
print(array)

# sort the array
k = eval(input()) #k-item to be searched
result=binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print('Element not found')
else:
    print('Element found at index: ',result)

# use the binary search function to find the item in the list

# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```

''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: kishor kumar B.
RegisterNumber: 23009985
'''
def binarySearch(array, k, low, high):
    
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    if low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
            return binarySearch(array, k, low, high)
        else:
            high=mid-1
            return binarySearch(array, k, low, high)
    else:
        return -1
            
        
    
array = eval(input())
array.sort()
print(array)

# sort the array
k = eval(input()) #k-item to be searched
n=len(array)
result=binarySearch(array,k,0,n-1)
if result==-1:
    print('Element not found')
else:
    print('Element found at index: ',result)

# use the binary search function to find the item in the list

# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result+

```
## Sample Input and Output
### linear search method
![Screenshot 2023-12-29 204944](https://github.com/Kishorerz/Search-Algorithm/assets/144451216/844140df-d8b2-4a12-bb6c-5eca339e47d2)
###  Binary Search
![Screenshot 2023-12-29 205010](https://github.com/Kishorerz/Search-Algorithm/assets/144451216/59fd0e17-8090-4dea-866a-c9f5032b7374)

### Binary Search (recursive Method)
![Screenshot 2023-12-29 205046](https://github.com/Kishorerz/Search-Algorithm/assets/144451216/9bcf63e0-17e9-4785-bbac-f941ffdc81de)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
