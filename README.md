# uscisStats

This project is intent for immigrants to check adjacent receipt number status. It uses USCIS webpage http request to fetch the entire webpage based on a receipt number, then parse the case status filtered by case type, and plot adjacent case status. It also store and compare the result of this execution and last execution result, to report the differences - as the USCIS's progress within these execution.

## Disclaimer
For the good of all immigrants, please use it only for personal reference, and respect the confidentiality of status information for other people's cases. Thank you.

## How To Use
Run directly in Jupyter Note Book, or copy them to python3. 

Please run `concurrent_version.ipynb` for crawling certain range of cases. it will create a `today.json` as a result of initial data. 

Afterwards, you only need to run the `compare_and_statistic.ipynb` to go over the cases saved in the initial data. It will create an copy of `today.json` called `yday.json`, then create a new `today.json` as of the updated result. The report of differences and statistic between `today.json` and `yday.json` will be printed. 

### Constant
```
RECEIPT_NUMBER_BASE: Your receipt number without the last N digits
RANGE_START: A smaller N digits integer as the end of receipt number to check start with
RANGE_END: A larger N digits integer as the end of receipt number to check end with
CASE_TYPE: Type of Form to filter, put 'Form' to show all types of forms
CONCURRENCY_LEVEL: Controls how many requests will be maded concurrently
```

Please note that adjacent receipt number status may only be informative if you are filling with paper base, since each center is processing with different speed. And this information can be used as a reference of how soon will your case being processed, based on the consumptions that
1) Receipt number is increment based on receipt date, and 
2) Each USCIS center is processing by the receipt date

**NOTE: `CONCURRENCY_LEVEL` has been tuned to the proper value - 11. Increasing it will trigger USCIS's throttling, resulting in some requests fail.**


## Contact Me
For any further questions, or if you need help to run you receipt for you, please contact sunnyliyanbo@gmail.com or jino.yolo@gmail.com
