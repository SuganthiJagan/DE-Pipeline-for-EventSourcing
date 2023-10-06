## Python dbt-Redshift project
## TASKS: 

### Data Ingestion
Data ingestion is done using Python and can be found under load_data folder.
JSON events in "events.jsonl.bz2" are loaded as pandas dataframe. Then the data is ingested to Redshift Database through "load_dataset_to_redshift.py"

### Data Transformation
Data Transformation is done using dbt and can be found under transformed_data/models folder.
- staging: Intermediate data transformations are created as views
- marts:   Final analytics tables are created as a_device_session.sql, b_school_session.sql, c_device_usage_history.sql, and d_master_school.sql files respectively

### Basic Statistics
From the four final tables, some basic descriptive statistics are derived as,
- Total number of devices: 65
- Total number of schools: 55
- Total number of sessions: 1136

## Note:
**dbt_run_artifacts** directory is managed by Github Actions Workflow so **do _not modify_**. This directory stores the dbt state file.

#### Contributors
Suganthi Jaganathan (September, 2023 -) - @SuganthiJagan

#### Maintainers
Suganthi Jaganathan - @SuganthiJagan
