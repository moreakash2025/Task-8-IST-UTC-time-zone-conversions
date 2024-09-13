# Task-8-IST-UTC-time-zone-conversions


PySpark Timezone Conversion
This project demonstrates how to perform timezone conversion using PySpark. The code converts timestamp data from UTC to IST (Indian Standard Time) and shows how to work with timezones in a Spark DataFrame.

Requirements
Apache Spark (version 3.0 or later)
PySpark
Java (JDK 8 or higher)
Project Overview
This PySpark application reads a dataset containing timestamp data, converts the timestamps to two different timezones: UTC and IST, and displays the converted times.

Key Functions:
to_utc_timestamp: Converts the timestamp to UTC.
from_utc_timestamp: Converts a UTC timestamp to another timezone (in this case, IST).
Dataset
The dataset used in this project is a list of timestamp values. The schema of the DataFrame consists of:

id: Identifier for the record.
date: The timestamp in string format (YYYY-MM-DD HH:MM:SS).
Sample Data:
id	date
1	2024-09-06 08:00:00
2	2024-09-06 09:00:00
...	...
50	2024-09-08 09:00:00
Code Overview
Spark Session: Initializes a Spark session using SparkSession.builder().

DataFrame Creation: A DataFrame is created using a predefined list of timestamp values.

Schema Definition: The DataFrame schema is automatically inferred from the data.

Timestamp Conversion:

The date column is converted to a timestamp type.
The timestamp is then converted to UTC using to_utc_timestamp.
IST conversion is done using from_utc_timestamp with the Asia/Kolkata timezone.
Output: The resulting DataFrame includes three columns:

Original date
Converted UTC time
Converted IST time
