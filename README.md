# RAT Repository

Repository for the Reasoning Analysis Team within the RepliCATS project

Project set-up in progress.

## Directory Structure

This repository collects the documentation for the data collection and analysis conducted by RAT under the following folders/sub-folder system:

### Archives

- Files prepared for archival in a public repository

### Data

- PrimaryData (including the source files we receive from the Data Management team - Raw data from the platform is stored on their team repository).
- CleanedData (source data prepared for analysis - including both platform textual data and any other textual sources such as interviews).

### Docs (Text Documents)

- Admin (e.g., meeting notes, timelines, etc.)
- Records (e.g., process documentation for methods, analysis, project decisions and practices, etc.,)
- Manuscripts (e.g., paper drafts)
- Reports

### Figures

- Copies of data visualisation - figures, tables, graphs, etc.,

### Scripts

- Any scripts written for processing RAT data (e.g. R scripts)

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
