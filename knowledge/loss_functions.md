# What is a loss function?

A loss function is simply an equation that maps model error to loss. The choice of loss function will cause the model to learn differently, so picking a loss function that is relevant for your particular use-case is important.

Lets start by looking at two commonly used loss functions for regression:
Mean Squared Error (MSE) - Take the sum of the squared errors, then divide by the number of samples.

Mean Average Error (MAE) - Take the sum of the absolute errors (ignore and - signs), then divide by the number if samples. 

After calculating the error for each sample, the mean squared error function squares those errors, and then takes the mean of the squared errors. In contrast, the mean average error function just takes the mean of the errors without any squaring. Each of these loss functions will impact model training differently.

When we put the error from the model predictions into the function, we get the loss as the output. If we plot the relationship between error and loss, we get the plots below:

[FIX AXES]

If we calculate our error on training samples, we can then work out the loss. From there we can plot a point on one of the curves above. When we differentiate the curve at that point, we can work out the gradient.


You should understand the following about these functions:
With Mean Squared Error, the relationship with error and loss is squared, so bigger errors will result in much higher loss compared with Mean Average Error. 
For datasets that have a huge range in the target, this can cause the larger predictions to dictate how the model’s weights are updated much more than the smaller predictions, which can impact model performance. 
One advantage of MSE is that at very small error values, the loss is also very small, allowing us to make very small weight updates as we are close to 0 error (which is exactly what we want).

Mean Average Error has the same gradient throughout the function range.
This may be beneficial for datasets with a huge range in the target.
Having the same gradient for large errors and small errors can make training difficult. For large errors, the updates are small so it takes longer to train the model. For small errors, the updates are too big, which makes it difficult for the model to converge on an optimal set of model parameters.
Because the gradient is always the same, we do not need to calculate it each time, making gradient descent very fast for this function.

When training the model, we try to find the weights that give us the lowest error/loss from our training data. This technique is called function optimisation, and involves differentiating the function (to get the gradient), setting the result to zero, and solving the equation. It is a key part of gradient descent. You can find more info here. 