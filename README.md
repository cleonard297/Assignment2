# Assignment2
 #Part1
 makeCacheMatrix<- function(x= matrix()) {
+   inv <- NULL
+   set <- function(y){
+       x<<- y
+       inv<- NULL
+ }
+ get<- function() x
+ setInverse<- function(solveMatrix) inv<<- solveMatrix
+ getInverse<- function() inv
+ list(set=set, get= get, setInverse= setInverse, getInverse= getInverse)
+ }

#The above function creates a matrix that caches its inverse 


