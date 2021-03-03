# mnist_database_digit_recognition
mnist database digit recognition

1)
mnist training program in c++
     
   compile:
   
      g++ training_mnist.cpp
    
   run:
   
      ./a.out  

   input:     
   
      hardcoded file name for 60,000 mnist training images
      hardcoded file name for 60,000 mnist training labels
      download training data from http://yann.lecun.com/exdb/mnist/
        train-images-idx3-ubyte.gz
        train-labels-idx1-ubyte.gz
        
        unzip and rename accordingly for hardcoded filename values
   
   output:
   
      write updated model weights to file
      
   note:
   
      while this program is updating the weights you can execute testing_mnist.cpp
      to check the accuracy using the mnist test data. you can also just wait for the 
      process to complete and check the final output. 

      refer to testing_mnist.cpp for further details.
      
      
2)
mnist testing program in c++ by @menascii
     
   compile:
   
      g++ testing_mnist.cpp
    
   run:
   
      ./a.out  

   input: 
   
   	  hardcoded file name for neural network model weights
		generated by executing training_mnist.cpp

      hardcoded file name for 10,000 mnist testing images
      hardcoded file name for 10,000 mnist testing labels
      download training data from http://yann.lecun.com/exdb/mnist/
        t10k-images-idx3-ubyte.gz
        t10k-labels-idx1-ubyte.gz
        
        unzip and rename accordingly for hardcoded filename values
   
   output:
   
     print wrong digit predictions
     print total correct results percentage and cost

	!!!!!! wrong prediction !!!!!!
	####### testing digit #######
	mnist testing image #: 2810
	............................
	............................
	............................
	............................
	............................
	..........@@@@@@@@@.........
	..........@@@@@@@@@@........
	.........@@@@@@@@@@@........
	.........@@@@@@@@@@.........
	.........@@@@@@@@@@.........
	.........@@@@@@@@@@@........
	........@@@@@@@@@@@@@.......
	........@@@@@@@@@@@@@.......
	........@@@......@@@@.......
	.................@@@@@......
	..................@@@@......
	..................@@@@......
	........@@........@@@@......
	.......@@@@......@@@@@......
	.......@@@@@...@@@@@@.......
	.......@@@@@@@@@@@@@@.......
	.......@@@@@@@@@@@@@........
	........@@@@@@@@@@@.........
	.........@@@@@@@@...........
	.........@@@@@@@............
	............................
	............................
	............................

	expected value:  5
	predicted value: 3
	cost error:      0.478307

	#############################
	correct predictions: 6532 / 10000 = 65.32%
      
   note:
   
      this program can be executed while training_mnist.cpp is
      executing. it will use the current weights written to the shared
      model weights file. need to optimize but still pretty fast.

