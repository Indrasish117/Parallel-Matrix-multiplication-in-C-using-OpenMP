# Parallel-Matrix-multiplication-in-C-using-OpenMP
Speeding up matrix multiplication operation by taking advantage of multicore CPU architectures.

The routine MatMul() computes C = alpha x trans(A) x B + beta x C, where alpha and beta are scalars of type double, A is a pointer to the start of a matrix of size n x m doubles, B is a pointer to the start of a matrix of size n x p doubles, C is a pointer to the start of a matrix of size m x p doubles, and b is the block size. 

The main function creates and populates the matrices A and B with random values and tests the routine with varying matrix sizes and varying number of threads(numt).

At the end there is the linear(non parallel) routine that performs as follows:
![Capture1](https://user-images.githubusercontent.com/49993917/77862447-0e7d0c80-7239-11ea-8bb4-42a7e71ea5c8.PNG)

Compared to that the parallelised code offers significant reductions in computation time: 
![Capture2](https://user-images.githubusercontent.com/49993917/77862451-12a92a00-7239-11ea-9651-f633bd21c997.PNG)

(My laptop is equipped with an i3-6006U, 2 cores with Hyperthreading)
