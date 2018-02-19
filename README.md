# Sample ETL Data Job

This is a companion project for the post [ETL Job Processing with Serverless and AWS Redshift]().

## Pre-requisites

Setting up AWS Redshift is out of scope of this sample, but we need one set up to dump data into it from our ETL job. Once you have it set up and configured, keep the cluster endpoint in Redshift handy, as we will need it later to configure the database connection string.

### Redshift cluster endpoint

`<cluster_name>.xxxxxxxxxxxx.<region>.redshift.amazonaws.com:<port>`

### DB Connection String

`postgres://<username>:<password>@<hostname>:<port>/<db_name>`
where `<hostname>:<port>` is the cluster endpoint

## Install dependencies

`$ pip install -r requirements.txt`

## Install plugins

`$ sls plugin install -n serverless-python-requirements`

This will install the plugin and will add the `plugins` section in the `serverless.yml` file.

## Run locally

`sls invoke local -f etlSample`

## Run

`sls invoke -f etlSample`
