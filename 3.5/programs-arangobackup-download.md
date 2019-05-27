---
layout: default
description: download hot backups to remote
---
Download a hot backup to remote
=============================

{% hint 'tip' %}
This functionality is only available with the enterprise
version. Currently `S3` endpoints are the only supported remote endpoint.
{% endhint %}

Hot backups can be downloaded to a remote `S3` repository:

```bash
arangobackup download --server.endpoint tcp://myserver:8529 --rclone-config-file /path/to/remote.json --identifier 2019-05-13T07.15.43Z_some-label --remote-path S3://remote-endpoint/remote-directory
```

This process may take as long as it needs to download the data from the
single server or all of the cluster's db servers to the remote
endpoint given network limitations thereto. 

The status of the download process may be acquired at any later time.

```bash
arangobackup download --server.endpoint tcp://localhost:9530 --rclone-config-file ~/remote.json --remote-path S3://remote-endpoint/remote-directory --status-id=1234
```