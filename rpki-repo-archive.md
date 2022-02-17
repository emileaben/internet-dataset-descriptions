# RPKI repo archive

The RPKI repo archive is at https://ftp.ripe.net/rpki/ 

The archive is structured as follows:
   * Subdirectory per trust anchor (XXX explain the APNIC situation)
   * Directories per day (XXX document structure)
 
##  Data Issues

There was an issue with syncing the APNIC data from XXX to XXX , which results in roughly half of the days having truncated data

Around October 2021 the data pipeline changed. Before this day rpki-validator-2 was used, after that day routinator 0.10.1 used.

The roa.csv file is missing from a large number of repos.

## Changelog
Dates are the date of the change in the processing. They are likely reflected started in the file that starts on the next day.

#### 2022-02-17:
`rrdp` is enabled. This should resolve the updates containing only partial data for APNIC.

**Resolves:** large fraction of days with partial data for APNIC

#### 2022-02-15:
The containers running the data collection job have IPv6 connectivity

#### 2021-10-01 (approximate):

Data collection switched from rpki-validator-2 to routinator 0.10.1.

  * routinator starts with a clean cache every day.
  * `rrdp` is not enabled (similar to rpki-validator-2).
  * The container running the job does not have IPv6 connectivity.

**Known issue:** A large fraction of the days has partial data for APNIC.
