# Fourier-Transform-CUDA.Thread.MPI
Implemented 2D Fast Fourier Transform (FFT) and Discrete Fourier Transform (DFT) using CUDA, Thread and MPI.

To excecute the program, make the project in your build fold, then you can do the example commands:
    
    $./Cuda forward inputfile.txt outputfile.csv
    
    $./Thread forward inputfile.txt outputfile.csv
    
    $mpirun -np 8 MPI forward inputfile.txt outputfile.csv
    
*forward means normal FT, backward means Inverse FT.
