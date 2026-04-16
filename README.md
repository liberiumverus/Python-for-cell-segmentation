A custom Python analysis pipeline developed during my final year project to overcome limitations in existing image analysis tools. Designed to work alongside FIJI ImageJ Tissue Analyzer, this workflow streamlines quantitative analysis of segmented cellular data.


Overview

This project focuses on analysing segmented cells from Drosophila wing, wing disc, and pouch datasets.

The scripts automate:

- Spatial visualisation of cells
- Histogram generation for key cellular metrics
- Export of structured CSV tables for downstream analysis

All outputs are generated directly from .db files produced by Tissue Analyzer.

Features
1. Single-Sample Analysis
Spatial plots of cell positions
Histograms of:
- Cell area
- Perimeter
- Orientation
- Elongation (S1)
- Neighbour distribution analysis
- Cell density heatmaps
Automatic CSV export of histogram binning

Output location:
→ Same directory as the input .db file

2. Multi-Group Comparison
Box plots with jittered data points
Bar charts with error bars (± standard deviation)
Significance annotations (Mann–Whitney U test, pre-calculated)

Parameters analysed:

- Total wing area
- Perimeter
- Perimeter / Area
- Aspect Ratio
- Circularity
- Roundness

Output location:
→ Desktop (as compiled figures)


Usage
Input Requirements
.db file generated from FIJI ImageJ Tissue Analyzer
Data must contain:
- Cell coordinates
- Shape descriptors
- Neighbour information


Running the Scripts


Update file path in the script:
db_path = "path/to/your/TA.db"


For comparison plots:

Manually input datasets into the script


Insert pre-calculated:
- Mean / standard deviation
- Mann–Whitney U p-values
Run the script to generate outputs


Output Summary
Output Type	Description	Location
- Spatial plots	Cell distribution maps:	Same folder as .db
- Histograms	Metric distributions:	Same folder as .db
- CSV tables	Histogram bin data:	Same folder as .db
- Box plots	Multi-group comparisons:	Desktop
- Bar charts	Mean ± SD visualisation:	Desktop


🧠 Notes
- Statistical tests are externally computed and manually input into the plotting script
- Designed for clarity, reproducibility, and publication-quality figures
- Emphasis on high-resolution output (print-ready figures)
