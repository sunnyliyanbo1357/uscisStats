# uscisStats

This project is intent for immigrants to check adjacent receipt number status. It uses USCIS webpage http request to fetch the entire webpage based on a receipt number, then parse the case status filtered by case type, and plot adjacent case status. Since each request to USCIS website can take up to 10 seconds, the entire run can take hours based on your range. For the good of all immigrants, please use it only for personal reference, and respect the confidentiality of status information for other people's cases. Thank you.

## How To Use
Clone or copy the code and run in python 3

```
RECEIPT_NUMBER_BASE: Your receipt number without the last N digits
RANGE_START: A smaller N digits integer as the end of receipt number to check start with
RANGE_END: A larger N digits integer as the end of receipt number to check end with
CASE_TYPE: Type of Form to filter, put 'Form' to show all types of forms
```

Please note that adjacent receipt number status may only be informative if you are filling with paper base, since each center is processing with different speed. And this information can be used as a reference of how soon will your case being processed, based on the consumptions that
1) Receipt number is increment based on receipt date, and 
2) Each USCIS center is processing by the receipt date


## Contact Me
For any further questions, or if you need help to run you receipt for you, please contact sunnyliyanbo@gmail.com
