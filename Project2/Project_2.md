

### Project 2

### Images!

```![Thermal Elevation Change Data](giffy.gif)```

### Project Parameters & Code

Data:

- LC08_L1TP_039007_20170814_20170825_01_T1_sr_band5 (Landsat Data)

- Ocean Profile temperature elevation data (My data)

Tools:

- Built tables from ocean vertical point data for 1m, 10m, 50m, 100m, 150m, 200, 250) as Add Delimited Text Layer
- Inverse Distributed Weight Interpolation from Vector
- Clip Interpolated raster surfaces of temperature at different elevations by polygon

Product:

Map: My map shows the temperature changes between sea level elevation in front of Canada's melting glaciers
- The number in the right corner represents elevation in m
- The heat map indicates in red the warmer water and blue the cooler water via continous heatmap  per elevation temperature range
- The black points are represent where the CTD cast locations temperature

My Coordinate Reference System is Extent:
NAD83(CSRS) / EPSG Arctic zone 5-37

Code:

- I want to select the features in the 1m vector table file that have an ID name of C4-C10, C14-16, and C22 (these buggers show me where the ocean influence is coming in and eating away at the glacier from underneath).

- then I want to change there symbol color to Red.
```
from PyQt5.QtGui import QColor
from PyQt5.QtCore import Qt
from qgis.utils import iface

```
iface.addVectorLayer('D:\Desktop\Arctic data\CTD\1m.gpkg')

1m = iface.activeLayer()
renderer = 1m.renderer()
symbol = renderer.symbol()
symbol.setColor(QColor(Qt.black))
1m.triggerRepaint()
iface.layerTreeView().refreshLayerSymbology(1m.id())

iface.showAttributeTable(iface.activelayer())

load_layer()
change_color()

# Selecting the vector to pull the select features from for the new file
feature = 1m_layer.getFeature( one )

# save selected features to file
QgsVectorFileWriter.writeAsVectorFormat(1m_layer, 'D:/Desktop/Arctic data/glacier_eater.gpkg', 'utf-8', LAYERVARIABLE_name_selectedfeatures.crs(),'GPKG', True)

#Need to merge in something like this to actually pull the items in the vector related to a attribute ID!

>>> 1m_warm= layer.getFeature()
>>> 1n_warm.attributes()
[ 'C4', 'C5', 'C6', 'C7', 'C8', 'C9', 'C10', 'C14', 'C15', 'C16', 'C22']
The attributes method returns the feature data

#This is the code bit that might help towards making the select vector points I care about RED.

5 class FirstScript:
6
7 def __init__(self, iface):
8 self.iface = iface
9
10 def load_layer(self):
11 self.iface.addVectorLayer('D:/Desktop/Arctic data/CTD')
12
13 def change_color(self):
14 active_layer = self.iface.activeLayer()
15 renderer = active_layer.renderer()
16 symbol = renderer.symbol()
17 symbol.setColor(QColor(Qt.red))
18 active_layer.triggerRepaint()
19 self.iface.layerTreeView().refreshLayerSymbology(active_layer.id())
20
21 def open_attribute_table(self):
22 self.iface.showAttributeTable(self.iface.activeLayer())
23
24
25 def run_script(iface):
26 fs = FirstScript(iface)
27 fs.load_layer()
28 fs.change_color()
29 fs.open_attribute_table()


```
