# AutoRegressiveModeling
This repository contains a Google Colab notebook in which we use a basic autoregressive model to forecast and analyze the behavior of the log-returns of stocks, and use the model parameters to support basic conclusions about several stocks.

Let $\{P_t\}$ be the closing prices of a stock, and define the log-returns to be
$$X_t = \log\left(\frac{P_t}{P_{t-1}}\right).$$

We model the log-returns as
$$X_{t+1}-\mu = \phi\cdot(X_t-\mu) + \varepsilon_t$$,
where $\varepsilon_t\sim\mathcal{N}(0, \sigma_{\varepsilon}^2)$ is Gaussian noise. We include functions to determine $\mu, \phi$, and $\sigma_{\varepsilon}^2$ through maximum likelihood estimation, and use these values to answer basic questions about the volatility of several stocks, both stable and unstable.
