---
title: Cellar add-on
position: 3
shortdesc: Cellar is a Amazon S3-compatible file storage system created and hosted by Clever Cloud.
tags:
- addons
keywords:
- S3
- amazon
- Storage
- file
- files
---

# Cellar <span class="cc-beta pull-right" title="Currently in private Beta version"></span>

<div class="panel panel-warning">
  <div class="panel-heading">
    <h4 class="panel-title">Note for Beta Version</h4>
  </div>
  <div class="panel-body">
    Cellar is currently in private Beta. If you want to use it, please send a mail at support@clever-cloud.com<br />
  Cellar is free during the beta period with a fair use at 20 GB. No credits wil be charged during the beta period,
  and under the fair use.
  </div>
</div>

Cellar is S3-compatible online file storage web service. You can use it with
your favorite S3 client.

To manually manage the files, you can use [s3cmd](http://s3tools.org/s3cmd).
You can download a s3cmd configuration file from the add-on configuration
page.

## Creating a bucket

In Cellar, files are stored in buckets. When you create a Cellar addon, no
bucket is created yet.

To create a bucket, you can use s3cmd:

```bash
    s3cmd mb s3://bucket-name
```
You can list files

```bash
    s3cmd ls s3://bucket-name
```

You can upload files (`--acl-public` makes the file readable by everyone).

```bash
    s3cmd put --acl-public image.jpg s3://bucket-name
```

<div class="panel panel-warning">
  <div class="panel-heading">
    <h4 class="panel-title">S3 signature algorithm</h4>
  </div>
  <div class="panel-body">
    Cellar doesn't support the `v4` signature algorithm from S3. Please make sure
    your client is configured to use the `v2` signature algorithm. The
    s3cmd configuration file provided on the add-on configuration page already has it.
  </div>
</div>