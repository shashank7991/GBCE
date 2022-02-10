# GBCE

## Requirements

Python 3.7 and no third-party libraries were used.

## Code structure and usage

All the key feature is fully contained in the top-level module `super_simple_stocks`.
It is to be used by packing a set of instances of `Stock` in a sequence and pass it as the only argument to `GBCE` initializer. The resulting instance is to be used as a representation of the complete GBCE.

`Stock` itself is abstract, objects may only be created by means of its two inheriting classes, `CommonStock` and `PreferredStock`.

From that point on the method `GBCE.record_trade` may be used to record new trades.

The calculations requested in the assignment instructions are then supplied by the following properties or methods:

- For a given instance of `Stock`:
  - _Calculate the dividend yield_: `Stock.dividend_yield`
  - _Calculate the P/E Ratio_: `Stock.price_earnings_ratio`
  - _Record a trade, with timestamp, quantity of shares, buy or sell indicator and price_: Create an instance of `Trade` and supply it to an instance of`GBCE` that contains the proper stock my means of `record_trade`
  - _Calculate Stock Price based on trades recorded in past 15 minutes_: `Stock.price`
- _Calculate the GBCE All Share Index using the geometric mean of prices for all stocks_: `GBCE.all_share_index`.

Basic documentation is included in the code.

## Tests

A moderately extensive suite of tests is included in `tests/`. 
Run them by executing the following commands:
 ````
$ git clone https://github.com/aadroher/super_simple_stocks
$ cd super_simple_stocks/
$ python -m unittest -v
````
