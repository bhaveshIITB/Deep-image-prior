# Deep Image Prior


This repositiory containes the implementation Method proposed for **Image Inpaiting** in paper [Deep Image Prior](https://arxiv.org/pdf/1711.10925.pdf) by *Dmitry et al.* .


> **Network used** : Custom U-Net(Encoder-Decoder type)\
> **Input for the model** : Latent matrix **_z_**. (np.mggrid is used as per the guidelines in supplementary material)\
> Output of the model is image(recovered) of the same size of the corrupted image\
> Loss is calculated w.r.t. the corrupted image.\
> **_Note_** : While calculating the loss the mask is added to the output image too. so that effective loss is calculated over the Uncorrupted region and model learns the prior for the corrupted region.


## Corrupted Image :                                     Recovered Image:
  ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/corrupted_img.png)                                          
  ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/model_output.jpg)

> The code is inspired from the [Official implementation](https://github.com/DmitryUlyanov/deep-image-prior) of *dmitry et al.* 


![alt-text-1](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/corrupted_img.png "title-1") </t></t>![alt-text-2](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/model_output.jpg "title-2")


| Corrupted Image  | Recovered Image |
| ------------- | ------------- |
| ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/corrupted_img.png)  | ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/model_output.jpg)  |
| Content Cell  | Content Cell  |
