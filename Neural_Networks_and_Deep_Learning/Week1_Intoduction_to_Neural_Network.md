## What is a neural network?

<img src='image/Fig1.png' width="400" height= "200" />


* *Let's start to the Housing Price Prediction example.*
    * Let's say you have a data sets with six houses.
    * You know the size of the houses in square feet or square meters
    * You know the price of the house
    * You want to fit a function to predict the price of the houses, the function of the size. 

* In linear regression 
    * We put a straight line to these data 
    * The prices can never be negative so for this let's bend the curve here. 
    * the blue line ends up being your function for predicting the price of the house as a function of this size. 
    * You can think of this function as a very simple neural network. 
    * It's almost as simple as possible neural network

<img src='image/Fig3.png' width="600" height= "200" />

* Simple neural network
* We have a input to the neural network: the size of a house(we call **x**). 
* **x** goes into this node, this little circle which is a single neuron and then it outputs the price (we call **y)**. 
* A single neuron in a neural network, implements the Relu function.
* The ReLU function which stands for rectified linear units means taking a max of zero (0) which is why you get a function shape like this.


**All the neuron does is takes inputs, computes the linear function, takes a max of zero, and then outputs the estimated value**

 * A larger neural network is then formed by taking many of the single neurons and stacking them together. So, if you think of this neuron that's being like a single Lego brick, you then get a bigger neural network by stacking together many of these Lego bricks.
 
* Instead of predicting the price of a house just from the size, you have also other features.
* Such as 
    * the size of the house 
    * the number of bedrooms, 
    * the zip code or postal code ,which is a future to tells you, walkability
    * the wealth of the neighborhood
* With  given these input features, the job of the neural network will be to predict the price y.
