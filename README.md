# A Python implementation of gradient descent
# gradient_descent_stuck_local_min.ipynb

I implemented gradient descent approach in Python on a 1D and 2D functions. The function has lots of local minima
and gradient descent doesn't work too well on a 1d/2d function because it gets trapped in those local minima.

Also demostrated how gradient descnt can get trapped in a local maxima when the gradient is 0, and implementted a way to untrap the algorithm

Seeing how gradient descent doesn't work too well on 1d and 2d functions, it's amazing to see that it generally works well in deep learning. The exact reason isn't completely clear, but there are two possible solutions:

1. There are many equally as good local minima in deep learning for gradient descent to settle into in high dimensional space

2. It's rare to have local minima in high dimensional space, considering for that to happen the point needs to be the local minima in all dimensions. In reality when a point is the local minima might be the local minima for some dimensions but not others, so gradient descent can keep learning until it reaches to the global minima. One 2D example is a saddle point, which is the local minima in one dimension but not the other. So gradient descent can move down the saddle point without being trapped.

# A Python implementation of dynamic learning rate and early stopping with gradient descent
# gradient_descent_dynamic_eta.ipynb

I implemented gradient descent approach in Python with dynamic learning rate and early stopping. 

If loss function continue to decrease, multiply learning rate by a constant (eg 1.05) every epoch. Otherwise decrease learning rate, divide learning rate by that constant

If loss function decrement is less than a set amount, trigger early stopping

As shown in the results, the vanilla gradient descent takes 12s to finish running the full 1000 epoches. While gradient descent with dynamic learning rate and early stopping takes just 0.087s running only 30 epoches, with even higher accuracy. It shows dynamic gradient descent with early stopping can save significant amount of time and resource. 

Alex Chen
