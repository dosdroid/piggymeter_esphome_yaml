# PiggyMeter ESPHome configurations - added calculated sensors


My one phase power meter for some reason does not provide enough decimal points on Absolute active energy total but provides enough granularity with Instantaneous voltage in phase L1 and Instantaneous current in phase L1.

This adds two new calculated sensors.

instantaneous_power_in_phase_l1 - calculates power from current and voltage

calculated_energy_consumption - approximates power consumption based on power and time between readings of iec62056. In order to minimize calculation errors and drifts it will normalize towards the value of Absolute active energy total in case it drifts more than selected value (default: 1 kWh).

Also I have added internal SoC temperature readings of esp 32 (Wemos S2 mini) and option to restart device remotely and edit the drift treshold via HA GUI

My powermeter is: ZPA ZE110.D0 - https://www.premereni.cz/cs/dulezite-informace/montaz-elektromeru/prehled-instalovanych-elektromeru/ze110d0/ 

For project description see https://aquaticus.info/meter.html
