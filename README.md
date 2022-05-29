# TriangularArbitrageCryptos

Triangular arbitrage is a technique that tries to exploit the price discrepancy across three different assets at the same time.  
For example, we can exchange BTC for USDT, BTC for ETH and ETH back to USDT.   
If the net worth in doing these three trades simultaneously is profitable then the 3 trades are executed simultaneously.  

Here we implement the triangular arbitrage in 4 steps.  
Step 1: Get all the valid crypto combinations. 
Step 2: Perform triangular arbitrage  
Step 3: Place the trade orders  
Step 4: Bundle it together  

Refer to this blog to understand more on triangular arbitrage implemented in this repo:  
https://lakshmi1212.medium.com/automated-triangular-arbitrage-of-cryptos-in-4-steps-a678f7b01ce7

Note:-

ZeroDivisionError: float division by zero

Hi,

I also can see this issue, this is because some of the symbols have 0.0 current price, not sure why this is fetching. anyway just add one more condition when current_price2 is not None is checked in the IF condition. whereever you are calling fetch_current_ticker_price() function.

example:
current_price2 = fetch_current_ticker_price(scrip2)
if current_price2 is not None and current_price2 != 0.0:

I have added 'and current_price2 != 0.0' this code in if condition wherever I am checking 'current_price',

For me working. Please reply if it works for you. Happy Earning
