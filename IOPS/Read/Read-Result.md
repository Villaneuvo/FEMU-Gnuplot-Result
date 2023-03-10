# read Plotting Result 

In this Benchmarking test i've been running FIO with Read Operation on Cloudlabs with FEMU. Here's about the Fio configuration details below :
```
[global]
ioengine = psync
runtime = 60 
rw = read
numjobs = n (1,4,16,32,64,128,256)
bs = 4k
direct = 1 
size = 1G
threads = n (1,4,16,32,64,128,256)
randrepeat = 0 
iodepth = 16   
thread
norandommap = 1
```
# Result

## Explanation :
x-axis = Shows running time observed in 60 second<br>
y-axis = Shows the KIOPS data changes every second<br>
<br>


## QD=1 (numjobs=1, threads=1)


### Plotting Result 
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453486/Research/Read/read-1_p8d3gc.jpg" alt="read-1" width="600"/>
<br><br>


## QD=4 (numjobs=4, threads=4)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453486/Research/Read/read-4_hukqtd.jpg" alt="read-4" width="600"/>
<br><br>


## QD=16 (numjobs=16, threads=16)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453486/Research/Read/read-16_onzxjj.jpg" alt="read-16" width="600"/>
<br><br>

## QD=32 (numjobs=32, threads=32)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453486/Research/Read/read-32_lukpff.jpg" alt="read-32" width="600"/>
<br><br>

## QD=64 (numjobs=64, threads=64)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453486/Research/Read/read-64_wcd05k.jpg" alt="read-64" width="600"/>
<br><br>

## QD=128 (numjobs=128, threads=128)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453487/Research/Read/read-128_moormv.jpg" alt="read-128" width="600"/>
<br><br>

## QD=256 (numjobs=256, threads=256)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453487/Research/Read/read-256_i6wn4a.jpg" alt="read-256" width="600"/>
<br><br>

# Summary 
From here we can see that the performance seems stable but in the configuration it shows that the performance can't go higher around 50 - 60, but on some configuration (actually on numjobs 4 and threads 4) it shows performance unstable. Meanwhile i've been create data that compare KIOPS performance in every configuration.

<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453486/Research/Read/read-data_jwvoic.jpg" alt="read-datba" width="600"/>
<br>

## Explanation :
0 = FIO Configuration with numjobs 128 and threads variable 128 <br>
1 = FIO Configuration with numjobs 16 and threads variable 16 <br>
2 = FIO Configuration with numjobs 1 and threads variable 1 <br>
3 = FIO Configuration with numjobs 256 and threads variable 256 <br>
4 = FIO Configuration with numjobs 32 and threads variable 32 <br>
5 = FIO Configuration with numjobs 4 and threads variable 4 <br>
6 = FIO Configuration with numjobs 64 and threads variable 64 <br>