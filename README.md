# Perceptron<br><br>
"In machine learning, the perceptron is an algorithm for supervised learning of binary classifiers: functions that can decide whether an input (represented by a vector of numbers) belongs to one class or another.[1] It is a type of linear classifier, i.e. a classification algorithm that makes its predictions based on a linear predictor function combining a set of weights with the feature vector. The algorithm allows for online learning, in that it processes elements in the training set one at a time." - Wikipedia<br><br>

More formally, we can pose this problem as a binary classification task where we
refer to our two classes as 1 (positive class) and -1 (negative class) for simplicity. We
can then define an activation function φ(z) that takes a linear combination of certain
input values x and a corresponding weight vector w , where z is the so-called net
￼input ![alt tag]( http://www.sciweavers.org/tex2img.php?eq=%28z%3Dw.x%2B...%2Bw.x%29&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0):<br>
![alt tag](http://www.sciweavers.org/tex2img.php?eq=w%20%3D%20%5Cbegin%7Bbmatrix%7Dw_%7B1%7D%20%20%5C%5C%20...%20%5C%5Cw_%7Bm%7D%20%5Cend%7Bbmatrix%7D%2C%20x%20%3D%20%5Cbegin%7Bbmatrix%7Dx_%7B1%7D%20%20%5C%5C%20...%20%5C%5Cx_%7Bm%7D%20%5Cend%7Bbmatrix%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)<br>

Now, if the activation of a particular sample ![alt tag](http://www.sciweavers.org/tex2img.php?eq=%20x%5E%7Bi%7D%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0) , that is, the output of φ(z), is ￼￼greater than a defined threshold θ , we predict class 1 and class -1, otherwise. In the
perceptron algorithm, the activation function φ (⋅) is a simple unit step function, which is sometimes also called the Heaviside step function:<br>
![alt tag](http://www.sciweavers.org/tex2img.php?eq=%20%CF%86%28z%29%20%3D%5Cbegin%7Bcases%7D1%20%26%20z%20%3E%3D%200%5C%5C-1%20%26%20otherwise%5Cend%7Bcases%7D%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)
For simplicity, we can bring the threshold θ to the left side of the equation and define a weight-zero as ![alt tag](http://www.sciweavers.org/tex2img.php?eq=%20w_%7B0%7D%20%20%3D%20%E2%88%92%20%5Ctheta%20%2C%20x_%7B0%7D%20%3D1&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0), so that we write z in a more compact form ![alt tag](http://www.sciweavers.org/tex2img.php?eq=z%3D%20w_%7B0%7D.x_%7B0%7D%2Bw_%7B1%7D.x_%7B1%7D%2B...%2Bw_%7Bm%7D.x_%7Bm%7D%3D%20w%5E%7BT%7D.x%20%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0) and ![alt tag](http://www.sciweavers.org/tex2img.php?eq=%20%CF%86%28z%29%20%3D%5Cbegin%7Bcases%7D1%20%26%20z%20%3E%3D%200%5C%5C-1%20%26%20otherwise%5Cend%7Bcases%7D%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0))
