# Cerner Stratum Paved Path Azure Templates

This Pipeline template is designed to dynamically move data from Oracle to Azure Data Lake.

The Pipeline is driven from a JSON file that needs to be staged on an Azure Storage Account. 

The format of the JSON file is of the following format. 

[
    {
        "SOURCE_SCHEMA_NAME": "**_SourceSchema_**",
        "SOURCE_TABLE_NAME": "**_SourceTable_**",
        "TARGET_FILE_PREFIX": "**_TargetFile_**",
        "TARGET_DIRECTORY": "**_TargetDirectory_**",
        "WHERE": "1=1",
        "Column_List": "*"
    },
    {
        "SOURCE_SCHEMA_NAME": "**_SourceSchema_**",
        "SOURCE_TABLE_NAME": "**_SourceTable_**",
        "TARGET_FILE_PREFIX": "**_TargetFile_**",
        "TARGET_DIRECTORY": "**_TargetDirectory_**",
        "WHERE": "1=1",
        "Column_List": "*"
    }
]

After the parameter file & Pipeline are deployed a trigger to run the pipeline with the same name as the parameter file must be created. The file extension “.json” should not be part of the trigger name. 