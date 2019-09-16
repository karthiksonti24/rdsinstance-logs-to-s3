# rdsinstance-logs-to-s3
python script for storing rds instance logs to s3 bucket

## Getting Started

This script will collect all logs of rds instance with engine type postgres,aurora-postgresql and store them into a target s3 bucket. It is written in a format to run in multiple account environment and all the logs are stored inside a separate account where s3 is present.

- You can  either specify an single instance in a region or you can specify all the instances by giving '*'.
- When all the instances are specified it picks up only the instances of engine type postgres and aurora-postgresql.
- proxy(if you are running in a vpc, else not required) is enabled in this script to fetch sts credentials.


## Usage

It can run inside a jenkins, cron job, aws lambda.

- AWS Region
- AWS RDS Instance
- Cross Account Role(List of target accounts in which you have to get logs of rds instances)
- S3 Bucket Name 
- Source Account Role(for storing logs into the s3 source account)
