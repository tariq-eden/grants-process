# RAT
Repository for the Reasoning Analysis Team within the RepliCATS project

Project set-up in progress.

## Directory Structure
This repository collects the documentation for the data collection and analysis conducted by RAT under the following folders/sub-folder system:

### Data 
- PrimaryData (including the source files we recieve from the Data Management team - Raw data from the platfom is stored on their team repository). 
- CleanedData (source data prepared for analysis - including both platform textual data and any other textual sources such as interviews). 

### Docs (Text Documents)
- Admin (e.g., meeting notes, timelines, etc.)
- Records (e.g., process documentation for methods, analysis, project decisions and practices, etc.,)
- Manuscipts (e.g., paper drafts)
- Reports 

### Figures 
- Copies of data visualisation - figures, tables, graphs, etc., 

### Scripts  
- Any scripts written in R for processing RAT data 

## Repositoary Exteranl Integrations 
This repository is linked with the RAT board of the repliCATS project management software (Monday) through the following automated proccesses: 
### GitHub changes to Monday 
- When pull request is opened in *RAT*, create an *item* (in the Data Management group) and sync future changes from GitHub
- When an issue is created in *RAT*, create an *item* (in the Data Management group) and sync future changes from GitHub
- When an item id is mentioned in a commit to *RAT*, create an update to the relevant item
- When a comment is created on an issue of *RAT*, create an update in the connected item

