# ferroamp_easee_pv-loadbalancing
Blueprint for PV loadbalancing using ferroamp and easee

This blueprint makes it possible to tune the charging power of your Easee Home charger to match your excess power from solar production.
Easee require a minimum of 6A for charging so the minimum charging power will be ~3.5kW for 3phase charging. 

Blueprint is custom made for Ferroamp EH and Easee Home charger but will work with other brands as long as they can provide the sensor required below.

<br>
<b>Important!</b><br>
Before you use this blueprint, make sure you have Ferroamp MQTT and Easee Charger integrations fully up & running. <br>
<br>
Link to <b>Easee</b> Integration: https://github.com/fondberg/easee_hass <br>
Link to <b>Ferroamp</b> Integration: https://github.com/henricm/ha-ferroamp <br>
<br>
<br>
<b>Sensor setup:</b><br>
Ferroamp Solar power sensor:<br>
<i>This sensor shall display the total power production from your solar panels in Watts.</i> <br>
<br>
Ferroamp Consumption power sensor:<br>
<i>This sensor shall display the total household consumption in Watts. </i> <br>
<br>
Ferroamp External voltage sensor:<br>
<i>This sensor shall display the voltage L1+L2+L3 (~690V). </i> <br>
<br>
Easee charging power sensor:<br>
<i>This sensor shall display charging power in kilowatts (kW). </i> <br>
<br>
Easee Charger Dynamic limit sensor:<br>
<i>This sensor shall display your current dynamic limit in Amps. Make sure to select CHARGER limit and not circuit.</i> <br>
<br>
Easee Charger Status sensor:<br>
<i>This is the status sensor for your Easee charger. By default the name is sensor.<your chargername>_status</i> <br>
<br>
Activate time:<br>
<i>Set the time in the morning when you want to activate loadbalancing. Set the time so it won't make a conflict with charging during night.</i> <br>
<br>
Deactivate time:<br>
<i>Set the time in the evening when you want to deactivate loadbalancing. Set the time so it won't make a conflict with charging during night.</i> <br>
<br>
<br>
Activate and deactivate times are important to keep nighttime charging at full power otherwise the logic will only allow charging at ~3.5kW due to lack of solar production. 
<br><br>
  
Good luck :-)
