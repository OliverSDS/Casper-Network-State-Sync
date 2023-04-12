# Casper Network Data Download Instructions
This repository provides instructions on how to download the Casper network data snapshot and place it in the appropriate directory. The snapshot was taken on April 1, 2023 at 12:46:40 UTC.

## Requirements
The wget command-line utility must be installed on your system.
## Instructions
- Open a terminal window.

- Navigate to the directory where you want to download the snapshot.

- Run the following command to download the snapshot:

``` wget https://caspernetwork.live/casper.tar.gz ```

- Once the download is complete, navigate to the Casper node directory:

``` cd /var/lib/casper/casper-node/ ```
- Extract the downloaded archive by running the following command:

``` tar -xzf /path/to/downloaded/casper.tar.gz ``` <br>
Note: Replace /path/to/downloaded/casper.tar.gz with the actual path to the downloaded archive.

- The snapshot is now ready to use in the Casper network.

License
This repository is licensed under the MIT License. See LICENSE for more information.
