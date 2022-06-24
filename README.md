# mortgage-calculator
Simple fixed rate mortgage calculator for personal finances. Made for my own use, but still fairly user-friendly. Calculates payments during and after the initial term, incorporating the Bank of England base rate and any overpayments. It's meant to be used in conjunction with the numbers provided by mortgage lenders.

The main utility is in the Jupyter notebook file mortgage-calculator.ipynb. Just plug in the relevant numbers to generate the output arrays:

````python 
m = mortgage(principal=200000,     # Amount *borrowed* (not the property price), e.g. £200,000 (or whatever currency)
             total_period=25*12,   # Total term in *months*. E.g. 25*12 for a 25 year term
             init_period=5*12+3,   # Initial term in *months*. E.g. for 5-year fixed term, use 60 (63 ish in practice)
             init_payment=747.14,  # Monthly payments in whatever currency
             init_rate=0.0286,     # Initial term interest rate expressed in decimal. E.g. for 2.86% use 0.0286
             subs_rate=0.0449,     # Subsequent term interest rate expressed in decimal. E.g. for 4.49% use 0.0449
             base_rate=0.1,        # Bank of England base rate during the *subsequent* term. E.g. for 10%, use 0.1
             over_payment=100      # Optional monthly overpayments in whatever currency
            )
````



