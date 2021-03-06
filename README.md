# Deep Image Prior


This repositiory containes the PyTroch implementations of Methods proposed for **Image Inpaiting** and **Image Denoising** in the paper [Deep Image Prior](https://arxiv.org/pdf/1711.10925.pdf) by *Dmitry et al.* .


> **Network used** : Custom U-Net(Encoder-Decoder type)\
> **Input for the model** : Latent matrix **_z_**. (np.mggrid is used as per the guidelines in supplementary material)\
> Output of the model is image(recovered) of the same size of the corrupted image\
> Loss is calculated w.r.t. the corrupted image.\
> **_Note_** : While calculating the loss the mask is added to the output image too. so that effective loss is calculated over the Uncorrupted region and model learns the prior for the corrupted region.


## Ablation study for Image Inpainting

| **Corrupted Images** |  **Recovered Images** |            
| ------------- | ------------- |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Inpainting/corrupted_img_kate.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Inpainting/model_output.jpg?raw=true)       |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Inpainting/corrupted_img_bhavesh.png)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Inpainting/bhavesh_recovered.png)     |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Inpainting/vase.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Inpainting/vase_recovered.png?raw=true)       |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Inpainting/corrupted_img_library.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Inpainting/library_recovered.png?raw=true)       |



## Ablation study for Image Denoising

> **_Note_**: The random(gaussian) noise is added in the same image ranging from 10% to 80%. In other words percentage number of pixels were removed from ground truth image in order to make the image noisy.


| **Noisy Images** |  **Denoised Images** |            
| ------------- | ------------- |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Denoising/kate_corrupted_1.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Denoising/recovered_kate_1.png?raw=true)       |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Denoising/kate_corrupted_2.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Denoising/recovered_kate_2.png?raw=true)       |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Denoising/kate_corrupted_3.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Denoising/recovered_kate_3.png?raw=true)       |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Denoising/kate_corrupted_4.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Denoising/recovered_kate_4.png?raw=true)       |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Denoising/kate_corrupted_5.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Denoising/recovered_kate_5.png?raw=true)       |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Denoising/kate_corrupted_6.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Denoising/recovered_kate_6.png?raw=true)       |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Denoising/kate_corrupted_7.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Denoising/recovered_kate_7.png?raw=true)       |
|      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Data/Denoising/kate_corrupted_8.png?raw=true)       |      ![](https://github.com/bhaveshIITB/Deep-image-prior/blob/master/Results/Denoising/recovered_kate_8.png?raw=true)       |





> The code is inspired from the [Official implementation](https://github.com/DmitryUlyanov/deep-image-prior) of *dmitry et al.* 
