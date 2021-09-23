# pytorch_EuroSat_vgg19



This repo contains a pytorch implementation of a VGG19 trained on the Sentinel-2 classification dataset [EuroSat]( https://github.com/phelber/EuroSAT)

Performing classification on this dataset is in now way shape or form a hard task. This was just done to produce a set of VGG19 weights, susceptible for a **four channel input** and kernels that are trained to **detect features in satellite imagery**. 

Those weights can be used to serve as a ***perceptual loss*** for other remote sensing machine learning tasks, or a p retrained network for fine tuning if you don't have a GPU.



### Training Details

The loss on the training and validation set over 50 epochs. Bets val-score was saved to the checkpoint folder. 

![training](/home/jp/Documents/code/vgg19_RS_perceptual_loss/figures/training.png)

### Confusion Matrix of the pretrained Network

Trained on 15k sampels, validated on 5k sampels. The model checkpoint can be found under /checkpoint/model_epoch_41_step_39018.pth



![cm_epoch_41_step_39018](/home/jp/Documents/code/vgg19_RS_perceptual_loss/checkpoint/cm_epoch_41_step_39018.png)
