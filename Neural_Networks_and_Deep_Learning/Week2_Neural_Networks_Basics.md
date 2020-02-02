# WEEK2: Neural Networks Basics

## Logistic Regression as a Neural Network

### Binary Classification

* Logistic regression is an algorithm for binary classification. 
* An example of a binary classification problem: Let's say you want to output a label to recognize images as either being a cat, in which case you output 1, or not-cat in which case you output 0,

* input image is 64 pixels by 64 pixels, then you would have 3x64X64 matrices corresponding to the red, green and blue pixel, what we're going to do is unroll all of these pixel values into an input feature vector x. 
* Define a feature vector x corresponding to this image as follows. We're just going to take all the pixel values 255, 231, and so on. 255, 231, and so on until we've listed all the **red pixels**. And then eventually 255 134 255, 134 and so on until we get a long feature vector listing out all the red, green and blue pixel intensity values of this image. 

* So in binary classification, our goal is to learn a classifier that can input an image represented by this feature vector x. And predict whether the corresponding label y is 1 or 0, that is, whether this is a cat image or a non-cat image.

#### Let's now lay out some of the notation that we'll use throughout the rest of this course. 

* `(x,y)` :represent a single training example:
    * x  --> *x-dimensional feature vector*
    * y  --> *label* (either 0 or 1).
* `$m$`: the number of training samples.

* The training sets will be written `(x(1), y(1))`: input and output for your first training example 
* `(x(2), y(2))` for the second training example up to `(x(m), y(m))` which is your last training example.


\begin{equation*}
X=
\begin{bmatrix}
\vdots & \vdots & \cdots  &  \vdots \\
 x^{(1)} & x^{(2)} & \cdots & x
 ^{(m)} \\
\vdots & \vdots & \cdots & \vdots
\end{bmatrix}
\end{equation*}


\begin{equation*}
Y=
\begin{bmatrix}
 y^{(1)} & y^{(2)} & \cdots & y^{(m)} \\
\end{bmatrix}
\end{equation*}

* **MATRIX X**

    * X set inputs `x(1)`, `x(2)` and so on `x(m)` and stacking them in columns. 
        * We take `x(1)` and put that as a first column of this matrix,
        * `x(2)`, put that as a second column and so on down to `x(m)`, 
        
    * Matrix X will have `m` columns, where `m` is the number of train examples and the number of railroads, or the height of this matrix is `n(x)`. 
    
    * X is a n(x) by m dimensional matrix,**X Shape :** `(n(x),m)` 

* **MATRIX Y**

    * Y to be equal to `y(1)`, `y(2)`, up to `y(m)` like so. 
    * Y here will be a `1` by`m` dimensional matrix. **Y Shape :** `(1,m)`

