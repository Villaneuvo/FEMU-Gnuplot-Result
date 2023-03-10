# read Plotting Result 

In this Benchmarking test i've been running FIO with write Operation on Cloudlabs with FEMU. Here's about the Fio configuration details below :
```
[global]
ioengine = psync
runtime = 60 
rw = write
ioengine = psync
runtime = 60 
rw = read
numjobs = n(1,16,32)
threads = n(1,16,32)
time_based = 1
group_reporting 
per_job_logs=0 
direct=1 
thread
size=1G 
```
# Result

## Explanation :
x-axis = Shows running time observed in 60 second<br>
y-axis = Shows the KIOPS data changes every second<br>
<br>

# BaseSize = 128k

## QD=1 (numjobs=1, threads=1)


### Plotting Result 
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453735/Research/BW-OP/Write/Write-128/write-128-1_swcby3.jpg" alt="write-bs-128-1" width="600"/>
<br><br>

## QD=16 (numjobs=16, threads=16)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453735/Research/BW-OP/Write/Write-128/write-128-16_hilfbs.jpg" alt="write-bs-128-16" width="600"/>
<br><br>

## QD=32 (numjobs=32, threads=32)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453735/Research/BW-OP/Write/Write-128/write-128-32_vs0igp.jpg" alt="write-bs-128-32" width="600"/>
<br><br>

# BaseSize = 256k

## QD=1 (numjobs=1, threads=1)


### Plotting Result 
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453746/Research/BW-OP/Write/Write-256/write-256-1_cp81i4.jpg" alt="write-bs-256-1" width="600"/>
<br><br>

## QD=16 (numjobs=16, threads=16)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453746/Research/BW-OP/Write/Write-256/write-256-16_ir5q9k.jpg" alt="write-bs-256-16" width="600"/>
<br><br>

## QD=32 (numjobs=32, threads=32)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453746/Research/BW-OP/Write/Write-256/write-256-32_axz4jb.jpg" alt="write-bs-256-32" width="600"/>
<br><br>

# BaseSize = 512k

## QD=1 (numjobs=1, threads=1)


### Plotting Result 
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453768/Research/BW-OP/Write/Write-512/write-512-1_j65cni.jpg" alt="write-bs-512-1" width="600"/>
<br><br>

## QD=16 (numjobs=16, threads=16)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453768/Research/BW-OP/Write/Write-512/write-512-16_es2f90.jpg" alt="write-bs-512-16" width="600"/>
<br><br>

## QD=32 (numjobs=32, threads=32)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453768/Research/BW-OP/Write/Write-512/write-512-32_hqns85.jpg" alt="write-bs-512-32" width="600"/>
<br><br>

# Summary 
From the result above we can conclude that the higher threads and numjobs, the greatest performance we can get, but its need to be balanced with the basesize. We can also noticed that the performance is actually good but sometimes it give us a drop perfomance.