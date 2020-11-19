# Reasoning Analysis Team (RAT) documentation for RepliCATS project

set-up in progress

## Directory Structure

The documentation for the data collection and analysis conducted by RAT under the following folders/sub-folder system:

### Archives

- Files prepared for archival in a public repository

### Data

- PrimaryData (including the source files we receive from the Data Management team, interview recordings etc.,).
- PreparedData (source data prepared for analysis - including cleaned textual sources from the platform, interview transcriptions, etc.,).
- Data Management (records of processes used for managing data within RAT). 

### Docs (Text Documents)

- Admin (e.g., meeting notes, timelines, etc.)
- Records (e.g., process documentation for methods, analysis, project decisions and practices, etc.,)
- Manuscripts (e.g., paper drafts)
- Reports

### Figures

- Copies of data visualisation - figures, tables, graphs, etc.,

### Scripts

- Scripts written for processing RAT data with R

## Additional Notes

### Repository External Integrations

This repository is linked with the RAT board of the repliCATS project management software (Monday) through the following automated proccesses:

#### Monday

- When pull request is opened in _RAT_ (on github), create an _item_ (in the Data Management group of the team board on Monday) and sync future changes from GitHub
- When an issue is created in _RAT_, create an _item_ (in the Data Management group) and sync future changes from GitHub
- When an item id is mentioned in a commit to _RAT_, create an update to the relevant item
- When a comment is created on an issue of _RAT_, create an update in the connected item
- When _Status_ changes to _open_ (in Monday Team board) create an issue in _RAT_(on github).

#### Local Devices

- Integration with git local repositories via including RAT as a remote repository, creating pull-requests for updates.
