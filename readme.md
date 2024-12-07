# ZFS backup tool

Incremental local backup with encrypted zfs volumes.

```
# ./backup2 --init --from from/dataset --to to/dataset
...

# ./backup2 --from from/dataset --to to/dataset
...

# ./backup2 --from from/dataset --to to/dataset
...

$ zfs list -r -t all from/dataset
NAME                                       USED  AVAIL     REFER  MOUNTPOINT
from/dataset                               265G   132G      250G  -
from/dataset@backup2-2024-12-07T07-53-23  71.8M      -      250G  -
from/dataset@backup2-2024-12-07T09-03-25  61.7M      -      250G  -

$ zfs list -r -t all to/dataset
NAME                                     USED  AVAIL     REFER  MOUNTPOINT
to/dataset                               264G  1.18T      250G  -
to/dataset@backup2-2024-12-07T07-53-23  71.5M      -      250G  -
to/dataset@backup2-2024-12-07T09-03-25     0B      -      250G  -
```
