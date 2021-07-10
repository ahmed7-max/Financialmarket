# Financialmarket
Financial market using geometric brownian motion

#Let’s simulate a financial market using geometric brownian motion

import numpy as np
import matplotlib.pyplot as plt
mu = 0.01
sigma = 0.1
start_price = 40

 #Then we generate 4000 values for the returns and finally we build the price time series starting from the start price

returns = np.random.normal(loc=mu, scale=sigma, size=400)
price = start_price*(1+returns).cumprod()
plt.plot(price)
