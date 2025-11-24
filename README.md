# CodeSamples

This repository contains two different code samples. The first, `VehicularAccidents_311ServiceRequestAnalysis`, adapts work I completed for a final project in my master’s program. The second folder, `CapstoneDataProcessing`, is the core of my code for my capstone project, which is still in progress as of November 2025.  

Together, these notebooks show how I work end to end with messy public-sector data: acquiring and cleaning datasets, joining across sources, building features, doing exploratory analysis, and organizing code in a way that is easy for others to follow.

---

## VehicularAccidents_311ServiceRequestAnalysis

#### NYC Accidents & 311 Complaints.ipynb

**Overall goal**  
Explore how New York City vehicular accidents and 311 service complaints line up in space and time, to see where traffic safety issues and resident-reported problems overlap.

**What this notebook does**  
1. Loads open data on motor vehicle collisions and 311 complaints for New York City.  
2. Cleans and standardizes fields such as dates, times, locations, and complaint categories.  
3. Joins and aggregates the datasets by location and time (for example, neighborhood or borough and time of day).  
4. Builds features that describe accident patterns and complaint patterns, such as counts, rates, and complaint types.  
5. Uses charts and tables to highlight hotspots and possible relationships between accidents and specific 311 complaint categories.

**Skills showcased**  
1. Working with real-world city open data in Jupyter.  
2. Data cleaning and feature engineering on multi-source datasets.  
3. Joining and aggregating data across time and geography.  
4. Exploratory data analysis and clear visualization to tell a story around safety and service delivery.

---

## CapstoneDataProcessing (PROJECT IN PROGRESS)

The notebooks in this folder support my capstone project, which looks at the relationship between urban trees and building energy performance in New York City. The focus is on building a reliable, analysis-ready dataset from multiple open data sources. NOTE: This project is currently in progress, and has been simplified to serve a sample. However, it still is a bit rough.

#### BuildingWork_Part1.ipynb

**Overall goal**  
Create a building-level panel dataset of New York City energy and water benchmarking results that can be linked to building geometry and later joined to tree canopy measures.

**What this notebook does**  
1. Pulls several years of Local Law 84 benchmarking data for New York City buildings.  
2. Cleans and standardizes building identifiers across years, including handling missing or inconsistent IDs.  
3. Geocodes buildings and assigns them to tax lots and building footprints.  
4. Joins in additional building attributes such as zoning, height, and other physical characteristics.  
5. Outputs a consistent building-level file that is ready for downstream spatial analysis and modeling.

**Sources used in this notebook include**  
1. New York City Open Data building energy and water disclosure datasets for Local Law 84 (multiple years).  
2. New York City Open Data building historic records.  
3. New York City Open Data building elevation and subgrade data.  
4. New York City Planning MapPLUTO building footprint and tax lot data.  
5. New York City Planning tree canopy change data derived from LIDAR.  
6. New York City Planning Labs geosearch service for address cleaning and geocoding.

**Skills showcased**  
1. Building robust ETL pipelines for large civic datasets.  
2. Cleaning and reconciling multi-year records at the building level.  
3. Basic geospatial processing and joining tabular data to spatial layers.  
4. Preparing high-quality, reusable datasets for analysis.

---

#### TreeWork_Part2.ipynb

**Overall goal**  
Construct a tree-level dataset that tracks which street trees exist in each year and when they are removed, based on inventory and work order records.

**What this notebook does**  
1. Loads New York City street tree inventory data and forestry work order records from open data.  
2. Cleans and aligns tree identifiers, locations, and key fields across the two datasets.  
3. Uses work order histories to infer tree removal dates and statuses.  
4. Restricts analysis to closed tickets to ensure reliable outcomes.  
5. Builds a yearly tree-level file that can be joined to nearby buildings for panel analysis.

**Sources used in this notebook include**  
1. New York City Open Data street tree inventory and point location data.  
2. New York City Open Data tree work order and forestry service request records.  
3. New York City Open Data geographic reference layers for streets and neighborhoods.  
4. New York City planning and open data portals for reference building and location context.

**Skills showcased**  
1. Working with operational city data that is noisy and event based.  
2. Designing rule-based logic to infer entity status over time (for example, whether a tree is still present).  
3. Combining event histories with inventory data to build panel-style datasets.  
4. Preparing features that can be linked to other spatial units such as buildings.

---

#### Analysis_Part3.ipynb

**Overall goal**  
Bring together the building and tree datasets from Parts 1 and 2 to study how changes in tree canopy relate to building energy performance. This analysis is in progress for this semester.

**What this notebook does**  
1. Merges the building-level dataset with nearby tree and canopy information.  
2. Filters to buildings with usable energy use and building characteristics.  
3. Creates final features that capture tree canopy exposure and changes over time at the building level.  
4. Runs exploratory analysis and first-pass models to examine relationships between canopy metrics and building energy intensity.  
5. Documents open questions and next steps for improving the models and interpretation.

**Status and skills showcased**  
1. This analysis is still in progress for the current semester, and I am continuing to refine the modeling and diagnostics.  
2. Demonstrates the ability to stitch multi-step data pipelines into a single analysis.  
3. Shows familiarity with panel-style data and modeling energy outcomes as a function of environmental and built-environment features.  
4. Highlights communication of intermediate results, limitations, and planned future work.
