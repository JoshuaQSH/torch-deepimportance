# TensorFlow version lenet5 - deepimportance
----------------------------------------------------------------
Layer (type)                 Output Shape              Param #   
=================================================================
input_2 (InputLayer)         (None, 28, 28, 1)         0         
_________________________________________________________________
block1_conv1 (Conv2D)        (None, 24, 24, 6)         156       
_________________________________________________________________
block1_pool1 (MaxPooling2D)  (None, 12, 12, 6)         0         
_________________________________________________________________
block2_conv1 (Conv2D)        (None, 8, 8, 16)          2416      
_________________________________________________________________
block2_pool1 (MaxPooling2D)  (None, 4, 4, 16)          0         
_________________________________________________________________
flatten (Flatten)            (None, 256)               0         
_________________________________________________________________
fc1 (Dense)                  (None, 120)               30840     
_________________________________________________________________
fc2 (Dense)                  (None, 84)                10164     
_________________________________________________________________
before_softmax (Dense)       (None, 10)                850       
_________________________________________________________________
predictions (Activation)     (None, 10)                0         
=================================================================
Total params: 44,426
Trainable params: 44,426
Non-trainable params: 0
_________________________________________________________________


# PyTorch version lenet5

----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1            [-1, 6, 24, 24]             156
              ReLU-2            [-1, 6, 24, 24]               0
         MaxPool2d-3            [-1, 6, 12, 12]               0
            Conv2d-4             [-1, 16, 8, 8]           2,416
              ReLU-5             [-1, 16, 8, 8]               0
         MaxPool2d-6             [-1, 16, 4, 4]               0
           Flatten-7                  [-1, 256]               0
            Linear-8                  [-1, 120]          30,840
              ReLU-9                  [-1, 120]               0
           Linear-10                   [-1, 84]          10,164
             ReLU-11                   [-1, 84]               0
           Linear-12                   [-1, 10]             850
================================================================
Total params: 44,426
Trainable params: 44,426
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.08
Params size (MB): 0.17
Estimated Total Size (MB): 0.25
----------------------------------------------------------------