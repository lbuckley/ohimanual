# File System
This section describes the files within the ohi-[assessment] folder that you have accessed by either cloning through GitHub and RStudio or downloading to your computer from GitHub.

## Assessments and scenarios
Within the **ohi-[assessment]** folder is the **scenario** folder. The scenario folder contains all the data, functions and other files required to calculate the Ocean Health Index. To calculate the Index for a different region or with new data or models, you will modify the files within this folder (default data is from the global assessment).

In this example, **ohi-global** is the assessment folder and **eez2013** is the scenario.

### eez2013
Each of the elements (files and folders) within `ohi-global/eez2013` are critical to the proper functioning of the Toolbox. All .csv files can be read with text editors or with Microsoft Excel or similar software.

![alt text](./fig/ohiglobal_file_location.png)

### layers.csv
`layers.csv` is the registry that manages all data to be used in the Toolbox.

![alt text](./fig/layers_csv_registry.png)

Each row of information represents a specific data layer that has been prepared and formatted properly for the Toolbox. The first columns contain information inputted by the user; other columns are generated later by the Toolbox App as it confirms data formatting and content. The first columns have the following information:

 + **targets** indicates how the data layer related goals or dimensions. Goals are indicated with two-letter codes and sub-goals are indicated with three-letter codes, with pressures, resilience, and spatial layers indicated separately.
 + **layer** is the identifying name of the data layer, which will be used in R scripts like `functions.R` and .csv files like `pressures_matrix.csv` and `resilience_matrix.csv`. This is also displayed on the Toolbox App under the drop-down menu when the variable type is ‘input layer’.
 + **name** is a longer title of the data layer; this is displayed on the Toolbox App under the drop-down menu when the variable type is ‘input layer’.
 + **description** is further description of the data layer; this is also displayed on the Toolbox App under the drop-down menu when the variable type is ‘input layer’.
 + **fld_value** indicates the units along with the units column.
 + **units** some clarification about the unit of measure in which the data are reported
 + **filename** is the .csv filename that holds the data layer information, and is located in the folder ‘layers’.
 
 
### layers folder
The layers folder contains every data layer as an individual .csv file. The names of the .csv files within the layers folder correspond to those listed in the *filename* column of the 'layers.csv' file described above.

![alt text](./fig/layers_folder_location.png)

Note that each .csv file within the 'layers' folder has a specific format that the Toolbox expects and requires. Comma separated value files (.csv files) can be opened with text editor software, or will open by default by Microsoft Excel or similar software. 

Here is an example of proper data formatting using the file *cc_acid_2013.csv*. Note the unique region identifier ('rgn_id') with a single associated pressure_score, and that the data are presented in ‘long format’ with minimal columns. Please see [Download this tutorial](http://www.nceas.ucsb.edu/~jstewart/HowTo_FormatDataForToolbox_v1.xlsx) for further details and instructions on data formatting requirements.

![alt text](./fig/cc_acid_format_example.png)


### conf folder
This folder includes includes R functions (*config.R* and *functions.R*) and .csv files containing information that will be accessed by the R functions (*goals.csv*, *pressures_matrix.R*, *resilience_matrix.csv*, and *resilience_weights.csv*).

![alt text](./fig/layers_folder_location_conf.png)

+ **config.R** is an R script that configures labeling and constants appropriately.
+ **functions.R** contains functions for each goal and sub-goal model, which calculate the status and trend using data layers identified as ‘layers’ in layers.csv. 
+ **goals.csv** is a list of goals and sub-goals and their weights used to calculate the final score for each goal. Other information includes the goal description that is also presented in the Toolbox App. `goals.csv` also indicates the arguments passed to functions.R. These are indicated by two columns: *preindex_function* (functions for all goals that do not have sub-goals, and functions for all sub-goals) and *postindex_function* (functions for goals with sub-goals).  
+ **pressures_matrix.csv** describes the layers (‘layers’ column in layers.csv) needed to calculate pressure categories. The matrix has weights assigned that were determined by Halpern et al. 2012 (Nature) based on scientific literature and expert opinion.
+ **resilience_matrix.csv** describes the layers (‘layers’ column in layers.csv) needed to calculate resilience categories.
+ **resilience_weights.csv** describes the weight of various resilience layers, were determined by Halpern et al. 2012 (Nature) based on scientific literature and expert opinion.

### spatial folder 
The spatial folder contains a single file, *regions_gcs.js*. This is a spatial file in the GeoJSON format; it has the appropriate study area and regions for the assessment. This file will be created by the OHI team for all regional assessments.

### calculate_scores.R
This R script will run the Toolbox calculations using the .csv files in the *layers* folder that are registered in *layers.csv* and the configurations identified in *config.r*. Scores will be saved in *scores.csv*.

### scores.csv
**scores.csv** is a record of the calculated scores for the assessment (Global 2013 scores). Scores are reported for each dimension (future, pressures, resilience, score, status, trend) for each reporting region, and are presented in ‘long’ format. 
