# Path-Finder
Now your task is to build an AI route finder. You are given a data file (tubedata.csv) in CSV format with the London
Tube map (which is not necessarily an up-to-date or complete map). The Tube map is defined in terms of a logical
relation Tube “step”. If you open the data file with any text editor, you will see the content of the file as:

Harrow & Wealdstone, Kenton, Bakerloo, 3, 5, 0

Kenton, South Kenton, Bakerloo, 2, 4, 0

···
Bank/Monument, Waterloo, Waterloo & City, 4, 1, 0

Each row in the CSV file represents a Tube “step” and is in the following format:

[StartingStation], [EndingStation], [TubeLine], [AverageTimeTaken], [MainZone], [SecondaryZone]

where:

• StartingStation: a starting station

• EndingStation: a directly connected ending station

• TubeLine: the tube line connecting the stations above

• AverageTimeTaken: the average time, in minutes, taken between the starting and the ending station

• MainZone: the main zone of the starting station

• SecondaryZone: the secondary zone of the starting station, which is 0 if the station is only in one zone. Note:

if the secondary zone is 0, use the main zone to define the zone for the ending station; otherwise, use the
secondary zone.

Throughout this coursework, you may find it helpful to refer to the London Tube map at:

https://content.tfl.gov.uk/large-print-tube-map.pdf

The preferred way to load the data is using the pandas Python library method read csv with the parameter
header=None using the process tubedata method in the search.py file attached to this coursework.
Note that in the labs, we used the NetworkX library for graph visualisation. But in this CW you should not use it
in the code you submit. You may use it to debug your code, but your final submission should NOT include any use
of the NetworkX library.
