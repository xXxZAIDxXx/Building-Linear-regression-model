# Building-Linear-regression-model
Building Linear regression model (Tensorflow)

This runs the train function and so adjusts the model weights with each epoch. It also calculates the current loss based on the current weight and bias and prints it out. At the end, the model will have adjusted its weights and biases to the point where it can produce pretty good results and we should be able to draw a line of best fit through the data. Run this loop and you should see 100 print statements describing how the loss changes. It should decrease very rapidly at first and then slow down, starting at around 730 and ending close to 1. We’re not so interested in achieving an accuracy measurement with this model; we just want to minimize loss so that we can draw a line through the data and use that to predict future values.

If you want to know the final values of weight and bias, print them out like this:

print(model.weight.numpy())
print(model.bias.numpy())
-----------------
print(model.weight.numpy())
print(model.bias.numpy())
These values should be stored in your model object after training. They should either be very close to your original values of m and b, respectively, or at least describe a line that makes sense. In fact, you can draw a line through your original data set by doing this:
-------------------------------------
new_x = np.linspace(0,4,50)
new_y = model.weight.numpy() * new_x + model.bias.numpy()
plt.scatter(new_x,new_y)
plt.scatter(x,y)
-------------------------------------
new_x = np.linspace(0,4,50)
new_y = model.weight.numpy() * new_x + model.bias.numpy()
plt.scatter(new_x,new_y)
plt.scatter(x,y)
This creates 50 new inputs and 50 new outputs where the outputs are the results of using the model’s final weight and bias as m and b. We should see that even though the final weight and bias may not be the same as m and b, they do provide a good line of best fit through the data.

And that’s it! We have successfully built our simple linear regression model using Tensorflow and employing perceptron logic to a self-made data set. Although it does nothing fancy, it serves as a benchmark to building a more sophisticated model and taught us some machine learning concepts along the way.
