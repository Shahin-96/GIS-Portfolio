# Area Impacted by Wildfire in California State


## Project Overview
In this project, I conducted a GIS-based analysis to quantify the impact of wildfires across California counties over the past 10 years (2012-2022). The objective was to determine the total area burned by wildfires in each county and summarize broader wildfire patterns. This kind of analysis provides valuable insights into wildfire recovery planning and resource allocation. The final output includes a county-level wildfire impact map, statistical summaries, and a GIS package that can be used for further decision-making.

Here are provide pictures of Sanitarium, Napa County, California and Junction City, Trinity County, California before and after wildfires.
| Sanitarium | Junction City |
|-------------|-------------|
| ![Sanitarium](https://github.com/user-attachments/assets/019fd42e-aea8-4452-9dd3-5fc0ab08fa66) | ![Junction City](https://github.com/user-attachments/assets/c23d0ed7-6dec-436e-991e-78ae88db9892) |



## Objectives
- Calculate the total wildfire-affected area for each county in California.
- Analyze spatial patterns of wildfire distribution over 10 years (2012-2022).
- Represent the percentage of each county affected by wildfires.
- Create a well-structured map layout for visualization and reporting.
- Publish and share the GIS results as a map package and PDF.


### Skills Learned
- Utilizing Data Management & Analysis Tools (Dissolve, Intersect, and Summary Statistics)
- Adding and calculating new fields for area and percentages
- Performing joins and field calculations
- Symbolizing counties based on percentage burned using Natural Breaks (Jenks) classification
- Designing an informative map layout
- Creating a map package
  
### Tools Used
- ArcGIS Pro
- ArcGIS Online

## Steps

### 1. Data Preparation
- Unzip the provided geodatabase (Wildfire_Impacted_Area_Assignment.gdb).
- Add the Counties and Wildfires feature classes to the map.

### 2. Spatial Analysis
- Dissolve wildfire perimeters into a single polygon to represent all impacted areas (using Dissolve Tool).
- Intersect the dissolved wildfire perimeters with county boundaries (using Intersect Tool).
  
### 3. Attribute Calculations
- Add a new field in the intersected layer to store area (in US Survey Acres).
- USe "Calculate Geometry" to determine the burned area for each county.
- Use Summary Statistics Tool to sum wildfire area by county, setting “COUNTY” as the case field.

### 4. Step 4: Join & Percentage Calculation
- Add a new field in the County layer to store wildfire area values.
- Join the Summary Statistics output to the County layer.
- Use Calculate Field Tool to populate the new field with wildfire area values.
- Remove the join to maintain dataset integrity.
- Add another field to store the percentage of county burned.
- Compute (!Wildfire_Area! / !Area_Acres!) * 100 to get percentage burned per county.

### Step 5: Map Visualization & Layout Design
- Symbolize counties based on percentage burned using Natural Breaks (Jenks, 5 classes).
- Label counties with their names.
- Create a well-structured map layout including:
Title
Legend (percentage burned classes)
Scale bar & North arrow
Basemap for reference
Data sources & publication date
- Add metadata to document processing steps, source data, and methodology.

### Step 6: Export & Share
Export the map layout as a PDF for report submission.
Create a map package and upload it to ArcGIS Online for public access.


![image](https://github.com/user-attachments/assets/6459c80a-77cc-4d7e-855d-5dfc6afa377e)





