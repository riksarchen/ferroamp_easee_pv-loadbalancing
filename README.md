# ferroamp_easee_pv-loadbalancing
<a href="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Friksarchen%2Fferroamp_easee_pv-loadbalancing%2Fblob%2Fmain%2Fferroamp_easee_pv-loadbalancing.yaml" target="_blank"><img src="https://my.home-assistant.io/badges/blueprint_import.svg" alt="Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled." /></a><br>br><br>
Blueprint for PV loadbalancing using ferroamp and easee

This blueprint makes it possible to tune the charging power of your Easee Home charger to match your excess power from solar production.
Easee require a minimum of 6A for charging so the minimum charging power will be ~3.5kW for 3phase charging. 

Blueprint is custom made for Ferroamp EH and Easee Home charger but will work with other brands of Inverter as long as it can provide the sensors required below.

<br>
<b><h2>Important!</h2></b><br>
Before you use this blueprint, make sure you have Ferroamp MQTT and Easee Charger integrations fully up & running. <br>
<br>
Link to <b>Easee</b> Integration: https://github.com/fondberg/easee_hass <br>
Link to <b>Ferroamp</b> Integration: https://github.com/henricm/ha-ferroamp <br>
<br>
<br>
<b><h2>Sensor setup:</h2></b><br>
<b>Ferroamp Solar power sensor:</b><br>
<i>This sensor shall display the total power production from your solar panels in Watts.</i> <br>
<br>
<b>Ferroamp Consumption power sensor:</b><br>
<i>This sensor shall display the total household consumption in Watts. </i> <br>
<br>
<b>Ferroamp External voltage sensor:</b><br>
<i>This sensor shall display the voltage L1+L2+L3 (~690V). </i> <br>
<br>
<b>Easee charging power sensor:</b><br>
<i>This sensor shall display charging power in kilowatts (kW). </i> <br>
<br>
<b>Easee Charger Dynamic limit sensor:</b><br>
<i>This sensor shall display your current dynamic limit in Amps. Make sure to select CHARGER limit and not circuit.</i> <br>
<br>
<b>Easee Charger Status sensor:</b><br>
<i>This is the status sensor for your Easee charger. By default the name is sensor.<your chargername>_status</i> <br>
<br>
<b>Activate time:</b><br>
<i>Set the time in the morning when you want to activate loadbalancing. Set the time so it won't make a conflict with charging during night.</i> <br>
<br>
<b>Deactivate time:</b><br>
<i>Set the time in the evening when you want to deactivate loadbalancing. Set the time so it won't make a conflict with charging during night.</i> <br>
<br>
<br><b>
Activate and deactivate times are important to keep nighttime charging at full power otherwise the logic will only allow charging at ~3.5kW due to lack of solar production. 
  <br><br></b>
  
Good luck :-)
