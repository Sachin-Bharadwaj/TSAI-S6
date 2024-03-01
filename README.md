# TSAI-S6
## Part-1

Back propogation on a simple neural network assuming same data point is repeated again and again (just for understanding)
<img width="531" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/6e74e155-d9b9-4ede-b640-5188f954f703"> <br>

The screenshot of the xlx showing the weight update and loss reduction using gradient descent <br>
<img width="1229" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/04383df2-8a04-4593-901a-cc9c51c69d6e">


<br>
The corresponding partial derivatives of the total loss with respect to weights are given by : <br>
<img width="224" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/989048b3-1c30-4648-a2b8-7ad1b9b4d4e7">

<br>
The figures below shows the loss convergence profile for different choice of learning rate parameters <br>
<img width="504" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/47ce702f-a2e6-46c8-bd9d-4a087cc6f87b"> <br>
<img width="494" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/c3eac203-e2ad-4bb6-b8b6-5e0531c9614d"> <br>
<img width="491" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/5c1882a4-f168-481b-9341-779a5169980d"> <br>
<img width="492" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/371361c4-16ce-4cd1-b1ea-d2cff0926da9"> <br>
<img width="491" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/def730ba-e5b6-42aa-97cc-2bab535aaf2e"> <br>
<img width="492" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/52934c4a-643c-45ab-a91b-5f5538899204"> <br>

## Part-2
This assignment is on training a network with less than 20K parameters and having test accuracy > 99.4% on MNIST dataset <br>
General theme in building this type of neural network is to only use Conv layers as far as possible as they take less parameters compared to fully connected network. Another thing is to build a receptive field of ~ 28x28 as MNIST images are 28x28 in size. We do not need more than 28x28 since dataset does not include partial hidden digits. We start with increasing channels to 8 upfront and build up receptive field until 7x7 (enough for MNIST dataset) before using maxpool layer to further increase the receptive field in subsequent conv layers. Finally we use 1x1 conv in the end to output the scores for the classes. <br>
<img width="386" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/51b5ba80-dfa5-45e6-ad80-54a32b94279d"> <br>
The network has less than 20k parameters. <br>
Here is the test accuracy for last few epochs of training: 
<img width="727" alt="image" src="https://github.com/Sachin-Bharadwaj/TSAI-S6/assets/26499326/974641f3-c4e6-4d26-a88d-9d8522ab7424">
















