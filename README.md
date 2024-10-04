# SRNE_Inverter_USB_Python_Influx
SRNE Inverters Linux Python script

Intro
Welcome to the SRNE Inverter Linux Python script

After making use of MySQL in the previous project https://github.com/sciferbl8ke/SRNE_Inverter_USB_Python I found that the database was a bottleneck after a large subset of data was in the primary table.  
I tried various things from indexes to partial indexes, archiving data older than 7 days and also trying to make use of Grafana's less data points in a timescale feature but it was slow in general.

Here we are with time-based databases "InfluxDB”, and it is working much better.

Changelog:
The code from the previous project remains the same apart from a few minor changes such as:
* MySQL connector and properties removed
* Probing timeout reduced to 50ms
* All MySQL strings removed

To use, check the file and ensure you have the correct dependencies installed, I prefer not to have the dependencies config linked to this project.
once you have all your dependencies installed, edit the file and set the option No_DB_Output_Print_Data = 1 and you will see the data and there will be no database activities.
After installing InfluxDB V2, configuring your tokens, orgs and buckets, put your string inside the file and test the connection by setting No_DB_Output_Print_Data = 0.

Have fun and enjoy
