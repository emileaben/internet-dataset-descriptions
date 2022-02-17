# RPKI repo archive

The RPKI repo archive is at https://ftp.ripe.net/rpki/ 

The archive is structured as follows:
   * Subdirectory per trust anchor (XXX explain the APNIC situation)
   * Directories per day (XXX document structure)
 
##  Data Issues

There was an issue with syncing the APNIC data from XXX to XXX , which results in roughly half of the days having truncated data

On XXX the data pipeline changed. Before this day rpki-validator-2 was used, after that day routinator was used.

The roa.csv file is missing from a large number of repos.
