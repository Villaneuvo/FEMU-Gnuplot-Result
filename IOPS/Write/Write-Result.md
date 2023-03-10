# read Plotting Result 

In this Benchmarking test i've been running FIO with write Operation on Cloudlabs with FEMU. Here's about the Fio configuration details below :
```
[global]
ioengine = psync
runtime = 60 
rw = write
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
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453584/Research/Write/write-1_eozadz.jpg" alt="write-1" width="600"/>
<br><br>


## QD=4 (numjobs=4, threads=4)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453584/Research/Write/write-4_ahdovo.jpg" alt="write-4" width="600"/>
<br><br>


## QD=16 (numjobs=16, threads=16)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453584/Research/Write/write-16_ldm3tx.jpg" alt="write-16" width="600"/>
<br><br>

## QD=32 (numjobs=32, threads=32)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453584/Research/Write/write-32_acqiff.jpg" alt="write-32" width="600"/>
<br><br>

## QD=64 (numjobs=64, threads=64)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453584/Research/Write/write-64_yipd7y.jpg" alt="write-64" width="600"/>
<br><br>

## QD=128 (numjobs=128, threads=128)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453584/Research/Write/write-128_kmkkbu.jpg" alt="write-128" width="600"/>
<br><br>

## QD=256 (numjobs=256, threads=256)


### Plotting Result
<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453584/Research/Write/write-256_lluw1p.jpg" alt="write-256" width="600"/>
<br><br>

# Summary 
From this configuration we can summary that if we increase both of varible it will give consistentcy performance but at the early it always get low performance. Meanwhile i've been create data that compare KIOPS performance in every configuration.

<img src="https://res.cloudinary.com/dkcur9nvf/image/upload/v1678453584/Research/Write/write-data_vhwhzs.jpg" alt="write-data" width="600"/>
<br>

## Explanation :
0 = FIO Configuration with numjobs 128 and threads variable 128 <br>
1 = FIO Configuration with numjobs 16 and threads variable 16 <br>
2 = FIO Configuration with numjobs 1 and threads variable 1 <br>
3 = FIO Configuration with numjobs 256 and threads variable 256 <br>
4 = FIO Configuration with numjobs 32 and threads variable 32 <br>
5 = FIO Configuration with numjobs 4 and threads variable 4 <br>
6 = FIO Configuration with numjobs 64 and threads variable 64 <br>