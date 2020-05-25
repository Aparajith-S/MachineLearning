# MachineLearning
## implementing a multilayer perceptron using numpy

A simple one-hidden-layer MLP is implemented from scratch.
- Gradient descent
- Forward pass
- Back-propagation
- Activation function : to keep derivatives simple, a sigmoid is used
- Loss evaluation using MSE

## Gradient descent
- Calculate predictions by a forward pass in the network  
<img src="https://latex.codecogs.com/gif.latex?\hat{y}&space;=&space;\sigma(w_{x}^{(i)}&plus;b)" title="\hat{y} = \sigma(w_{x}^{(i)}+b)" />  
where `i` is the ith layer of the network
- Calculate the error  
  <img src="https://latex.codecogs.com/gif.latex?E&space;=&space;-y\ln(\hat{y})&space;-(1-y)\ln(1-\hat{y})." title="E = -y\ln(\hat{y}) -(1-y)\ln(1-\hat{y})." />
- calculate gradient  
<img src="https://latex.codecogs.com/gif.latex?\triangledown&space;E&space;=&space;\left&space;(&space;\frac{\partial}{\partial&space;w_{1}}E,&space;\frac{\partial}{\partial&space;w_{2}}E,&space;.&space;.&space;.&space;,\frac{\partial}{\partial&space;b}E&space;\right)" title="\triangledown E = \left ( \frac{\partial}{\partial w_{1}}E, \frac{\partial}{\partial w_{2}}E, . . . ,\frac{\partial}{\partial b}E \right)" />  
this can be proven and reduced as  
<img src="https://latex.codecogs.com/gif.latex?\triangledown&space;E&space;=&space;(\hat{y}-y)*(x_1,...,x_n,1)" title="\triangledown E = (\hat{y}-y)*(x_1,...,x_n,1)" />
- calculate Gradient descent step and update weights
<img src="https://latex.codecogs.com/gif.latex?w_i^{k&plus;1}&space;\leftarrow&space;w_i^{k}&space;-&space;{\alpha}*\triangledown&space;E(w_i^k)" title="w_i^{k+1} \leftarrow w_i^{k} - {\alpha}*\triangledown E(w_i^k)" />

