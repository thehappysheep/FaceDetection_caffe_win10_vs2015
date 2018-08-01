# FaceDetection_caffe_win10_vs2015
## 1. Data introduce
the fance detection dataset contains about 42000 pictures ,those picture are divided into two parts,
one part in 0 file incliding face picture，the other file named 1 including non-face picture。
## 2. how to get data
you can download from baidu cloud ,the address is in the data_link.txt
## 3. how to start train your net
Frist of all,make sure you have install caffe and vs2105 correctlly on windows 10,and your computer has NVIDIA GPU
please follows those step
### 3.1
    you should replace the file path with your file path in all *.bat (such convert_data.bat 、comput_mean.bat)
### 3.2
    run the create_val_valliat_trainlist,it will generate vlidation data(you can change vilidation rate) from train data and 
    add label to the picture (0= face,1=nonface) then generate filelist.txt(which include picture name and label,will be used in the 
    progerss of converting limdb),valflielist.txt.
### 3.3
    then you can run convert_data.bat which turn the picture to lmdb
    create_filelist.py with python,then there will be a new txt named  filelist_new.txt
### 3.4
    run the compute_mean.bat to get the image data mean.
### 3.5
    run the train.bat to train the net.
### 3.6
    run the test.bat to test the validation data.
### 3.7
    if you want to continue to train the net , run train_continue.bat(you should frist modify the max-iteration in solver.prototxt)
### 3.8
     run the classcification.bat with the picture you want to test.
## 4.impotrant file
   1.facedata_mean.binaryproto(contains the picture's 3 channel mean value)
   2.solver.prototxt(some hyperparameter)
   3.train_test_net.prototxt(Alenet)
   4.Deploy.prototxt（will be used inclassification,very like train_test_prototxt，just some difference 。）
   5.class.txt 
   6data_link.txt
   




