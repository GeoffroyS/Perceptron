# Perceptron<br><br>
"In machine learning, the perceptron is an algorithm for supervised learning of binary classifiers: functions that can decide whether an input (represented by a vector of numbers) belongs to one class or another.[1] It is a type of linear classifier, i.e. a classification algorithm that makes its predictions based on a linear predictor function combining a set of weights with the feature vector. The algorithm allows for online learning, in that it processes elements in the training set one at a time." - Wikipedia<br><br>

More formally, we can pose this problem as a binary classification task where we
refer to our two classes as 1 (positive class) and -1 (negative class) for simplicity. We
can then define an activation function φ(z) that takes a linear combination of certain
input values x and a corresponding weight vector w , where z is the so-called net
￼input ![alt tag]( http://www.sciweavers.org/tex2img.php?eq=%28z%3Dw.x%2B...%2Bw.x%29&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0:)
