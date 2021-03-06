---
title: Create a bucket
seotitle: Create a bucket in InfluxDB
description: Create buckets to store time series data in InfluxDB using the InfluxDB UI or the influx CLI.
menu:
  v2_0:
    name: Create a bucket
    parent: Manage buckets
weight: 201
---

Use the InfluxDB user interface (UI) or the `influx` command line interface (CLI)
to create a bucket.

## Create a bucket in the InfluxDB UI

1. Click **Load Data** in the navigation bar.

    {{< nav-icon "load data" >}}

2. Select **Buckets**.
3. Click **{{< icon "plus" >}} Create Bucket** in the upper right.
4. Enter a **Name** for the bucket.
5. Select when to **Delete Data**:
    - **Never** to retain data forever.  
    - **Older than** to choose a specific retention policy.
5. Click **Create** to create the bucket.

## Create a bucket using the influx CLI

Use the [`influx bucket create` command](/v2.0/reference/cli/influx/bucket/create)
to create a new bucket. A bucket requires the following:

- bucket name
- organization name or ID
- retention period duration (`ns`, `us`, `ms`, `s`, or `h`)

```sh
# Syntax
influx bucket create -n <bucket-name> -o <org-name> -r <retention-period-duration>

# Example
influx bucket create -n my-bucket -o my-org -r 72h
```
