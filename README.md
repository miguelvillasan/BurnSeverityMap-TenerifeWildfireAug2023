# Burn Severity Map of Tenerife wildfire, August 2023.
![20230818_IFArafoCandelariaSentinel2](https://github.com/miguelvillasan/BurnSeverity-TenerifeFireAug2023/assets/112619698/0bd62cd9-9417-4b74-85bd-d3d90e415ba4)

Source: 

## Introduction

The recent catastrophe in Tenerife in August 2023 underscores the urgent need to employ advanced techniques for the monitoring and study of forest fires. On August 15, 2023, a devastating forest fire broke out in Tenerife, Canary Islands, driven by factors such as wind, heat, and low humidity levels. This tragedy prompted massive evacuations, extensive damage to the island's flora and fauna, and impacts on essential supplies. It is considered one of the most destructive fires in recent decades in Spain, affecting multiple municipalities on the island.

In this context, remote sensing emerges as a crucial tool. This technique involves acquiring information about an object or phenomenon without direct contact, typically using sensors aboard satellites or aircraft. The ESA's Copernicus program is a flagship initiative of the European Union for Earth observation and monitoring. It consists of a family of satellites (the Sentinels) and their associated data, which provide detailed images of our planet and help scientists and public policies understand and respond to environmental changes.

## Objective

To develop a fire severity map based on the calculation of the Normalized Burn Ratio (NBR) using Sentinel-2 satellite images and process the data using the Python programming language, focusing specifically on the Tenerife incident of 2023.

## Methodology 

1. Data Acquisition: Satellite images will be acquired from the Copernicus portal, specifically those corresponding to the Sentinel-2 satellite.

2. Pre-processing: Before calculating the NBR, it is essential to pre-process the images. This includes atmospheric corrections, spatial alignment, and cloud filtering.

3. NBR Calculation: NBR is a formula based on the reflectance of the near-infrared (NIR) and shortwave infrared (SWIR) bands. The formula is:

\[ NBR = \frac{(NIR - SWIR)}{(NIR + SWIR)} \]

To determine the fire's severity, the NBR will be calculated both before and after the event. Then, a subtraction between the two will be carried out to determine the change:

\[ \Delta NBR = NBR_{\text{before}} - NBR_{\text{after}} \]

4. Severity Classification: Based on the ΔNBR values, the fire's severity is categorized into different levels, such as low, moderate, and high.

## Case Study: Tenerife Forest Fire of 2023

The fire began on the night of August 15 and quickly spread, affecting significant areas like the Teide National Park, a World Heritage site. By August 22, the fire had affected 14,624 hectares within an 88-kilometer perimeter, impacting 12 municipalities. Finally, by August 25, the fire was stabilized but not completely extinguished.

Analyzing the severity of this fire using satellite images and the proposed index will provide valuable insights into the most affected areas and help authorities design more efficient recovery strategies.

Through the Sentinel-2 satellite from the Copernicus program, there is an aim to develop a severity index for forest fires

![20230825_TenerifeFire](https://github.com/miguelvillasan/BurnSeverity-TenerifeFireAug2023/assets/112619698/9d0e0fba-2240-41a9-950f-788024b1d32e)

Source:

## Getting Started

1. Cloning the Repository

To begin, clone the repository to your local machine:

```bash
git clone https://github.com/miguelvillasan/BurnSeverityMap-TenerifeWildfireAug2023
```
2. Setting up the Python Environment

Once you have the repository on your local machine, navigate to the directory:

```bash
cd BurnSeverityMap-TenerifeWildfireAug2023
```

Next, set up the Python environment using the provided requirements.txt file. This file lists all the Python packages required for this project. Install them with:

```bash
pip install -r requirements.txt
```

3. GeoJSON File

A GeoJSON file is provided which contains the coordinates of the Tenerife 2023 fire. This will be used to scope our analysis to the affected region. Make sure to refer to this file in your analysis scripts or notebooks as it provides essential spatial data.

4. Analysis Notebook

The repository also includes a Jupyter Notebook which contains the Python code used to calculate the fire severity map using the NBR index. 


## Conclusion

The combination of remote sensing and processing with Python offers a robust tool for assessing fire severity. By applying this methodology to the recent Tenerife incident, there's an expectation to gain a deeper understanding of the impact and assist in future prevention and recovery efforts.
