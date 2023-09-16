# Cat-Image-Classifier-Models

Hello! This is my first Neural Network implemented from scratch without using any ML frameworks.

### Dataset at a Glance:
Number of training examples: 209  
Number of testing examples: 50  
Each image is of size: (64, 64, 3)   
train_x_orig shape: (209, 64, 64, 3)   
train_y shape: (1, 209)   
test_x_orig shape: (50, 64, 64, 3)   
test_y shape: (1, 50)   

## Model Architecture
### 2-layer Neural Network
- The input is a (64,64,3) image which is flattened to a vector of size $(12288,1)$. 
- The corresponding vector: $[x_0,x_1,...,x_{12287}]^T$ is then multiplied by the weight matrix $W^{[1]}$ of size $(n^{[1]}, 12288)$.
- Then, add a bias term and take its relu to get the following vector: $[a_0^{[1]}, a_1^{[1]},..., a_{n^{[1]}-1}^{[1]}]^T$.
- Multiply the resulting vector by $W^{[2]}$ and add the intercept (bias). 
- Finally, take the sigmoid of the result. If it's greater than 0.5, classify it as a cat.

### L-layer Neural Network
- The input is a (64,64,3) image which is flattened to a vector of size (12288,1).
- The corresponding vector: $[x_0,x_1,...,x_{12287}]^T$ is then multiplied by the weight matrix $W^{[1]}$ and then you add the intercept $b^{[1]}$. The result is called the linear unit.
- Next, take the relu of the linear unit. This process could be repeated several times for each $(W^{[l]}, b^{[l]})$ depending on the model architecture.
- Finally, take the sigmoid of the final linear unit. If it is greater than 0.5, classify it as a cat.


### To test the model using your own image:
- add your image in the images folder
- change your images name in the predict cell in l-layer NN model.
- Run the code and check if the algorithm is right (1 = cat, 0 = non-cat)!
