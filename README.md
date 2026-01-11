# Honda CBR1100XX Super Blackbird - Wiring harness adapter board

This project incorporates a printed circuit board design that allows you to connect from the OEM Honda CBR1100XX Blackbird wiring harness to your stand-alone ECU of choice.
This adapter board specifically targets the early 2000's model EFI Honda Blackbird.

In my case, it is an Australian 2002 model.

The OEM Keihin ECU contains two groups of 22 connector pins that mate with bikes wiring harness. The harness side contains the two connectors (black and light gray) that the ECU mates with. These 22-pin connectors are proprietary and are located underneath the seat at the rear of the motorcycle.

This PCB design provides a means of conveniently interfacing with the existing 22-pin connector to your specific standalone ECU of choice without having to sever the existing wiring harness.
A custom wiring harness can then be separately built to interface to the stand alone ECU via standard Molex connectors numbered at the top of the board.<br/> The benefit of such an interface board also allows you to revert to the original Keihin ECU if you so wish since it allows the bikes wiring harness to remain undisturbed.
(Note: This will only be the case if the camshaft trigger wheel is also left undisturbed).

Fitment to a motorcycle will require the construction of two PCB's. An example of two completed boards are shown below together with its fitment to the existing wiring harness in place of the Keihin ECU.

![Alt Text](pcb/images/Assembled_1.jpg)
![Alt Text](pcb/images/OnBike.jpg)

Note: This project is in its early stages, so does not discuss packaging or sealing of the boards from the elements at this stage. It is evolutionary in nature and will attempt to improve shortcomings over time as new ideas come to light.

</BR>

This project has been designed in Kicad 6.0.11 under linux and is licensed under the TAPR Open Hardware License (www.tapr.org/OHL).

The directory structure of this project is as follows:

<p id=directories>
<img src="pcb/images/.directoryStructure.png" width="302">
</p>



<table border="1">

<tr> 
<td width="20%">
<strong><u>Directory</u></strong>
</td>
<td width="80%">
<strong><u>Description</u></strong>
</td>

</tr>

<tr>
<td width="20%">
BOM
</td>
<td width="80%">
Bill of materials
</td>
</tr>

<tr>
<td width="20%">
datasheets
</td>
<td width="80%">
Data sheets for pins and connectors
</td>
</tr>

<tr>
<td width="20%">
images
</td>
<td width="80%">
Various images, pictures, board renditions
</td>
</tr>

<tr>
<td width="20%">
kicad
</td>
<td width="80%">
The main kicad project folder.<br>
This contains the project itself (uses kicad 6.0.11)</br>
The main project file is 'CBR_AdapterBoard.kicad_pro' found under</br>'/pcb/kicad/CBR_AdapterBoard'.</br></br>
Gerber files can be found as a group of 9 individual files under the 'gerbers' folder or as a single zipped file for uploading to a PCB house for manufacture.</br></br>
The 'CustomLibrary' folder contains the custom symbols and footprints used in the project.
</td>

</table>

</br>


After cloning the repository and opening the project for the first time, you may need to set up the symbol and footprint library paths.

To setup the symbols library, in the menu:<br>
<pre><i>Preferences -> Manage Symbol Libraries</i><br>
  Then in the 2nd tab under 'Project specific libraries' add the following:<br>
Nickname: <b>Blackbird</b><br>
Library Path: <b>${KIPRJMOD}/../CustomLibrary/symbols/Blackbird_symbols.kicad_sym</b><br>
</pre>
<br><br>

To setup the footprint library, in the menu:<br>
<pre><i>Preferences -> Manage Foorprint Libraries</i><br>
  Then in the 2nd tab under 'Project specific libraries' add the following<br>
Nickname: <b>Blackbird</b><br>
Library Path: <b>${KIPRJMOD}/../CustomLibrary/footprints/</b><br>
</pre>
<br>


## Relevant links

### Wiring Harness
To see the ECU pin-out details, refer to the latest pdf file at:
[Wiring Harness Pinout diagram](https://github.com/BlackbirdStandalone/Documentation/tree/main/wiring).


