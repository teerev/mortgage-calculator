# mortgage-calculator
Simple fixed rate mortgage calculator for personal finances. Made for my own use, but still fairly user-friendly. Calculates payments during and after the initial term, incorporating the Bank of England base rate and any overpayments. It's meant to be used in conjunction with the numbers provided by mortgage lenders.

The main utility is in the Jupyter notebook file mortgage-calculator.ipynb. Just plug in the relevant numbers to generate the output arrays:

````python 
m = mortgage(principal=200000,
             total_period=25*12,
             init_period=5*12+3,
             init_payment=747.14,
             init_rate=0.0286,
             subs_rate=0.0449,
             base_rate=0.1,
             over_payment=100
            )
````



