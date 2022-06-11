| Device details: 
| We have used the following devices.
#. 3706A SYSTEM SWITCH/MULTIMETER
#. 3765 HALL EFFECT CARD
#. 6221 DC/AC CURRENT SOURCE
#. 2450 SOURCEMETER 2182A NANOVOLTMETER

| One can also prefrably use a picoammeter along with these, with appropriate modifications to the code ( user has to do that XD ). 


| The user provides a range of current values. For a specified value of current, 8 iterations of the following algorithm take place to compute V1 through V8.
| In a single iteration ( for Vi )  - 
#. The current source is configured. Current value is set.
#. The switch is configured for Vi mode.
#. The current supply is turned on.
#. The voltmeter takes multiple readings and stores them in a buffer. Mean is calculated and stored as Vi.
#. The current supply is turned off.

| Main Features:
* The front panel of Labview is divided into three sections- current source, voltmeter ( nanovoltmeter/ SMU), system switch. 
* The user has to first select the VISA resources for all the above mentioned instruments. 
* User has to specify the start, end, and step size in the first panel to generate a range of current values.
* The voltmeter buffer values, mean voltage, current set on the current source is displayed in the second panel. 
* In the third panel, user has to select among:

    #. GUARDED / UNGARDED mode
    #. VAN DER PAW / HALL EFFECT measurement mode
    #. The user can see the iteration number ( that is which Vi is being currently read ) along with the corresponding channels closed on the switch.

* Some other features are present on the panel- setting voltage compliance ( limit ), range selection, error displays, voltage limit indicator, etc. 

| Instructions:
| For DC/AC current source -
* If using GPIB cable,  go to the COMM>> turn on the GPIB communication. If using the RS323 , go to the COMM>> turn on the RS323 mode.
* Go to Triax>> and make inner shield as Guard. 

| Troubleshooting: 
* In case the sircuit is open, the voltage compl
* If you are using GPIB connections, make sure to use the proper driver.
* If you are connecting 2450 sourcemeter using GPIB cable, you may encounter errors with its driver.
* If you have installed the drivers and still your resources are not detected, you may try restarting the system.

| Warnings:
* Do not exceed the voltage compliance mentioned in the hall effect card specifications.
* Do not exceed the current value as recommended by the operator.
