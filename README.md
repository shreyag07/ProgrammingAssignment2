
### Example: Caching the inverse of a matrix


   makeCacheMatrix <- function(x = matrix()) {
  p <- NULL
  set <- function(y){
  x <<- y
  p <<- NULL
  }
  get <- function()x
  setInverse <- function(inverse) p <<- inverse
  getInverse <- function() p 
  list(set = set, get = get, 
  setInverse = setInverse, 
  getInverse = getInverse)
}

    

    cacheSolve <- function(x, ...) {
## To compute the inverse of the matrix
  p <- x$getInverse()
  if(!is.null(j)){
  message("getting cached data")
  return(p)
  }
  mat <- x$get()
  p <- solve(mat,...)
  x$setInverse(p)
  p
}
