# Reasoning Analysis Team (RAT) documentation for RepliCATS project

An overview of the RAT repository. For details on the structure and process more generally,
see the [RAT Wiki](https://github.com/metamelb-repliCATS/RAT/wiki)

## Directory Structure

A (proposal for) the folders/sub-folder structure used to document the data collection and analysis conducted by RAT
based on a combination of recommended directory structure for a repository and the folder structure in repliCATS shared drive

### Archives RAT

Files prepared for archival in a public repository
- PhaseOne_ArchiveFiles
- PhaseTwo_ArchiveFiles

### Data Input

- PreparedData (source data prepared for analysis - including cleaned textual sources from the platform, interview transcriptions, etc.,).
- PrimaryData (including the source files we receive from the Data Management team, interview recordings etc.,).

### Data Analysis (e.g., documentation for qualitative methods, analysis, practices, etc.,)
- Analyst_calibrations
- Analyst_ICR_calculations
- Analyst_Training
- Codebooks
- NVivo_Exports
- Queries

### Data Management
- KnownClaims
- ScoreClaims

### Data Outputs RAT

### Figures
- Copies of data visualisation - figures, tables, graphs, etc.,

### Scripts

- Scripts written for processing RAT data with R

## Additional Notes

### Repository External Integrations

This repository is linked with the RAT board of the repliCATS project management software (Monday) through the following automated processes:

#### Monday

- When pull request is opened in _RAT_ (on github), create an _item_ (in the Data Management group of the team board on Monday) and sync future changes from GitHub
- When an issue is created in _RAT_, create an _item_ (in the Data Management group) and sync future changes from GitHub
- When an item id is mentioned in a commit to _RAT_, create an update to the relevant item
- When a comment is created on an issue of _RAT_, create an update in the connected item
- When _Status_ changes to _open_ (in Monday Team board) create an issue in _RAT_(on github).

#### Local Devices

- Integration with git local repositories via including RAT as a remote repository, creating pull-requests for updates.

