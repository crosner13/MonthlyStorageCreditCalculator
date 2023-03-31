
# Overview
This calculator is used to find the amount of storage credits items, users, and groups use on a monthly basis in an ArcGIS Online organization. 

## Instructions
The user should clone this repo to their computer, open a project in ArcGIS Pro, and add this notebook to the project. This will ensure that the user has access to Esri's arcgis.gis module, which comes pre-packaged in the default Python environment and is only available with an install of ArcGIS Pro. 

User can then log in with their ArcGIS Online organization credentials, define the function, and then specify if they want to calculate the monthly storage costs of items, users, and/or groups. 

## Known Issues
- File path for output CSV files is specified in relevant code blocks, but should be defined earlier elsewhere.
- Item sizes and credit costs are rounded to the third decimal point. This was originally done in the hopes that it would speed up calculation time; unsure if exact precision is needed.
- Numeric type is float; unsure if exact precision is needed
- Trying to calculate credit costs for items that are actively being edited (such as Survey123 result feature layers) in other applications lead to wildly inflated credit cost estimations. Running the calculator when those items are not being edited returns the numbers back to normal.
- Views of hosted feature layers are automatically assigned costs of zero, but unsure if this is actually the case
