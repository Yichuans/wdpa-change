# Description

Check differences including additions, deletions and changes at field level, between any two WDPA versions. It produces a table of 'update', 'change' and 'delete' for all records (in the case of 'update', each attribute value change is picked up).

## Get started

1. Download and unzip the content in `release` in a folder of your choosing.
1. Open a (non-empty / empty) project in ArcGIS Pro.
1. On the ribbon, select Insert --> Toolbox --> Add Toolbox.
1. Go to the folder where you unzipped, select the `.tbx` file (with red icon), and press 'OK'.
1. Open the Catalog pane --> Toolboxes --> The WDPA QA toolbox should now be visible.
1. Expand the toolbox, so that the embedded scripts become visible.
   
1. Right-click the script to run (e.g. for polygons or points), click Open, and specify the two input Feature Layers and change the output to be a CSV file (so that you can open in Excel by default)
1. Click Run, and click 'View Details' if you wish to see the progress.
    
## Console use

It can be run as a standalone script.

Find `Python Command Prompt` from your windows search (should be in your ArcGIS Pro installation) this is to ensure the Python envoked can see libraries such as `arcpy`.

Change directory to the place where `check_wdpa_update.py` is located.

```bash
python check_wdpa_update.py {old_data_path} {new_data_path} {output_csv_file_path)
```
where `old_data_path` is the base WDPA dataset to compare against, `new_data_path` the new WDPA dataset, and `output_csv_file_path` the output csv full path. Please ensure the path does not have any space in the file name. If not, make sure you enclose the whole input path with quotes (`"`). 

An example of the syntax

```bash
(arcgis-pro-py3) c:\users\yichuans\WDPA>python check_wdpa_updates.py E:\WDPA_Dec2016_Public.gdb\WDPA_point_2016 "E:\WDPA_2017_Public.gdb\WDPA point 2017"
```
