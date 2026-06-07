# Functional Data Regression Using Linear Functionals

In this laboratory work, we consider a regression problem where the input object is not a finite vector of features but a function \(x(t)\) defined on the interval \([0,1]\). The goal is to transform each function into a finite-dimensional feature vector using linear integral functionals and then fit a linear regression model.

For a function \(x(t)\) and a weight function \(\varphi_k(t)\), the \(k\)-th feature is defined as the inner product in the space \(L^2[0,1]\):

$$
z_{ik} = \langle x_i,\varphi_k\rangle
       = \int_0^1 x_i(t)\varphi_k(t)\,dt.
$$

After computing the features, the regression model takes the form

$$
\hat y_i = \beta_0 + \sum_{k=1}^{m}\beta_k z_{ik}.
$$

The model can also be interpreted through a weight function

$$
w(t)=\sum_{k=1}^{m}\beta_k\varphi_k(t),
$$

since

$$
\hat y(x)=\beta_0+\langle x,w\rangle.
$$

The main objective of the experiments is to compare different systems of functionals and to study the influence of the number of functionals, regularization, noise level, and grid density on prediction quality.
