# Ratchet Swap

A ratchet swap is an interest rate swap with two legs. One leg is a standard floating leg and the other leg is a ratchet leg. The ratchet leg pays a ratchet floating rate. 

The ratchet floating rate coupon is based on an index, e.g., 6-month EURIBOR. The rate is further subject to a minimum decrease of 0 bps and a maximum increase of a threshold, such as, 15 bps. These rates are reset two business days prior to the first day of each coupon period. 

We denote these payments dates, which are 0.5 years apart under 30/360 and are subject to modified business day conventions, by T. Suppose we are at time t, we can visualize the situation The following notation is used:

•	N is the notional amount (here  = EUR 20,000,000)
•	C is the (annualized) coupon rate for the first pay period (here C = 4.50%)
•	 is 0.5 years (under 30/360) between the payments dates  and  
•	 is the forward EURIBOR rate for the period  as seen at time t
•	  is two business days prior to  
•	 is the ratchet rate over  
•	 is the discount factor from time  as seen at time t

Thus L denotes the spot 6 month EURIBOR rate observed two business days prior to payment date   for convenience we will denote this quantity by   At time   one party must pay  where  is defined recursively.
	                                                  

The valuation methodology is based on the Monte Carlo spot LIBOR rate model. The model generates spot rates which log-normally distributed at each reset date. These spot rates are derived from corresponding forward rates whose stochastic behavior is constructed in an arbitrage-free manner. Outcomes for the spot rate are generated for each reset date. These rates are then applied to the ratchet-type payoff structure. The ratchet instrument is then valued by discounting and averaging these payoffs.

Reference:

https://finpricing.com/knowledge.html
