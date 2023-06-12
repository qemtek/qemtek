# What is gradient descent?

Gradient descent is the idea that, given a starting point, we can find the minimum of a function by iteratively calculating the gradient at that point, subtracting it from the point, then finding the parameter values that would generate the new point. This statement relies on two conditions:

The function is convex, which means if you take two points anywhere on the curve, the curve between those points is always below them (see diagram, compare with the plots above).
The size of the update is small enough to ensure that we dont keep bouncing between the left and right size of the minimum point. We can achieve this by multiplying the gradient update by a smaller value, which is referred to as the learning rate.

To find the gradient for a particular parameter, we have to differentiate the loss equation ‘with respect to’ (wrt) our parameter. The result is what is known as a partial derivative (partial because it is not the complete derivative, because the result is only in terms of the parameter we are interested in).
