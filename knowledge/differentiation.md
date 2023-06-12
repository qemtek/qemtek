# What is differentiation?

Differentiation is the process of finding the derivative (or rate of change) of a function. We usually look at the rate of change of something, relative to something else. 

For example, to find the gradient of a straight line, we would look at the change in y, relative to the change in x, over some region of the line. If the change in x was 2, and the change in y was 1, the gradient would be 0.5 (y changes by 0.5 for every 1 change in x).

We could verify this result by differentiating the equation of a straight line and plugging in the numbers. To differentiate an equation with respect to a certain variable, we use the power rule:

We differentiate a function with respect to x. We apply this rule to any term containing x. Here we multiply the term by the power of x, then we drop the power.

Any terms that do not contain x we treat as containing x^0, which is 1. When we differentiate X^0, we get 0. Anything multiplied by 0 is also 0, so any terms that don’t contain x disappear when we differentiate them.

Applying this to the equation of a straight line we get:

Y = mx + c
dy/dx = m

Things get a bit harder if the line is non-linear, as the gradient is different at different parts of the curve. To find the gradient of a point on a non-linear curve, we need to draw a line perpendicular to that point (known as the tangent) and find the gradient of that, as if we were finding the gradient of a straight line.

In most cases we dont actually draw the gradient and calculate the error like this, because we can work it out by differentiating the equation of that line and plugging in the values, but its still useful to be able to visualise this process.

[Give example of differentiating a non-linear curve]

In the context of machine learning, differentiation is important because we need to differentiate our loss function to obtain a gradient for each model parameter, which is then used to make updates to that parameter in order to minimise loss (resulting in a trained model).
