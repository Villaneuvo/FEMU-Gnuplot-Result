# read Plotting Result 

In this Benchmarking test i've been running FIO with read Operation on Cloudlabs with FEMU. Here's about the Fio configuration details below :
```
[global]
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
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453649/Research/BW-OP/Read/Read-128/read-128-1_oxjznk.jpg" alt="read-bs-128-1" width="600"/>
<br><br>

## QD=16 (numjobs=16, threads=16)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453649/Research/BW-OP/Read/Read-128/read-128-16_o4bl9z.jpg" alt="read-bs-128-16" width="600"/>
<br><br>

## QD=32 (numjobs=32, threads=32)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453649/Research/BW-OP/Read/Read-128/read-128-32_bwbptc.jpg" alt="read-bs-128-32" width="600"/>
<br><br>

# BaseSize = 256k

## QD=1 (numjobs=1, threads=1)


### Plotting Result 
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453698/Research/BW-OP/Read/Read-256/read-256-1_qh5olq.jpg" alt="read-bs-256-1" width="600"/>
<br><br>

## QD=16 (numjobs=16, threads=16)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453698/Research/BW-OP/Read/Read-256/read-256-16_dzzd8p.jpg" alt="read-bs-256-16" width="600"/>
<br><br>

## QD=32 (numjobs=32, threads=32)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453698/Research/BW-OP/Read/Read-256/read-256-32_whlada.jpg" alt="read-bs-256-32" width="600"/>
<br><br>

# BaseSize = 512k

## QD=1 (numjobs=1, threads=1)


### Plotting Result 
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453682/Research/BW-OP/Read/Read-512/read-512-1_gr7n7q.jpg" alt="read-bs-512-1" width="600"/>
<br><br>

## QD=16 (numjobs=16, threads=16)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453682/Research/BW-OP/Read/Read-512/read-512-16_dq7lug.jpg" alt="read-bs-512-16" width="600"/>
<br><br>

## QD=32 (numjobs=32, threads=32)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453682/Research/BW-OP/Read/Read-512/read-512-32_nln399.jpg" alt="read-bs-512-32" width="600"/>
<br><br>

# Summary 
As we can see here numjobs and threads really affecting the benchmark performance, the higher number of both of variable, the greatest performance we can get, but it needs to be balance with the base size or it can give us bad performance.