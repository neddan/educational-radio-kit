**Troubleshooting**

The troubleshooting guide section is divided into multiple sections for easier isolation of issues. The issues are broadly categorized into *Installation and Assembly* as well as *Usage*. To find your specific fault simply refer to the troubleshooting guide to find what fault matches the one you are experiencing. **Please do note that this section of the guide is a technical guide for advanced users!**

**1.0	Installation and Assembly** 

*1.1.	You have different components than what is listed in the requirements*

If you end up having different components than what is listed on the requirements section then you can proceed with verifying and trying the following;

1.	Different ICs than what is listed for example a different power management IC (PMIC): any TP43xx IC and any other ICs used from the same family should have the same basic circuitry meaning to say it should work without major modifications. 

However, if you have a chip from a different manufacturer, you can use that part’s datasheet to check which pins are responsible for what function. The basic working principle should be the same therefore only the orientation of the pins and other minor requirements might differ.

2.	If you have different values of supporting components such as capacitors and resistors or diodes, it is important to note that these are trickier to improvise due to the nature of a radio receiver. Therefore, if you have different value capacitors, make sure the voltage remains the same as listed in the requirements. The capacity can be varied but not less than the recommended. 

**NOTE!** This is applicable to components in the power section only.  For the amplifier and tunning sections, components are not replaceable without thorough re-evaluation of the entire circuit. For help with replacing components in the tunning and amplifier sections especially resistors and capacitors please refer to the online radio kit community for help with real-time troubleshooting. 

*1.2.	Having trouble with soldering components onto the PCB*

If you are trying to solder the components but are having trouble getting this done, check the following to try and solve your problem;

1.	Make sure you have the right wattage soldering iron and that it is properly plugged into your electrical outlet. Soldering simple PCBs such as this one requires no less than 40 Watts of electrical power. 60 Watts can be used but 80 Watts and above is too much heat for the PCB and can cause burning. Stand alone soldering irons are rated on the handle or otherwise packaging. Check to confirm wattage. In the case of an adjustable iron, set the temperature to 350ºC.

2.	Check the type of solder wire being used. A wire of diameter less than or equal to 1mm is recommended for easy melting. Bigger solder wire may be harder to melt and may harden upon getting into contact with the PCB due to conduction cooling effect of the PCB. In addition to that, a flux core solder wire is recommended which is softer and easier to melt. Check for indications such as lead-free or leaded solder, this also affects melting temperature.

3.	If your soldering joints are sticking onto each other, especially in the case of IC pin legs, use Soldering flux to ensure free flowing of the molten solder. Conversely, if your molten solder is not sticking on to the surface you are soldering onto, consider using rosin flux. The rosin ensures that solder sticks as it hardens. Therefore, having both rosin and rosin-free flux at hand will be helpful.

**NOTE!** In order to avoid soldering mistakes, it is advised to start with soldering the main section IC first then moving on to soldering diodes and resistors followed lastly by capacitors and any other big components. In addition to that, soldering the PCB section by section ensures cleaner work and less mistakes.

*1.3.	No power on VCC pin after soldering the power section*

If after assembling and soldering the power section of the PCB, you get no power on VCC pin of the PCB as stated in step 6, then follow through the following to try and identify your fault;

1.	No power from source. This could be caused by a severed connection from the power source i.e., battery, charger & solar. Using a multimeter in continuity mode, measure the connection from the positive (“+” or red wire) to the INPUT point and negative (“-“ or black wire) to the GND point on the PCB. For the external batteries, measure continuity from the + and – leads on the battery loading side to the VCC and GND points. As for the internal battery, refer to point number 2.

2.	In other cases, the issue may lie with the voltage from the source. The PMIC expects a certain range of voltages in order for it to work. Therefore, using a multimeter, check and measure the voltage from the power sources to verify their integrity. Micro-USB should read 5.1 (+/-0.2) volts, solar 5.0 (+/-0.5) volts, internal lithium-ion 3.7-4.1 (+/-0.1) volts and each single A battery no less than 1.5 (+/-0.1) volts. If any of the voltages are abnormal, they should interfere with the stable output expected on VCC pin.


3.	If all connections are okay, then another likely cause of missing voltage on the VCC pin could be faulty capacitors. Using a multimeter in continuity mode, check the continuity from positive to negative/GND of the PCB. 

There should be No continuity (an audible continuity beep from the meter). Instead, a reading of 0.2-0.5 Ω or greater on the meter should indicate properly working capacitors or any component connecting to ground e.g., diodes. 

An audible beep in continuity mode indicates a shorting to ground which is causing the IC not to output any voltage. Verify this by placing one probe of the multimeter on any ground pad and then placing the other probe on either side of all capacitors in the power section.

Once a short is discovered, remove capacitors one by one and test them out of circuit (place probes on the two legs and verify there is no beep or low Ω reading. Healthy capacitors read “OL” or “1” indicating no continuity). Replace any faulty capacitors if discovered.  

4.	Faulty diodes. Apart from capacitors, another culprit that may short to ground is a diode. A reverse polarity protection diode (which is connected from positive to negative)

5.	Faulty power management IC. In some instances, all the supporting components may be fine. However, the PMIC itself may be faulty. Simply replace the chip with another one.

**NOTE!** If after replacing the IC the issue is still not resolved, please request for assistance on the online community to get real-time assistance with your particular issue. Also take note that it is safe practice to disconnect any power sources when running tests other than voltage tests.

*1.4.	No sound after soldering the amplifier section.*

This part assumes that you have finished soldering the amplifier section and are trying to test audio but no pop sound is coming out of the speaker. Several of the following reasons could be the contributing factors;

1.	No power flowing to the amplifier. 

*1.5.	No static noise after soldering the tunning section.*

*1.6.	Volume is not increasing or decreasing.*

*1.7.	The static is not changing after tuning.*

*1.8.	The red charging light is not turning on.*

*1.9.	Red charging light turning on after connecting external  batteries.*

*2.0.       Further troubleshooting.*
