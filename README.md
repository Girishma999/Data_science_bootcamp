# sat2map
An implementation of pix2pix using PyTorch.
Original paper: [Image-to-Image Translation with Conditional Adversarial Networks](https://arxiv.org/pdf/1611.07004.pdf).

## Team Details
1. Ms. Pathipati Girishma Chowdary **(200100110)**
2. Ms. Patil Utkarsha Jitendra **(200100112)**
3. Pranav Vivek Yatnalkar **(200020096)**
4. Khandekar Ved Mangesh **(20d170019)**

## Training the model
**Note: ** *We have provided `generator100.pth` which is the generator trained for 100 epochs on 1096 images. Rename it to `generator.pth` and follow the steps below to test the pre-trained model.*
We assume that you have successfully installed PyTorch with CUDA support.
The model has been trained on Windows 11 with Python 3.10.8 using NVIDIA CUDA.
Note that support for Apple silicon is still limited and using mps backend might not work.
We trained it on the 1096 images for 200 epochs. For the learning rate and other parameters, please refer to `train.py`.

Follow the following steps to train the generator and test it using `test.py`
1. Create a directory with the name of `ckpnt`. This will be used to store the checkpoints during training.
2. Create a directory with the name of `data`. This will store the training and testing data.
3. Download the datset from [here](https://www.kaggle.com/datasets/vikramtiwari/pix2pix-dataset).
4. Extract the zip file and navigate inside `archive/maps` and copy the `maps` folder inside the `data` folder created in step (2).
5. Run `python train.py` on the command line

The above steps will generate `generator.pth`.
Now run `python test.py` and enter the number of the image in `data/maps/val` to test the model.

## References
1. https://www.tensorflow.org/tutorials/generative/pix2pix
2. https://github.com/togheppi/pix2pix
3. https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix
4. https://towardsdatascience.com/unet-line-by-line-explanation-9b191c76baf5