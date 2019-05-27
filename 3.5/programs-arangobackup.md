---
layout: default
description: arangobackup is a command-line client tool to create a global hot backups of an ArangoDB instance
---
Arangobackup
============

_Arangobackup_ is a command-line client tool which creates global hot
backups of the data and structures stored in ArangoDB.

Hot backups rely on hard link magic performed on the database's
persistence layer.

_Arangobackup_ can be used for all ArangoDB deployments modes (Single
Instance, Active Failover, and Cluster). It always creates what
is most readily described as a persistence layer consistent snapshot
of the entire instance. Therefore, no such thing as database or
collection level hot backups exist. Consequently, unlike with
_arangodump_/_arangorestore_, one may only restore a hot backup set to
the same layout. One can only restore a single server hot backup to a
single server instance and a 3 db server cluster's hot backup to a 3
db server instance.
If you are using the Enterprise Edition, snapshots can be uploaded to
or downloaded from remote S3 mount points. 