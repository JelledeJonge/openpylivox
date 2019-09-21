# OpenPyLivox
Python3 driver for Livox lidar sensors

***See the [Wiki](../../wiki) Pages for complete documentation (WORK IN PROGRESS)!***

Check out the [livox_controller_demo.py](./livox_controller_demo.py) file for complete details on how to use the OpenPyLivox v1.0 library

*NOTES:* 
- OpenPyLivox v1.0 has only been tested using Mid-40 sensors
- simultaneous operation of multiple Mid-40 sensors has been tested, but NOT using a Livox Hub
- the library has been tested on Mac OS X, Linux (GalliumOS on HP Chromebook), and Windows 7 and 10
- the library has been tested to work with Livox Mid-40 firmwares:
  - 03.03.0001 (double return)
  - 03.03.0002 (triple return)
  - 03.03.0003 (noise filtering)
  - 03.03.0004 (noise filtering - strict)
  - 03.03.0005 (short blind-zone)
  - 03.05.0000 to 03.06.0000 (standard versions)
- The CSV output file's header record, allows the point cloud data to be easily opened in the <b>amazing</b> open source software, CloudCompare (download at https://cloudcompare.org)

`//X,Y,Z,Inten-sity,Time,ReturnNum`      (ReturnNum is only included when using firmwares 03.03.0001 or .0002)

**Quirky Fact:** Intensity (a.k.a., Reflectivity in the Livox documentation) has a hyphen in the CSV header record in order to 'trick' CloudCompare into assigning the field as a scalar type by default. This enables displaying the point cloud in CloudCompare using a more visually appealing colour spectrum (e.g., left image below). It also provides a way to (possibly) help filter out some unwanted noisy data. Of course, the colour scheme can be changed to many other options, after importing the point cloud in CloudCompare (e.g., greyscale in right image below)

<table style="border:0px;">
  <tr style="border:0px;">
    <td style="border:0px;"><img src="./images/image1_rs.png"></td>
    <td style="border:0px;"><img src="./images/image2_rs.png"></td>
  </tr>
</table>
  
