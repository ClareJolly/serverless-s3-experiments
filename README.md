# Serverless S3 Experiments

To accompany my main serverless repo - [here](https://github.com/ClareJolly/serverless-offline-experiments)

---

## Contents <!-- omit in toc -->

- [Serverless S3 Experiments](#serverless-s3-experiments)
  - [Pre-requisites](#pre-requisites)
  - [Set up](#set-up)

---

## Pre-requisites

You can read about the local s3 plugin here - https://www.serverless.com/plugins/serverless-s3-local - I am using this guide for the most part (and added serverless-bundle)

- perhaps serverless `npm add -g serverless`
- aws cli

  - `aws configure --profile s3local`

    Add the credentials

    ```
    aws_access_key_id = S3RVER
    aws_secret_access_key = S3RVER
    ```

    You can try putting an object like this:

    ```
    aws --endpoint http://localhost:4569 s3 cp ~/tmp/data.csv s3://local-bucket/userdata.csv --profile s3local
    ```

---

## Set up

Clone the repo

- `yarn`

Note: for some reason I am having to run these commands with `sudo` - I need to look into why and alternative solutions

- start the s3 server `yarn start:s3`
- run lambda `yarn start`
