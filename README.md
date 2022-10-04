[![License: CC0-1.0](https://licensebuttons.net/l/zero/1.0/80x15.png)](http://creativecommons.org/publicdomain/zero/1.0/)
[![Made For B&R](https://github.com/hilch/BandR-badges/blob/main/Made-For-BrAutomation.svg)](https://www.br-automation.com)

# Getting started with B&R mapp view




This tutorial shows how to use B&amp;R "Mapp View" Technology Package to implement a simple visualization project as described in Automation Studio online help:

![04_layout](https://github.com/hilch/mapp-view-getting-started/blob/master/media/04_visualization_mockup.png)


Follow the steps below (some pics link to YouTube) or just download the complete release with Automation Studio
project included.

* To run Mapp View on a real PLC a license '1TGMPVIEW.00-01' is required !
* A '1TGMPBRCLNT.10-01' is required for a B&amp;R- Client
* A '1TGMPCLIENT.10-01' is required for a 3rd party client.

We will use a B&amp;R "ArSim" simulated plc so there is no license required.

## 1. Install Technology Package Mapp Motion 5.5

![install mapp motion](https://github.com/hilch/mapp-motion-getting-started/blob/master/media/02_install_mapp_motion_55.png)

## 2. Create a new project with 'ArSim'

[![02](http://img.youtube.com/vi/AiyE6XDUEtA/0.jpg)](http://www.youtube.com/watch?v=AiyE6XDUEtA)

## 3. Insert a Mapp View Visualization into Logical View

[![03](http://img.youtube.com/vi/RZ38lSVSR6E/0.jpg)](http://www.youtube.com/watch?v=RZ38lSVSR6E)

## 4. Create a Layout

we will use the following layout:

![04_layout](https://github.com/hilch/mapp-view-getting-started/blob/master/media/04_visualization_layout.png)

1. insert a layout file and give an id to it
2. add an area 'AreaMain', heigth=600px, width=700px
3. add an area 'AreaNavigation', heigth=600px, width=100px, left=700

[![04](http://img.youtube.com/vi/NXKHmO_vA74/0.jpg)](http://www.youtube.com/watch?v=NXKHmO_vA74)

## 5. insert pages and contents

1. insert 'Navigation.content" into 'AreaContents'
2. insert 'Page1' and add 'Page1Content' to it
3. insert 'Page2' and add 'Page2Content' to it

[![05](http://img.youtube.com/vi/3RwLSz6mHcA/0.jpg)](http://www.youtube.com/watch?v=3RwLSz6mHcA)

## 6. config 'Page1Content'

1. give content a 'Name'
2. config contents heigth and width (600px x 700px)
3. insert a 'Label' widget with text 'Speed'
4. insert a 'Radial Gauge' widget

[![06](http://img.youtube.com/vi/k3JbJhhjnn0/0.jpg)](http://www.youtube.com/watch?v=k3JbJhhjnn0)

## 7. config 'Page2Content'

1. give content a 'Name'
2. config contents heigth and width (600px x 700px)
3. insert a 'Label' widget with text 'Temperature'
4. insert a 'Numeric Output' widget

[![07](http://img.youtube.com/vi/5TJZtMvdz-Y/0.jpg)](http://www.youtube.com/watch?v=5TJZtMvdz-Y)

## 8. config 'NavigationContent'

1. give content a 'Name'
2. config contents heigth and width (600px x 100px)
3. insert a 'Navigation Bar' widget which will be a container for buttons
4. insert two 'Navigation Button' widgets.

[![08](http://img.youtube.com/vi/FrqzgM4ykXc/0.jpg)](http://www.youtube.com/watch?v=FrqzgM4ykXc)

## 9. config pages

1. set 'layoutId' and 'pageId'
2. set page contents 'refId' to 'AreaMain' and navigation content to 'AreaNavigation'
3. set background colours to Areas

[![09a](http://img.youtube.com/vi/RtvG8ZdDPpk/0.jpg)](http://www.youtube.com/watch?v=RtvG8ZdDPpk)

4. config Navigation Buttons e.g. set text and 'pageId'

[![09b](http://img.youtube.com/vi/sTdqS5BWHj4/0.jpg)](http://www.youtube.com/watch?v=sTdqS5BWHj4)

## 10. insert visualization into Configuration View

1. insert visualisation to folder 'mappView'
2. set 'Visualisation id' to 'FirstVisu'
3. set 'StartPage' ('Page1')
4. add 'Page1' and 'Page2' to '<Pages>'

[![10](http://img.youtube.com/vi/MR8PW3gr4m8/0.jpg)](http://www.youtube.com/watch?v=MR8PW3gr4m8)

## 11. insert program

1. insert program and initialize two variables 'Speed' and 'Temperature'
2. declare variables

[![11](http://img.youtube.com/vi/mk94ezcm95g/0.jpg)](http://www.youtube.com/watch?v=mk94ezcm95g)

## 12. activate OPC UA server

1. active OPC UA server in CPU configuration
2. insert OPC UA 'Default View'
3. enable PLC variables visible as OPC UA variables

[![12](http://img.youtube.com/vi/fBoYfqBxXYo/0.jpg)](http://www.youtube.com/watch?v=fBoYfqBxXYo)

## 13. connect variables and widgets

1. insert binding to folder 'mappView' in Configuration View
2. give binding an id and use this id in Visualization's configuration
3. connect variables and widgets ( = binding )

[![13](http://img.youtube.com/vi/ap58UPmMq-M/0.jpg)](http://www.youtube.com/watch?v=ap58UPmMq-M)

## 14. test visualization

1. compile and deploy project
2. open browser and navigate to 'http://127.0.0.1:81/index.html?visuId=FirstVisu'

[![14](http://img.youtube.com/vi/9GENVD3buxU/0.jpg)](http://www.youtube.com/watch?v=9GENVD3buxU)


