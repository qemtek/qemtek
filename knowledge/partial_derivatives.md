# How do we calculate a partial derivative?

We do this by treating the values of all other parameters as constants (numbers), rather than variables. When we differentiate a constant, it disappears. The equation we are left with is known as a partial derivative.

If we have a model that takes 1 feature and predicts a value (straight line), we have the following equations:

MSE = 1/n * E(yi - yhati)^2

Yhat = x1 * w1 + b (this is our straight line equation, where yhati is our prediction)

Subtracting yhat we get:
MSE = 1/n * E(yi - x1i * w1i + b)^2
If we want to find the partial derivative of the loss with respect to X (this is the derivative we need to find the gradient we need to update X), we need to treat b as a constant when we differentiate.

But we have an issue. The differentiation rules we have learnt [add this] so far only work for single functions. The MSE equation above actually contains two functions.
Function 1: f(a) = a^2
Function 2: f(x, b) = y - x1 * w1 + b
Note the f(x) and f(x, b) notation is used to state that something is a function. Inside the brackets, you add the variables needed by the function to return a value. Y and w1 are constants, not variables, so their values are fixed. X and b are unknowns that can have a range of values, so we specify these as inputs.

A function containing another function is known as a composite function. To differentiate a composite function we need to use the chain rule.
