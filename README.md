# EDS223 Homework 2: Redlining in LA County

This repository contains the response to Homework 2 in EDS223 - *Geospatial Analysis & Remote Sensing*, completed by Sofia Sarak.

The assignment explores historically redlined districts in Los Angeles County, California. It incorporates spatial data on the "residential security" grades assigned by the Home Owners’ Loan Corporation (HOLC) about eighty years ago. More information on the economic and racial segregation that came from this grading system, and redlining, can be found [here](https://ncrc.org/holc/). 

The analysis in this repository includes a spatial visualization of HOLC grades across LA, visualizations comparing environmental justice indicators across the grades, and a visualization exploring bird biodiversity and percentages associated with observation contribution, also by grade. These results are then summarized and reflected on in responses.

For more information on the homework assignment itself, reference the [assignment description](https://eds-223-geospatial.github.io/assignments/HW2.html).

## Data Source

Our environmental justice data comes from the United States Environmental Protection Agency’s former EJScreen: Environmental Justice Screening and Mapping Tool. This tool is no longer operating, but an [unofficial version](https://pedp-ejscreen.azurewebsites.net/) is still running. EJScreen provided environmental and demographic information for the US at the Census tract and block group levels; in this analysis, block group level data was used and was downloaded from the [EPA site](https://www.epa.gov/ejscreen/download-ejscreen-data). 

Digitized maps and information on the HOLC classification system were created by the [Digital Scholarship Lab](https://dsl.richmond.edu/) at the University of Richmond as part of the [Mapping Inequality project](https://dsl.richmond.edu/panorama/redlining/#loc=5/39.1/-94.58) (and was downloaded from their [website](https://dsl.richmond.edu/panorama/redlining/#loc=5/39.1/-94.58&text=downloads)).

Biodiversity data was sourced from the [Global Biodiversity Information Facility](https://eds-223-geospatial.github.io/assignments/gbif.org), which is the largest aggregator of biodiversity observations in the world. The data set typically includes the species and the location and date that it was observed. This analysis uses data from 2021 onward.

*Information on data sources was retrieved from original assignment description.*

## Repository Structure
```
├── data
│   ├── ejscreen
│   │   ├── EJSCREEN_2023_BG_Columns.xlsx
│   │   ├── EJSCREEN_2023_BG_StatePct_with_AS_CNMI_GU_VI.gdb
│   │   │   ├── a00000001.freelist
│   │   │   ├── a00000001.gdbindexes
│   │   │   ├── a00000001.gdbtable
│   │   │   ├── a00000001.gdbtablx
│   │   │   ├── a00000001.TablesByName.atx
│   │   │   ├── a00000002.gdbtable
│   │   │   ├── a00000002.gdbtablx
│   │   │   ├── a00000003.gdbindexes
│   │   │   ├── a00000003.gdbtable
│   │   │   ├── a00000003.gdbtablx
│   │   │   ├── a00000004.CatItemsByPhysicalName.atx
│   │   │   ├── a00000004.CatItemsByType.atx
│   │   │   ├── a00000004.FDO_UUID.atx
│   │   │   ├── a00000004.freelist
│   │   │   ├── a00000004.gdbindexes
│   │   │   ├── a00000004.gdbtable
│   │   │   ├── a00000004.gdbtablx
│   │   │   ├── a00000004.horizon
│   │   │   ├── a00000004.spx
│   │   │   ├── a00000005.CatItemTypesByName.atx
│   │   │   ├── a00000005.CatItemTypesByParentTypeID.atx
│   │   │   ├── a00000005.CatItemTypesByUUID.atx
│   │   │   ├── a00000005.gdbindexes
│   │   │   ├── a00000005.gdbtable
│   │   │   ├── a00000005.gdbtablx
│   │   │   ├── a00000006.CatRelsByDestinationID.atx
│   │   │   ├── a00000006.CatRelsByOriginID.atx
│   │   │   ├── a00000006.CatRelsByType.atx
│   │   │   ├── a00000006.FDO_UUID.atx
│   │   │   ├── a00000006.freelist
│   │   │   ├── a00000006.gdbindexes
│   │   │   ├── a00000006.gdbtable
│   │   │   ├── a00000006.gdbtablx
│   │   │   ├── a00000007.CatRelTypesByBackwardLabel.atx
│   │   │   ├── a00000007.CatRelTypesByDestItemTypeID.atx
│   │   │   ├── a00000007.CatRelTypesByForwardLabel.atx
│   │   │   ├── a00000007.CatRelTypesByName.atx
│   │   │   ├── a00000007.CatRelTypesByOriginItemTypeID.atx
│   │   │   ├── a00000007.CatRelTypesByUUID.atx
│   │   │   ├── a00000007.gdbindexes
│   │   │   ├── a00000007.gdbtable
│   │   │   ├── a00000007.gdbtablx
│   │   │   ├── a00000039.freelist
│   │   │   ├── a00000039.gdbindexes
│   │   │   ├── a00000039.gdbtable
│   │   │   ├── a00000039.gdbtablx
│   │   │   ├── a00000039.horizon
│   │   │   ├── a00000039.I49AREALAND_1.atx
│   │   │   ├── a00000039.I49AREALAND.atx
│   │   │   ├── a00000039.I49AREAWATER.atx
│   │   │   ├── a00000039.I49ID.atx
│   │   │   ├── a00000039.spx
│   │   │   ├── EJSCREEN - Shortcut.lnk
│   │   │   ├── gdb
│   │   │   └── timestamps
│   │   └── ejscreen-tech-doc-version-2-2.pdf
│   ├── gbif-birds-LA
│   │   ├── gbif-birds-LA.dbf
│   │   ├── gbif-birds-LA.prj
│   │   ├── gbif-birds-LA.shp
│   │   └── gbif-birds-LA.shx
│   └── mapping-inequality
│       └── mapping-inequality-los-angeles.json
├── eds223-homework2.Rproj
├── HW2.pdf
├── HW2.qmd
└── README.md
```

## Course Information

-   **Course Title:** [EDS 223 - Geospatial Analysis & Remote Sensing](https://eds-223-geospatial.github.io/)
-   **Term:** Fall 2025
-   **Program:** [UCSB Masters in Environmental Data Science](https://bren.ucsb.edu/masters-programs/master-environmental-data-science).

Teaching Team:

-   **Instructor:** [Annie Adams](https://github.com/annieradams)
-   **Teaching Assistant:** Alessandra Vidal Meza

Complete materials for the discussion sections and additional resources can be found on the [course website](https://eds-223-geospatial.github.io/).

*This README was adapted from the README template provided in EDS220; see course details and original repository [here](https://github.com/sofiasarak/eds220-2025-in-class).*
