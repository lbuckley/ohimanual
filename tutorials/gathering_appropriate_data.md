# Gathering Appropriate Data


\*\* **Note: this page is under development**


* Goals:
    + which goals to include? 
    + how will the goals be weighted?
* Spatial scale:
    + what are the regions within the study area?
* Data:  
    + which data layers can be updated?
    + which data layers must be changed to develop new goal models?
* Goal models:
    + develop any goal models with the best available data
    


# Data Discovery and Acquisition: How to Gather Appropriate Data for the Ocean Health Index

The Ocean Health Index (OHI) spans disciplines and integrates diverse data and sources to give a comprehensive assessment of ocean health. A hallmark of the OHI is that it uses freely-available data to create models that capture the philosophy of individual goals, and finding appropriate data requires research and creativity. This document describes how to gather appropriate data, and provides examples.

OHI scores by goal are calculated at the scale of the reporting unit, which is called a **region** and then combined using a weighted average to produce the score for the overall area assessed, called a **study area**. 

Each data component that is included in the OHI is called a **data layer** because it will be combined with others to create the most complete picture of ocean health. Each data layer is scaled from 0-1 to be combined with others on the same unitless scale. This is true for all data used to model status, trend, pressures, and resilience.


## Data gathering responsibilities

Gathering appropriate data requires searching for and accessing freely-available data. It is important that team members responsible for data discovery make thoughtful decisions about whether data are appropriate for the regional assessment, and that they also get feedback from the full team to discuss the merits of different data sources. 

Data discovery and acquisition can be quite an iterative process, as there are both practical and philosophical reasons for including or excluding data, in addition to requiring access to the data. Practical considerations are discussed in ‘Requirements for data layers’, and philosophical considerations are introduced here and described more deeply in the Ocean Health Index Guide (available on ohi-science.org).

## The process of data discovery

In terms of philosophical considerations, the most important thing to remember when gathering data is that the data must contribute to measuring ocean health. Many data sources that enhance our knowledge of marine processes may not directly convey information about ocean health and may not be appropriate within the OHI framework. Because of this, compiled indicators can sometimes be more suitable than would raw data measuring single marine attributes.

Begin by understanding and comparing the best approaches used in assessments that have been completed, including global 2013, Brazil, and the US West Coast. If finer-resolution local data were available in the study area, they could be used either in a newly developed regional goal model using locally appropriate and informed approaches, or in the existing global goal model. When local data were not available, the same global-scale data were used with the original global goal model, which is least desirable because it does not provide more information than the global study. When looking for data, the following decision tree may be useful. This should be a goal-by-goal process:

>>> ![alt text(./fig/data_discovery.png)

Searching for data requires exploring data sources beyond any single discipline, and a good place to start is with an internet search. Internet searches can lead to published data in government and non-governmental organization reports, peer-reviewed articles, and masters and doctoral dissertations. Not everything will be freely available online but it is sometimes possible to request access.

It is good practice to keep detailed notes of attributes of each potential data layer, since there may be different options to work with. Searching for data by goal is a good approach, although some data layers will be used for multiple goals.

## Requirements for data layers

Four requirements to remember when investigating (or ‘scoping’) potential data layers are: relevance to ocean health, the reference point, spatial scale, and temporal scale. Each data layer must then be formatted in a specific way to be used by the OHI Toolbox App; (See: [formatting_data_for_toolbox](https://github.com/OHI-Science/ohimanual/blob/master/tutorials/formatting_data_for_toolbox.xlsx).

### 1.  Relevance to ocean health

There must be a clear connection between the data and ocean health, and determining this will be closely linked to each goal model.

### 2.  Reference point

Each data layer must be scaled to a reference point, and therefore when considering different data sources it is important to identify what a reasonable reference point may be. Ask the following types of questions as you explore data possibilities:
  * Is there a known relationship associated with these data?
  * Have policy targets been set regarding these data?
  * Would a historic target be appropriate?
  * Could a region within the study area be set as a spatial target?
  
### 3.  Appropriate spatial scale

Data must be available for every region within the study area.*

### 4.  Appropriate temporal scale

Data must be available for at least five years to calculate the trend. Longer time series are preferable because this can be used to set temporal reference points.*

It is not always possible to meet the spatial and temporal requirements with each data layer. In these cases it can still be possible to use these data if appropriate gap-filling techniques are used (see HowTo_FormatDataForToolbox, available from ohi-science.org). It is important that data satisfy as many of these requirements as possible, and in cases where creative ways of working with such data are not possible, it might be better to exclude these data from the analyses and try a different approach.


## Example: US West Coast data discovery

Below are examples of some decisions made when exploring available data for the US West Coast regional assessment. Determining whether certain data could be included started with a good understanding of the data layers and models included in the global assessment, and because the US West Coast is a data-rich region, finer-resolution local data could be used in place of many of the global data layers.

### Reasons data were excluded
There are a lot of existing data that contribute to our scientific understanding of ocean processes and interactions but that are not ideal for the OHI. Reasons to exclude data occur both on a practical level (do data adhere to the requirements above?) and on a philosophical level, which requires reflecting on the relationship with ocean health. Some common reasons for excluding data are listed below:

  * **The data do not cover the entire area of the reporting region**
The state of California had excellent, long-term data on public attendance at state parks that would have been quite useful in the calculation of the tourism and recreation goal. However, Oregon and Washington did not have these same data so they were could not be used.

  * **There is not a clear and scientifically proven connection between the metric described by the data and ocean health** 
Along the US West Coast, kelp beds are a very important habitat because of their contribution to biodiversity and coastal protection. However, kelp coverage is quite variable and is driven primarily by abiotic natural forcing (wave/storm disturbance and temperature) and thus kelp coverage is not a good metric of ecosystem health. For these reasons kelp coverage was not included in the assessment.

  * **The feature being measured may provide benefits to people, but this feature is not derived from the ocean**
Sea walls and riprap provide coastal protection to many people along the US West Coast. However, these structures are not a benefit that is derived from the ocean itself, so only biogenic habitats were included in the calculation of this goal. These data can be included as a pressure due to habitat loss.

  * **Data collection is biased and might misrepresent ocean health**
The US Endangered Species Act identifies a species list focused on species of concern within the US. As such, these data are biased since they assess only species whose populations may be in danger. For the calculation of the biodiversity goal, using these data would be inappropriate because this goal represents the status of all species in the region, not just those that are currently of conservation concern. Using these data may have shown the status of biodiversity to be lower than it really is because the selection of species to assess was already biased towards species of concern.

### Creative approaches to using data

  * Time series data are not long enough to calculate a trend or a reference point (when a historical reference point is most appropriate)
For the US West Coast, available data measure the current extent of seagrass habitats, however, these only exist for one time point in most areas so could not be used to calculate the trend or set a historical reference point. As these were the best data available for habitat coverage, we built a model to calculate the status and trend of seagrass habitats using other data that were available over time. A reasonable approach was to model the pressures exerted on seagrasses over time as a proxy for seagrass health.