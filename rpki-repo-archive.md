# RPKI repo archive

The RPKI repo archive is at https://ftp.ripe.net/rpki/ 

The archive is structured as follows:
   https://ftp.ripe.net/rpki/TAL/YYYY/MM/DD/
with:
   * TAL : Trust anchor [1]
   * YYYY : Year
   * MM   : Month
   * DD   : Day

The individual daily directories per trust anchor contain 2 files:
   * repo.tar.gz : The raw repository content (as a tar-gzipped archive)
   * roas.csv    : The VRPs (Verified ROA Payloads) that were extacted from the PKI materials
 
##  Data Issues

There was an issue with syncing the APNIC data from XXX to XXX , which results in roughly half of the days having truncated data

Around October 2021 the data pipeline changed. Before this day rpki-validator-2 was used, after that day routinator was used.

The roas.csv file is missing from a large number of repos.

[1] For a while (from XXX to XXX) APNIC ran multiple trust anchors. For APNIC
