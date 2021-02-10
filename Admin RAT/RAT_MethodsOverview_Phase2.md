# Documenting Qalitative Methods for the repliCATS project
(Phase 2, 2020 - 2022)

## Introduction / Context
This document follows on from the [documentation in Phase 1](https://docs.google.com/document/d/1TFhaIv8YKr9xwT5fN_R3SKfFPBTzax5P/edit#) as an in-progress record of our approaches to collecting and analysing textual within the repliCATS project (formatted by actual approaches taken, with any circumstances where these differ from those planned included along with relevant literature informing these decisions).

## Data Collection
## Data Inputs
## Data Formatting
## Data Management
The Tech-Team use PostgreSQL (Version 9.6) for their database management, so to access the back-up databases shared with us we need to use this as well. Once the databases are unzipped and openned on PostgreSQL, we should be able to connect to them from R-Studio to integrate when query / run any scripts on those database-backups with the rest of the analysis. 

A backup of the Phase1 database is stored (in a compressed form) in the [RepliCATS-Database-Backup_repository](https://github.com/metamelb-repliCATS/RepliCATS-Database-Backup) 
When shared, the database backups for Phase 2 will also be stored here (note that there may be two databases - one for single-trace claims and one for bushel-claims)

The Data-Management-Team is refining the data-processing pipeline for the project as a whole (so RAT may not need to access to databases directly, tbc). 

Within RAT, we expect to have two distinct data-processing needs for Phase 2 across ~6 different data-pipelines: 
a) A process of manually-coding the free-text responses  (using a refined Codebook, V11-tbc), for: 
1. phase1-claims
2. single-claims
3. bushel-claims
4. A process for analysing the manually-coded free-text responses from across both Phase 2 (single-trace & bushel claims) and Phase 1. 
b) A process for auto-coding the free-text responses (using a refined reasonWAgg Codebook, V6 -tbc) and extracting the code-application counts per-participant/per-claim/per-node, for both:
5. single-claims 
6. bushel-claims

### Troubleshooting:
- Given the databases for single-trace-claims and bushel-claims are seperate, combined analyses will be more difficult and, unless crucial for existing research questions, should be avoided.  
- 

## Data Analysis
### Approach to Qualitative Analysis (literature review)
### Analyst Training
### Analyst Calibration
### Analyst ICR Calculations
### Codebooks
## Data Outputs
## Troubleshooting
## Project Outputs
