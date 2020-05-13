+++
title = "flux"
outputs = ["Reveal"]
[logowg]
src = "/img/wg_white_removed_medium.png"
[logoflux]
src = "/img/ml/flux_icon.png"
[reveal_hugo]
custom_theme = "mh.scss"
custom_theme_compile = true
+++

<br>
## <center>Machine learning in <span style="vertical-align: middle"><img src="/img/ml/julia.png" " alt="" height="" width="130"></span> with</center>{{<img src="/img/ml/flux_tall.png" title="" width="60%" line-height="0.5rem">}}{{</img>}}

#### <center>Marie-Hélène Burle</center>

###### <center><training@westgrid.ca></center>

###### <center>*May 13, 2020*</center>

---

## <center>Machine learning</center>

{{%fragment%}}
<br><br>
<center>Computer programs whose performance at a task improves with experience</center>
{{%/fragment%}}

---

## <center>Neural networks</center>

---

##### <center>Biological neuron</center>
<br>
{{<img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/Neuron.svg" title="" width="100%" line-height="0.5rem">}}
Schematic from <a href="https://commons.wikimedia.org/w/index.php?curid=1474927">Dhp1080, Wikipedia</a>
{{</img>}}

<br>
<center>Electrically excitable cell receiving information through dendrites & transmitting the compiled output through the axon</center>

---

##### <center>Artificial neuron</center>

{{<img src="/img/ml/artificial_neuron_nw.png" title="" width="65%" line-height="0.5rem">}}
Modified from <a href="https://royalsocietypublishing.org/doi/10.1098/rsta.2019.0163">O.C. Akgun & J. Mei 2019</a>
{{</img>}}

<center>Analogous design</center>
The weighted sum of a set of numeric inputs is passed\\
through an activation function before yielding a numeric output

---

##### <center>More realistic biological neuron</center><br>

{{<img src="/img/ml/neuron_grayanatomy_nw.png" title="" width="80%" line-height="0.5rem">}}
<br>a: axon, c: dendrites <br><br><br>
Drawing from stained neuron from <a href="https://en.wikipedia.org/wiki/Gray's_Anatomy">Gray's Anatomy</a>
{{</img>}}

<center>The actual level of branching is vastly superior</center>

---

##### <center>Biological neural network</center>

{{<img src="/img/ml/brain_neurons.jpg" title="" width="90%" line-height="0.5rem">}}
<br>Neurons (in green) in mouse cortex; the dark branches are blood vessels <br><br><br>
Image by <a href="https://news.berkeley.edu/2020/03/19/high-speed-microscope-captures-fleeting-brain-signals/">Na Ji, UC Berkeley</a>
{{</img>}}

<center>The human brain has 65–90 billion of them</center>
and it is a system with emergent properties

---

##### <center>Artificial neural network (ANN)</center>

{{<img src="/img/ml/nn_single_layer_nw.png" title="" width="60%" line-height="0.5rem">}}
Modified from <a href="https://royalsocietypublishing.org/doi/10.1098/rsta.2019.0163">O.C. Akgun & J. Mei 2019</a>
{{</img>}}

<center>**Fully-connected**, **single-layer**, **feedforward** neural network</center>

---

##### <center>Artificial neural network (ANN)</center>

{{<img src="/img/ml/nn_multi_layer_nw.png" title="" width="90%" line-height="0.5rem">}}
<br>Neural network with 2 hidden layers <br><br><br>
From <a href="https://themaverickmeerkat.com/2020-01-10-TicTacToe/">The Maverick Meerkat</a>
{{</img>}}

<center>**Fully-connected**, **feedforward**, **deep** neural network</center>

---

##### <center>Threshold potential</center>

{{<img src="/img/ml/all_none_law_nw.png" title="" width="48%" line-height="0.5rem">}}
Modified from <a href="https://commons.wikimedia.org/w/index.php?curid=78013076">Blacktc, Wikimedia</a>
{{</img>}}
<br>
<center>The information is an all-or-nothing electrochemical pulse or action potential</center>
Greater stimuli don't produce stronger signals but increase firing frequency

---

##### <center>Activation functions</center>

{{<img src="/img/ml/act_func_nw.png" title="" width="50%" line-height="0.5rem">}}
From <a href="https://arxiv.org/abs/1908.08681">Diganta Misra 2019</a>
{{</img>}}

<center>Many activation functions have been tried</center>
Choices based on problem complexity & available computing budget

---

##### <center>Bias</center>
<br>

A bias allows to [shift the output of the activation function to the right or to the left](https://stackoverflow.com/q/2480650/9210961)

Offset

---

##### <center>Convolutional neural network (CNN)</center>

Image recognition
spatial structure
local receptive field (small section of image) connected to one hidden neuron
slide the local receptive field by a stride length to connect to a second hidden neuron on the same layer
you end up with a convolved feature
Large image: too many neurons and pixels are independent of each other if they are not close together

---

##### <center>Recurrent neural network (RNN)</center>

Chain structured data (e.g. text)

<center>Long Short-Term Memory (LSTM)</center>
<br>

{{<img src="https://upload.wikimedia.org/wikipedia/commons/3/3b/The_LSTM_cell.png" title="" width="80%" line-height="0.5rem">}}
From <a href="https://commons.wikimedia.org/w/index.php?curid=71836793">Guillaume Chevalier, Wikipedia</a>
{{</img>}}

---

## <center>How do neural networks learn?</center>
<br>

---
 
Paradigm of the current approach to AI:<br><br>

<center>feeding vast amounts of data to algorithms;</center>
so it is a **data driven** approach \\
and it is about **learning**, \\
i.e. strengthening **pathways** <br><br><br>

Example in image recognition:

rather than coding all the possible ways, pixel by pixel, that a picture can represent an object, we feed examples (image/label pairs) to a neural network

---

##### <center>Supervised learning</center>
<br>
Training set of example input/output pairs

{{%fragment%}}
<br>
Goal:\\
If \\(X\\) is the space of inputs and \\(Y\\) the space of outputs, find a function \\(h\\) so that\\
for each \\(x\_i \in X\\), \\(h(x\_i)\\) is a predictor for the corresponding value \\(y\_i\\)

(i.e. find the relationship between inputs and outputs)
{{%/fragment%}}

{{%fragment%}}
<br>
Continuous outputs: **Regression** \\
Discrete outputs: **Classification**
{{%/fragment%}}

---

in fact h\_\theta()

\theta represents the parameters of the NN

---

##### <center>Unsupervised learning</center>
<br>
Unlabelled data

<br>
Look for structure within the data

<br>
*Examples:* \\
Clustering\\
Social network analysis\\
Market segmentation\\
PCA\\
Cocktail party algorithm (signal separation)

---

###### <center>Cost function</center>

---

Feature (attribute): input variable\\
Target variable: output variable\\

---

##### <center>Overfitting</center>

{{<img src="/img/ml/overfitting.png" title="" width="40%" line-height="0.5rem">}}
From <a href="https://commons.wikimedia.org/w/index.php?curid=3610704">Chabacano, Wikipedia</a>
{{</img>}}

Some noise from the data was extracted by the model while it does not represent general meaningful structure and has no predictive power

---

##### <center>Heaviside step function</center>
<br>

---

##### <center>Gradient descent</center>
<br>

{{<img src="https://upload.wikimedia.org/wikipedia/commons/f/ff/Gradient_descent.svg" title="" width="100%" line-height="0.5rem">}}
From <a href="https://commons.wikimedia.org/w/index.php?curid=20569355">Olegalexandrov & Zerodamage, Wikipedia</a>
{{</img>}}

Iterative optimization method
Adjust the weights and the bias

---

###### <center>Batch gradient descent</center>

Use all examples in each iteration

Slow for large data set:\\
you only adjust the weights after all the samples have been through.

---

###### <center>Stochastic gradient descent</center>

Use one example in each iteration

Much faster than batch gradient descent:\\
you adjust the weight after each example

---

###### <center>Mini-batch gradient descent</center>

Intermediate approach:\\
Use mini-batch size examples in each iteration

Allows a vectorized approach that stochastic gradient descent did not allow
So you can parallelize

---

##### <center>Backpropagation algorithm</center>
<br>


---

##### <center>Epoch</center>
<br>

one forward pass and one backward pass of all the training examples

---

{{<img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/Recurrent_neural_network_unfold.svg" title="" width="%" line-height="0.5rem">}}
From <a href="https://commons.wikimedia.org/w/index.php?curid=1474927">fdeloche, Wikipedia</a>
{{</img>}}

---

#### <center>Flux</center>
<br>

{{<img src="https://upload.wikimedia.org/wikipedia/commons/3/37/Gated_Recurrent_Unit%2C_base_type.svg" title="" width="%" line-height="0.5rem">}}
From <a href="https://commons.wikimedia.org/w/index.php?curid=66225938">Jeblad, Wikipedia</a>
{{</img>}}


---

## <center>How to implement neural networks?</center>

---

#### <center>ML libraries</center>
<br>

The most famous ML libraries are:

- [PyTorch](https://pytorch.org/), developed by Facebook's AI Research lab\\
- [TensorFlow](https://www.tensorflow.org/), developed by the Google Brain Team

Both are most often used through their Python interfaces<br><br>

Julia's syntax is very well suited for the implementation of mathematical models & Julia's speed is attractive in computation hungry fields

So Julia has seen the development of many ML packages

---

#### <center>ML packages in Julia</center>
<br>

There is a [wrapper for TensorFlow](https://github.com/malmaud/TensorFlow.jl), a package for [probabilistic ML](https://github.com/TuringLang/Turing.jl), a [framework to compose ML models](https://github.com/alan-turing-institute/MLJ.jl), an [implementation of the scikit-learn API](https://github.com/cstjean/ScikitLearn.jl), and others, but the two most popular ML packages are [Flux](https://github.com/FluxML/Flux.jl) and [Knet](https://github.com/denizyuret/Knet.jl).

Today, we will have a look at Flux.

---

## <center>Example application:</center>
## <center>classifying the [MNIST](http://yann.lecun.com/exdb/mnist/)</center>

---

#### <center>The [MNIST](http://yann.lecun.com/exdb/mnist/) database</center>
<br>
{{<img src="/img/ml/mnist_nw.png" title="" width="70%" line-height="0.5rem">}}
Modified from <a href="https://commons.wikimedia.org/w/index.php?curid=64810040">Josef Steppan, Wikimedia</a>
{{</img>}}
<br>

<center>A set of images of handwritten digits</center>
used for testing ML systems

---

#### <center>The [MNIST](http://yann.lecun.com/exdb/mnist/) database</center>
<br>
{{<img src="/img/ml/mnist_nw.png" title="" width="70%" line-height="0.5rem">}}
Modified from <a href="https://commons.wikimedia.org/w/index.php?curid=64810040">Josef Steppan, Wikimedia</a>
{{</img>}}
<br>

<center>pair of greyscale RGB codes (from 0 to 255) &</center>
labels from 0 to 9 which represents which number they actually are

---

#### <center>The [MNIST](http://yann.lecun.com/exdb/mnist/) database</center>
<br>
{{<img src="/img/ml/mnist_classify_nw.png" title="" width="90%" line-height="0.5rem">}}
<span style="font-size: 0.9rem;">&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;From <a href="https://www.freecodecamp.org/news/big-picture-machine-learning-classifying-text-with-neural-networks-and-tensorflow-d94036ac2274/">FreeCodeCamp</a></span>
{{</img>}}
<br>
Goal: assign each image to one of 10 classes (the digits 0...9)

---

#### <center>The [MNIST](http://yann.lecun.com/exdb/mnist/) database</center>
<br>
{{<img src="/img/ml/mnist_classify_nw.png" title="" width="90%" line-height="0.5rem">}}
<span style="font-size: 0.9rem;">&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;From <a href="https://www.freecodecamp.org/news/big-picture-machine-learning-classifying-text-with-neural-networks-and-tensorflow-d94036ac2274/">FreeCodeCamp</a></span>
{{</img>}}
<br>

&emsp;&ensp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;60,000 images to **train**\\
&emsp;&ensp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;10,000 images to **test**
<br>

---

#### <center>Classify [MNIST](http://yann.lecun.com/exdb/mnist/)</center>
<br>
{{<img src="/img/ml/1*av47vApmzuM0AN21VaIcSA.png" title="" width="%" line-height="0.5rem">}}
{{</img>}}

---

Load packages and bring functions into scope
{{<i>}}
```julia
using Flux
using Flux: onehotbatch, onecold, crossentropy, throttle
# saves us from having to type Flux.onehotbatch(), etc.
```
<br>
Training data
{{<i>}}
```julia
img = Flux.Data.MNIST.images();   # create an array with the training images
lab = Flux.Data.MNIST.labels();   # create an array with the training labels
```

---

##### <center>What does the **image** data look like?</center>

{{<i>}}
```julia
typeof(img)
```
{{<o>}}
```julia
Array{Array{ColorTypes.Gray{FixedPointNumbers.Normed{UInt8,8}},2},1}
```
{{<i>}}
```julia
length(img)
```
{{<o>}}
```julia
60000
```
{{%c%}}img{{%/c%}} is a one-dimensional array of 60,000 two-dimensional arrays

---

{{<i>}}
```julia
img[1]
```
{{<o>}}
```julia
28×28 Array{Gray{N0f8},2}
with eltype ColorTypes.Gray{FixedPointNumbers.Normed{UInt8,8}}:
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)  …  Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)  …  Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)  …  Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)  …  Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)  …  Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)  …  Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
 Gray{N0f8}(0.0)  Gray{N0f8}(0.0)     Gray{N0f8}(0.0)  Gray{N0f8}(0.0)
```
Each of these arrays represents one training image and is made of {{%b%}}28x28{{%/b%}} values of the gray scale of each pixel of the image

---

{{<i>}}
```julia
img[1][1, 1]
```
{{<o>}}
```julia
Gray{N0f8}(0.0)
```
This is the value of the top left pixel of the first image of the training dataset
<br>

{{%fragment%}}
{{<i>}}
```julia
float(img[1][1, 1])
```
{{<o>}}
```julia
0.0
```
It can be converted to a float
{{%/fragment%}}

---

Let's see what a few of these images look like:
{{<i>}}
```julia
using Plots
plot(plot(img[5]), plot(img[8]), plot(img[87]), plot(img[203]))
```
{{<o>}}
{{<imgshadow src="/img/ml/digit.png" title="" width="40%" line-height="0.5rem">}}
{{</imgshadow>}}

---

##### <center>What does the **label** data look like?</center>

{{<i>}}
```julia
typeof(lab)
```
{{<o>}}
```julia
Array{Int64,1}
```

{{<i>}}
```julia
length(lab)
```
{{<o>}}
```julia
60000
```
{{%c%}}lab{{%/c%}} is a one-dimensional array of 60,000 integers

---

{{<i>}}
```julia
lab[1]
```
{{<o>}}
```julia
5
```
<br>
This is the value of the first label

---

The 5<sup>th</sup>, 8<sup>th</sup>, 87<sup>th</sup>, and 203<sup>rd</sup> images were:
{{<imgshadow src="/img/ml/digit.png" title="" width="20%" line-height="0.5rem">}}
{{</imgshadow>}}

{{%fragment%}}
Here are the corresponding labels:
{{<i>}}
```julia
[lab[5], lab[8], lab[87], lab[203]]'
```
{{<o>}}
```julia
1×4 LinearAlgebra.Adjoint{Int64,Array{Int64,1}}:
 9  3  3  8
```
{{%/fragment%}}

---

###### <center>onehotbatch</center>
<br><br>

{{%c%}}onehotbatch(){{%/c%}} turns a batch of labels into a binary matrix

<br>

{{%c%}}onecold(){{%/c%}} performs the inverse operation

---

###### <center>onehotbatch</center>

{{<i>}}
```julia
lab[1:3]
```
{{<o>}}
```julia
3-element Array{Int64,1}:
 5
 0
 4
```

---

###### <center>onehotbatch</center>

{{<i>}}
```julia
onehotbatch(lab[1:3], 0:9)
```
{{<o>}}
```julia
10×3 Flux.OneHotMatrix{Array{Flux.OneHotVector,1}}:
 0  1  0
 0  0  0
 0  0  0
 0  0  0
 0  0  1
 1  0  0
 0  0  0
 0  0  0
 0  0  0
 0  0  0
```

---

###### <center>onecold</center>

{{<i>}}
```julia
onecold(onehotbatch(lab[1:3], 0:9), 0:9)
```
{{<o>}}
```julia
3-element Array{Int64,1}:
 5
 0
 4
```

---

###### <center>Splatting</center>

Consider this simple example:
{{<i>}}
```julia
+(2, 3)
```
{{<o>}}
```julia
5
```
{{<i>}}
```julia
a = (2, 3);
+(a)
```

{{%fragment%}}
{{<o>}}
```julia
ERROR: MethodError: no method matching +(::Tuple{Int64,Int64})
```
{{%/fragment%}}

---

###### <center>Splatting</center>

Consider this simple example:
{{<i>}}
```julia
+(2, 3)
```
{{<o>}}
```julia
5
```
{{<i>}}
```julia
a = (2, 3);
+(a...)
```

{{%fragment%}}
{{<o>}}
```julia
5
```
{{%/fragment%}}

---

###### <center>Relu: rectifier activation function</center><br>

&emsp;&emsp;&emsp;&emsp;&emsp;\\(f(x) = max(0, x)\\)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; In Flux: {{%c%}}relu(){{%/c%}}

{{<i>}}
```julia
x = -5:5; plot(x, relu.(x), legend = false)
```
{{<o>}}
{{<imgshadow src="/img/ml/relu.png" title="" width="50%" line-height="0.5rem">}}
{{</imgshadow>}}

---

###### <center>Softmax activation function</center><br>

\\[\sigma(\mathbf{z})\_i=\frac{e^{z\_i}}{\sum\_{j=1}^{K}e^{z\_j}}\\]

\\[\text{ for }i=1,...,K\text{ and }\mathbf{z}=(z\_1,...,z\_K)\in\mathbb{R}^K\\]

{{<si "1.3" "(\(\mathbb{R}\) represents the set of real numbers)">}}

<br>
<center>Normalizes a vector of real numbers</center>
into a vector of numbers between 0 and 1 which add to 1

---

###### <center>Softmax activation function</center><br>

<center>In Flux: {{%c%}}softmax(){{%/c%}}</center>
{{<i>}}
```julia
plot(softmax(-5.0:0.1:5.0))
```
{{<o>}}
{{<imgshadow src="/img/ml/softmax.png" title="" width="50%" line-height="0.5rem">}}
{{</imgshadow>}}

---

##### <center>Cross entropy loss function</center><br>

Cross entropy: distance between what the model believes the output distribution should be and what the original distribution really is

---

## <center>Let's start building models</center>

---

#### <center>Single-layer perceptron (SLP)</center>

Linearly separable patterns only

Building block of ANN

y = sigma w\_i*x\_i + b

x\_i input
w\_i weight
b bias
y output

Training: Peceptron Learning Rule (PLR) or Delta Rule

---

#### <center>Multi-layer perceptron (MLP)</center>

{{<img src="https://upload.wikimedia.org/wikipedia/commons/4/46/Colored_neural_network.svg" title="" width="%" line-height="0.5rem">}}
From <a href="https://commons.wikimedia.org/w/index.php?curid=24913461">Glosser.ca, Wikipedia</a>
{{</img>}}

Theoretically, universal function approximator

One single layer: shallow neural network
Multiple single layer: deep neural network

Training (weights and biases updated): backpropagation with gradient based optimization algorithms such as SGD, RMSProp, Adam

---

#### <center>Convolutional neural network</center>

---

{{%c%}}Dense(){{%/c%}} fully connected layer

---

adam: optimizer

---

#### <center>Saving models</center>
<br>

<center>[BSON.jl](https://github.com/JuliaIO/BSON.jl) allows to save models in [Binary JSON](http://bsonspec.org/) format</center>

---

transfer learning (TL): instead of random initialization, start from model trained on related problem for weight initialization
allows to get good results on small datasets

https://github.com/FluxML/ONNX.jl

---

#### <center>GPU support</center>
<br>

[](https://github.com/JuliaGPU/CuArrays.jl)

{{<i>}}
```julia
using CuArrays
```
Moving data to the GPU with the function{{%c%}}gpu(){{%/c%}}

It can be used conveniently by piping code to the gpu function
{{<i>}}
```julia
xxxx |> gpu
```
Moving data back to the CPU with the function {{%c%}}cpu(){{%/c%}}
{{<i>}}
```julia
xxxx |> cpu
```

---

<img src="/img/ml/flux_icon.png" style="position: absolute; top: 22%; left: 51.2%; width: 4.5%;">

## <center style="font-size: 5.0rem; font-variant: small-caps">Questions?</center>

---

useful links
