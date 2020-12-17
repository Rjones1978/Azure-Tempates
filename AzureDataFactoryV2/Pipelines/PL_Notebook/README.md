# Cerner Stratum Paved Path Azure Templates

This Pipeline template is designed to dynamically run any number of Databrick Notebooks in parallel.

The Pipeline is driven from a JSON file that needs to be staged on an Azure Storage Account. 

The format of the JSON file is of the following format. 

[
    {
        "NOTEBOOK_PATH": "WORKSPACEPATH"
    },
    {
        "NOTEBOOK_PATH": "WORKSPACEPATH"
    }
]

After the parameter file & Pipeline are deployed a trigger to run the pipeline with the same name as the parameter file must be created. The file extension “.json” should not be part of the trigger name. 