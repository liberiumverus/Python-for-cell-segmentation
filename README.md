# Python-for-cell-segmentation
Just a frustrated Uni student who can't get a software to work so he created a Python code to brute force his way through his FYP. This code creates spatial plots, histograms and their respective csv for easy data analysis of histogram data, and exports it as a file output. This works in tandem with FIJI ImageJ Tissue Analyzer. Best used for cell segmenting of Drosophila wings, wing disc and pouch.


Also includes box plots and bar charts with significance plots. Both uses pre-calculated std and p-values for Mann-Whitney U as I coudn't find out whats wrong with the plot. 


Single sample plots and histograms will be exported to the same directory as the database that was used


Overlay plots and pooled cell histograms will be exported into the desktop as a separate file


For box plots and bar charts, input in dataset inside code accordingly and run the code. Will output 6 plots for the parameters: total wing area, perimeter, perimeter/area, aspect ratio, circularity and roundness. Error bars represent +- std and bar charts plots average values.

