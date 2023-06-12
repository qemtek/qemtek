How do we use chain rule?

The chain rule states that: 

This looks daunting, but like anything it is made up of simple steps. The left hand side states that if we want to differentiate a composite function with respect to x, we have to use the equation on the right hand side. To start with, we should identify what our outer function f() and inner function g() are:

f(x) = x^2
g(x) = y - x1 * w1 + b

On the right hand side we also need g’(x) and f’(x), which are the derivatives of g(x) and f(x). We can do this using the power rule of differentiation, which states that the derivative of x^n is n * x^(n-1).

f’(x) = 2x

g'(x) = (-1 * x1 * w1)' + b'
= -1 * (w1 * x1)' + 0
= -1 * w1 * 1
= -w1

Plugging these into the equation we get:

f’(g(x))g’(x) = 2(y - x1 * w1 + b) * -w1
dMSE/dx = -2w1(y - x1 * w1 + b)

Once we have this equation, to find the gradient at the particular point, we have to insert the values for all of our variables.

[do a proper example of this]

And now we have the gradient update for x. The last thing to do is to multiply this gradient by our learning rate to ensure that we are only making small updates to our model parameters. What the learning rate should be is dependent on the problem you are trying to solve, but 0.01 or 0.001 are good starting points.
