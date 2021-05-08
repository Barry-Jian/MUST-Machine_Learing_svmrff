
# Machine_Learing_svmrff
  For the Final report of Machine Learning, the main idea is to use Random Fourier features+ Liblinear to approximate Libsvm and SVMLight using Gaussian kernels.   
  First, pre-process the three data sets: remove the 'inf' 'nan' '？' in them; for the Adult data set, we should perform one-hot encoding.After some simple visualization, you can 
observe the characteristics of the data.   
  I think the key to programming is the definition of three functions: 
1. Change the ordinary data format into a format that Libsvm can read 
2. Change the ordinary data format into a format that SVMLight can read 
3. Perform RFF transformation on the features in the original data set   
  For SVMLight,I want to use svmlight package to build svm model and solve the problem. Unfortunately, it hard to install the package and i used the code shown below: 

!git clone https://github.com/mblondel/svmlight-loader 
%cd svmlight-loader 
!python setup.py build &amp;&amp; python setup.py install import svmlight 

  Actually,you can also find other website(github) or official website to install this package. For some reasons, I failed. In my opinion, it has big relationship with 
Visual C++ and I donot have enough time to fix it. SO,I downloaded the exe file and used powershell to establish svmlight model.
  In the code below, you can obtain the function "generate_data_file" !  In the case of RFF mapping to 500 dimensions, Liblinear's approximation effect is not bad, and the time 
is considerable.
  The key to the problem is how to choose the dimension of the mapping to balance the result and the time complexity of the algorithm. Of course, you can also try to scale 
the data in different forms. You can perform grid search to adjust the parameters and then balance the residuals and variances (the solution to the inverse problem can be 
introduced)  Because the code still needs to be modified, I temporarily uploaded the html file, and the total file is visible after the report is completed！！   
Welcome to discuss！
