# Data Kit - Alternative Fuel Stations

## Version

Current version: 2026-03-26

## Provider

  - Organization: [Mid-Ohio Regional Planning Commission](https://morpc.org)
  - Contact: 
    - Name: Adam Porr
	- E-mail: aporr@morpc.org
	- Phone: 614-233-4216

## Introduction

The [Alternative Fuels Data Center](https://afdc.energy.gov/) (a division of the U.S. Dept. of Energy) maintains a database containing the locations and attributes of alternative fuel stations. This data kit includes a summary of alternative fuel stations openings by geography by year for the MORPC 15-county region.  The geography levels include incorporated places, non-incorporated townships, counties, and the region as a whole.

## Outputs

This data kit includes a long form table in CSV format (see `./output_data/altfuelstations_long.csv`) which provides a count of station openings indexed by geographic identifier, year, and fuel type.
  
The data is accompanied by a [Frictionless Resource file](https://specs.frictionlessdata.io/data-resource/), which provides a high-level description of the data and a link to the associated table schema.  The Resource file also provides the [MD5 checksum](https://en.wikipedia.org/wiki/Md5sum) ("hash") and the file size ("bytes") of the data file to allow for integrity checking.

The table schema is described by a [Frictionless Schema file](https://specs.frictionlessdata.io/table-schema/), which describes each of the fields contained in the table, including its name and type, and sometimes provides additional metadata about the table.

## Processes

The output table is is produced by a [Jupyter notebook](https://jupyter.org/) (see `./insights-altfuelstations.ipynb`).

The process is fully automated, but depends on outputs from several upstream processes.

## Inputs

The process requires the following inputs:

  1. Summarized data for the alternative fuel stations, which is produced by upstream process [morpc-altfuelstations-summarize](https://github.com/morpc/morpc-altfuelstations-summarize). See `./input_data/morpc-altfuelstations-all-long.csv` for the snapshot of the input data used to produce the current output.
  1. MORPC standard geographies lookup table, which is produced by upstream process [morpc-geos-collect](https://github.com/morpc/morpc-geos-collect)
  
Note that access to some of the upstream content is restricted to MORPC staff.

## Revision history

Revisions are listed in reverse chronological order.

### 2026-03-26 Adam Porr <aporr@morpc.org>

Incorporate upstream data through 2025. Include charts for Central Ohio communities who are not MORPC members. Other minor improvements to code and documentation.

### 2025-02-22 Adam Porr <aporr@morpc.org>

Initial release.
