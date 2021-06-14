# ArcGIS Describe Geodatabase
Python toolbox for describing the structure of an ArcGIS geodatabase. Forked from https://github.com/MichaelTroyer/ArcGIS_Describe_Geodatabase.
Python 3 code updated to run in ArcGIS Pro 2.7+.
Replaced dependency on [Python csv module](https://docs.python.org/3/library/csv.html) with [pandas.DataFrame.to_csv](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.to_csv.html). Use of pandas DataFrame intended to allow for further extension.

## Purpose:
### Write geodatabase structural details to comma-separated text file. Python 3-based replacement for some functionality of [X-Ray for ArcCatalog](https://www.arcgis.com/home/item.html?id=9ea218ff575f4a5195e01a2cae03a0ae), which is only available for ArcGIS 10.x.

    Will create a unique .csv table for each table or feature class in a database detailing for each field:
        * name
        * type
        * length
        * aliasName
        * domain
        * defaultValue
        * isNullable
        * required
        * editable
        * precision
        * scale
        * unique record count
        
    Will create a unique csv for each domain
    
    Will create a csv detailing all the relationship classes in a database:
        * relationshipClassName
        * originClassName
        * destinationClassName
        * originClassKey
        * destinationClassKey
        * forwardPathLabel
        * backwardPathLabel
        * cardinality
        * classKey
        * keyType
        * isAttachment
        * isAttributed
        * isComposite
        * isReflexive
        * notification

## To Do:

- Feature Dataset & Feature Class properties (joined with attribute table for presentation)
- Topology properties
- Geometric network properties
- Raster properties
- Export to HTML (X-Ray for ArcCatalog data dictionary replacement)
