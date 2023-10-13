# Multi-Scale CycleGAN Night to Day
- Converting night into day is one of the most interesting applications in generative models, due to the great difficulty in recreating the scene during the day, especially in cases of extreme darkness, and thus the difficulty lies in imagining the scene during the day when the lighting is very weak.
- The proposed system focuses on using a CycleGan architecture that helps in reconstructing the scene in the daytime.
- The structure of the discriminator has been modified so that it can study the correctness of reshaping an object, only a part of which is visible due to extreme darkness and poor lighting. The discriminator was also designed to be able to recognize objects that are close to and far from the camera, so that it studies the correctness of the process of shaping the scene during the day.
- Through the proposed methodology, the discriminator attempts to study the relationship of the pixel with its neighbors, and whether the pixel's current value with its neighbors is correct or not (using kernel = 5 at each output convolutional layer) which helps in evaluating whether the pixel is correctly positioned with respect to its neighbors or not.
- Thus, in this way we try to overcome the problem of great difficulty in reconstructing the scene in extreme darkness.
- During the process of converting night into day, as long as we are studying images that include images of the road, it is possible that some objects may sometimes be close to the camera and others far from the camera, and all we seek is for each object to be recreated in the images as if it were in the daytime. Therefore, the discerner must recognize the entire object, whether it is close to the camera or far from the camera.

## Discriminator Architecture
![download (19)](https://github.com/kaledhoshme123/Multi-Scale-CycleGAN-Night-to-Day/assets/108609519/4971914d-fdf1-462c-92d9-823d5809eff5)

## CycleGAN Architecture:
![__results___15_0 (1)](https://github.com/kaledhoshme123/Multi-Scale-CycleGAN-Night-to-Day/assets/108609519/6aa9383c-790e-4c51-b5bb-c053901a575d)

## Results:
| Examples    |
| :---: |
|  ![__results___27_0](https://github.com/kaledhoshme123/Multi-Scale-CycleGAN-Night-to-Day/assets/108609519/f551c021-05d8-4c4d-96b5-9fb51e830582) | 
|  ![__results___28_0](https://github.com/kaledhoshme123/Multi-Scale-CycleGAN-Night-to-Day/assets/108609519/4e35697a-de44-48d5-a664-c808697e2769) | 
|  ![__results___29_0](https://github.com/kaledhoshme123/Multi-Scale-CycleGAN-Night-to-Day/assets/108609519/91597e6b-00bc-4b6e-9ec2-294a18b104f2) | 

### Note:
I have Trained CycleGan for 35000 Epochs (you train more than and You will get more accurate results )
