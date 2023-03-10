# RandRead Plotting Result 

In this Benchmarking test i've been running FIO with RandRead Operation on Cloudlabs with FEMU. Here's about the Fio configuration details below :
```
[global]
ioengine = psync
runtime = 60 
rw = randread
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
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453377/Research/RandRead/rand-read-1_wy1zdq.jpg" alt="randread-1" width="600"/>
<br><br>


## QD=4 (numjobs=4, threads=4)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453377/Research/RandRead/rand-read-4_zhb35h.jpg" alt="randread-4" width="600"/>
<br><br>


## QD=16 (numjobs=16, threads=16)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453377/Research/RandRead/rand-read-16_xogyaj.jpg" alt="randread-16" width="600"/>
<br><br>

## QD=32 (numjobs=32, threads=32)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453377/Research/RandRead/rand-read-32_hsr0vz.jpg" alt="randread-32" width="600"/>
<br><br>

## QD=64 (numjobs=64, threads=64)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453377/Research/RandRead/rand-read-64_yvj4h5.jpg" alt="randread-64" width="600"/>
<br><br>

## QD=128 (numjobs=128, threads=128)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453378/Research/RandRead/rand-read-128_nntwux.jpg" alt="randread-128" width="600"/>
<br><br>

## QD=256 (numjobs=256, threads=256)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453378/Research/RandRead/rand-read-256_zdkxyi.jpg" alt="randread-256" width="600"/>
<br><br>

# Summary 
From what i've been observed KIOPS will increase significantly when numjobs and threads on the right number, but if both of variable get higher number it will get consistent performance of KIOPS but sometimes it will drop significantly to. Meanwhile i've been create data that compare KIOPS performance in every configuration. 

<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453377/Research/RandRead/rand-read-data_sgdgaz.jpg" alt="randread-data" width="600"/>
<br>

## Explanation :
0 = FIO Configuration with numjobs 128 and threads variable 128 <br>
1 = FIO Configuration with numjobs 1 and threads variable 1 <br>
2 = FIO Configuration with numjobs 256 and threads variable 256 <br>
3 = FIO Configuration with numjobs 32 and threads variable 32 <br>
4 = FIO Configuration with numjobs 4 and threads variable 4 <br>
5 = FIO Configuration with numjobs 16 and threads variable 16 <br>
6 = FIO Configuration with numjobs 64 and threads variable 64 <br>