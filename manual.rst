================
Instruction Manual
================

----------
Device details: 
----------

| We have used the following devices.
#. 3706A SYSTEM SWITCH/MULTIMETER
#. 3765 HALL EFFECT CARD
#. 6221 DC/AC CURRENT SOURCE
#. 2450 SOURCEMETER 2182A NANOVOLTMETER

| One can also prefrably use a picoammeter along with these, with appropriate modifications to the code ( user has to do that XD ). 

----------
Working:
----------

| The user provides a range of current values. For a specified value of current, 8 iterations of the following algorithm take place to compute V1 through V8.
| In a single iteration ( for Vi )  - 
#. The current source is configured. Current value is set.
#. The switch is configured for Vi mode.
#. The current supply is turned on.
#. The voltmeter takes multiple readings and stores them in a buffer. Mean is calculated and stored as Vi.
#. The current supply is turned off.


----------
Basic Settings:
----------
These have to be done manually by the user.
| For DC/AC current source -
* If using GPIB cable,  go to the COMM>> turn on the GPIB communication. If using the RS323 , go to the COMM>> turn on the RS323 mode.
* Go to Triax>> and make inner shield as Guard. 

----------
Main Features:
----------

* The front panel of Labview is divided into three sections- current source, voltmeter ( nanovoltmeter/ SMU), system switch. 
* The user has to first select the VISA resources for all the above mentioned instruments. 
* User has to specify the start, end, and step size in the first panel to generate a range of current values.
* The voltmeter buffer values, mean voltage, current set on the current source is displayed in the second panel. 
* In the third panel, user has to select among:

    #. GUARDED / UNGARDED mode
    #. VAN DER PAW / HALL EFFECT measurement mode
    #. The user can see the iteration number ( that is which Vi is being currently read ) along with the corresponding channels closed on the switch.

* Some other features are present on the panel- setting voltage compliance ( limit ), range selection, error displays, voltage limit indicator, etc. 

----------
Troubleshooting: 
----------

* In case the sircuit is open, the voltage compl
* If you are using GPIB connections, make sure to use the proper driver.
* If you are connecting 2450 sourcemeter using GPIB cable, you may encounter errors with its driver.
* If you have installed the drivers and still your resources are not detected, you may try restarting the system.

----------
Warnings:
----------

* Do not exceed the voltage compliance mentioned in the hall effect card specifications.
* Do not exceed the current value as recommended by the operator.

----------
Working in the guarded mode:
----------
| To work in the guarded mode, two things have to be done.
#. The two jumper wires in the Hall effect card have to be repositioned as per the instructions in their manual.
#. The guarded mode has to be selected in the third panel in LabView.

----------
Software Requirements:
----------
#. NI LabView 
#. GPIB driver provided by NI instruments

----------
Requirements for Connections:
----------
* 4 Triax to banana cables ( if you are using a puck station ) , OR simply , 4 Triax to - cables which can be connected to the sample ( for example, we have 4 Traix to crocodile cables, and 4 banana to banana cables which were connected together to obtain the above )
* Coax to banana cable ( we have made this by cutting a Coax to Coax cable )
* One traix to triax cable.
* Two banana cables.
* The cables we have used for making connections to the system;

    #. 2 GPIB cables
    #. 2 type-B cables

----------
Making the connections:
----------

The user can make the connections like so. The coax to banana + crocodile isn't a necessity. The connections can be learnt more about properly by going through the manuals of the devices. 

.. image:: docs/fig.png
    :scale: 50


.. image:: docs/Front.jpg
    :width: 500


.. image:: docs/Back.jpg
    :width: 500
