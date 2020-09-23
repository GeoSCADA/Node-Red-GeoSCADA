node-red-GeoSCADA
===================

A <a href="http://nodered.org" target="_new">Node-RED</a> node to send/receive telemetry data with <a href="http://www.schneider-electric.com/en/product-range-presentation/61264-clearscada/" target="_new">Geo SCADA Expert</a>.

Install
-------

Note - the following install below will not work until the node has been contributed. Until then please follow the instructions in the Word file in this repository.


Run the following command in your Node-RED user directory - typically `~/.node-red`

    npm install node-red-contrib-GeoSCADA


Usage
-----

### Geo SCADA Set Point Value output node

Uses the Geo SCADA web API to send an analogue, digital or string value in `msg.payload` to an Internal Point of that type in Geo SCADA.
* Optionally uses `msg.topic` to set the point`s full name, if not already set in the properties.
* Optionally uses `msg.time` to set the process time of the point, and if absent the Geo SCADA server will use its receipt time.

### Geo SCADA Get Object Data node

Gets summary data about an object. For example, when using a point name, the data includes Current Value, Time, Quality etc.

### Geo SCADA Query node

Execute any SQL query and return the results to node-red.
