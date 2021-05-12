![GitHub release (latest by date)](https://img.shields.io/github/v/release/vinaydawani/EZTracker?style=for-the-badge)
![GitHub](https://img.shields.io/github/license/vinaydawani/EZTracker?color=yellow&style=for-the-badge)
![QGIS](https://img.shields.io/badge/MADE%20FOR-QGIS%203-success?style=for-the-badge&logo=qgis)
![python](https://img.shields.io/badge/Made%20With-Python%203.8-blue.svg?style=for-the-badge&logo=Python)

# EZTracker User Manual

### [Tomas Baliu-Rodriguez](https://www.linkedin.com/in/tomas-baliu-rodriguez-369a1315b/), [Michael Mott](https://www.linkedin.com/in/michael-mott-681269175/), [Claire Horack](https://www.linkedin.com/in/claire-horack-babb8294/), [Vinay Dawani](https://www.linkedin.com/in/vinaydawani/)
<br>

## Vision Statement

**For** Data Analysts<br>
**who** want to dynamically find similarities in attributes across geographic data,<br>
**the** EZTracker<br>
**is an** interactive plugin in QGIS<br>
**that** highlights polygons that fall within an attribute value range similar to a user-selected polygon.<br>
**Unlike** a static map that displays data ranges throughout the region,<br>
**our product** allows a user to click the target polygon, providing a dynamic view of similar polygons<br>
**which supports our strategy to** visualize data and better inform data analysts<br>

## Installation Guide

### Method 1(recommended):

1) Download the file eztracker.zip
2) Open QGIS
3) Plugins>Manage and Install Plugins
4) Click on Install from ZIP tab
5) Click on the “...” button and navigate to extracker.zip
6) Click Install Plugin
7) You will now find the plugin on the plugin toolbar

### Method 2:

1) Download the file eztracker.zip
2) Extract folder to one of the options below, whereUSER_NAME is the actual account
name on the computer
a) PC:
C:\Users\USER_NAME\AppData\Roaming\QGIS\QGIS3\profiles\default\pyt
hon\plugins\
b) MAC: /Users/USER_NAME/Library/Application
Support/QGIS/QGIS3/profiles/default/python/plugins/
3) Open QGIS.
4) Click on Plugins>Manage and Install Plugins>
5) Click on Installed Tab.
6) Select EZTracker.
7) Click close.
8) You will now find the plugin under the plugin toolbar.

## Usage Guide

1) Click on the EZTracker plugin.
2) Load one or more polygonal .shp files into the layers window and set one as active.
3) Select a numerical attribute from the drop-down menu. If no attributes are listed
then there are no numerical attributes for that .shpfile.
4) Select a number for the bound. This number will be added and subtracted to the
largest and smallest attribute values acquired from the polygon selections.
5) Click one or more polygons from the active layer and all polygons containing
attribute values that fall within the bound will be highlighted. When multiple
polygons are selected, all polygons containing an attribute value in between the
attributes of the selections will be highlighted.
6) Clicking outside the layer will remove all polygon selections and highlights.
7) To change the layer you are working with, set the desired layer as active.
8) When you update the Attribute Value Range, the QGISmap will not display the
update to the highlights until it is clicked on. It is recommended to do so using a
middle mouse button as this will not affect the current selections made by the user.
If you prefer, you may reselect the yellow polygons by clicking on them to see the
updated result.

### Saving a result:

1) Once you have the similar features that are desired, click the ‘Select Folder’ button
and select the location you wish to have the file saved.
2) Enter a name for the file. If left blank nothing will happen. If the file name already
exists in the location, the original file will be overwritten.
3) Click Save as Style.
4) This output is saved as a .qml file. This is saving the rule symbology that creates the
output viewed on the map. It is important to note that the .qml file needs to be saved
near to the .shp file used to create it.

### Retrieving a saved output:

1) First load in the .shp file that was used to create the output.
2) Right-click on the layer and click Properties
3) Click Symbology
4) In the Symbology tab, at the bottom of the window click Style.
5) Click Load Style.
6) Click on the ‘...’ next to File.
7) Navigate to the desired .qml file that was previously saved
8) Click Load Style
9) Click apply

## Results:

![figure 1](assets/fig%201.png)
Figure 1: One Selection with a Bound 

![figure 2](assets/fig%202.png)
Figure 2: Four Selections with no Bound 

![figure 3](assets/fig%203.png)
Figure 3: Two Selections with no Bound and AttributeList 

![figure 4](assets/fig%204.png)
Figure 4: Radio Button folder selection

![figure 5](assets/fig%205.png)
Figure 5: The File Name and Saved Output 

In Figure 1, you can see that Franklin County was selected along with the Percent of
Democratic voters in the numerical attribute Combobox with a bound of .1 meaning 10% in
our data. Thus, all counties containing plus or minus10% of the democratic votes as
Franklin County was highlighted.

In Figure 2, you can see four counties in central Ohio were selected but no bounds, thus the
bounds will be the highest and lowest attribute values(in this case percentages again) from
the selection. So all highlighted counties fall within the voting percentages of the four
selected counties. Giving a higher bound would highlight even more counties that fall
within the natural extents plus and minus the bound.

In Figure 3, you can clearly see that all the area IDs in between the selection are highlighted.
Also, the drop-down for the numerical attributes is shown.

In Figure 4, you see the result of clicking on the radio button next to the save button. This
pulls up a file explorer and the user then clicks on choose folder once they find the area to
save.

In Figure 5, you see that the user gave the output a valid name and hit save after choosing a
folder. The output is clearly saved in the selected folder with the given name as a QML file.
___
Any feedback is welcome and you can send it [here](https://vinaydawani.dev/contact).