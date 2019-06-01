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

#Part 2
cacheSolve <- function(x, ...) {
   # Returns a matrix that is the inverse of 'x'
  inv <- x$getInverse()
  if(!is.null(inv)){
    message("getting cached data")
    return(inv)
   }
  data <- x$get()
  inv <- solve(data)
  x$setInverse(inv)
  inv      
}
