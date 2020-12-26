# ![LOGO](images/LOGO.png)



### 					                    									Extensive Vision AI Program

##### Assignment 6A

- Run this [network](https://colab.research.google.com/drive/1STOg33u7haqSptyjUL40FZIxNW4XdBQK)  and train for 100 epochs to obtain base accuracy
- Fix the above network:
  - Remove dense
  - Add layers required to reach RF
  - Fix kernel scaleup and down (1x1)
  - Ensure all dropouts are properly placed
  - Obtain accuracy more than the base accuracy in less than 100 epochs.Hint, Use "border_mode='same',"

**Assignment 6B**

- Rewrite the [network](https://colab.research.google.com/drive/1STOg33u7haqSptyjUL40FZIxNW4XdBQK) using the convolutions in the order given below:

  - Normal Convolution
  - Spatially Separable Convolution  (Conv2d(x, (3,1)) followed by Conv2D(x,(3,1))
  - Depthwise Separable Convolution
  - Grouped Convolution (use 3x3, 5x5 only)
  - Grouped Convolution (use 3x3 only, one with dilation = 1, and another with dilation = 2) 
  - Train this new model for 50 epochs. 

  