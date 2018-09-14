# IoT sandbox

Blueprint of useful IoT software for the [Subutai Platform](https://subutai.io) 

## How to use this product

IoT sandbox allows you to spin up an online environment with simple steps. It's just a matter of inserting your desired usernames and passwords, and then clicking "next next finish".  Once the environment is up, everything is ready.

Data can then be sent from IoT devices via [mqtt](https://en.wikipedia.org/wiki/MQTT), a lightweight messaging protocol commonly supported by both DIY kits and professional equipment. Sensors, Raspberry Pis and other devices will be able to send data directly into the Subutai environment in which the BP is run. The data is gathered by [Telegraf](https://www.influxdata.com/time-series-platform/telegraf/) and automatically stored on [InfluxDB](https://www.influxdata.com/time-series-platform/influxdb/). The user can then create dashboards for data visualization using [Grafana](http://grafana.org/). All the software needed comes already installed and preconfigured by the Blueprint.

### 1. Run the Blueprint on Subutai

Assuming you have already signed up to the Subutai Bazaar, hop to the [Products](https://bazaar.subutai.io/products) page and click the IoT sandbox Blueprint.

![Click IoT sandbox](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-01.png) 

Insert your desired variables: username, domain name and password for mqtt; name of the environment; password and domain name for grafana; and size of your container. It is ok to use the default values. Don't forget you need to use different domain names for mqtt and grafana.

![Set your Blueprint variables](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-02.png)

Select one Peer to host your Environment's container.

![Select a Peer](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-03.png)

Verify that the domain name was properly assigned.

![Check the exposed port](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-04.png)

Click Finish to start building your Environment.

![Build the Environment](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-05.png)

Wait for some minutes as the Environment is being built. Depending on the characteristics of the Peer you are using, it can take between 5 - 15 minutes.

![Wait some minutes](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-06.png)

Your environment is ready.

![Your environment is ready!](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-07.png)

Check the port mapping tab. You can click the domain name to access Grafana.

![Port mapping tab](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-08.png)

### 2. Check Grafana

Use your browser to acces the domain name you have chosen.

![Access Grafana](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-09.png)

Log in *using the username "admin"* and the password you defined for grafana before running the Blueprint.

![Log in](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-10.png)

Go to the list of dashboards. 

![Go to the list of dashboards](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-11.png)

Iot sandbox provides a smaple dashboard, that will display any data that comes into the container. You will naturally be able to create your own dashboards, customize this one or add data filters (in case you are sending data from different sensors, for instance). Check [Grafana's documentation](http://docs.grafana.org/) to learn more about it.

![Access the default dashboard](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-12.png)

As there is no data coming in, at first the dashboard will be empty.

![Empty panels](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-13.png)


### 3. Start sending data!

Now you can start sending data from whatever MQTT-enabled device, equipment or software you use. If you want to send simulated data, please check [this wiki page](https://github.com/subutai-blueprints/iot-sandbox/wiki/Testing-this-BP) about how to use node-red to send random data.

![Populated dashboard](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-16.png)

### 5. Do more with IoT sandbox

As with any other BP environment, IoT sandbox can be extended using the power of its open source base: InfluxDB, Telegraf, Grafana - and virtually any other software you can run on its Debian Stretch operating system. You have full admin access to all of those, out of the box. Check some useful resources below:

- [Grafana documentation](http://docs.grafana.org/).
- [InfluxDB documentation](https://docs.influxdata.com/influxdb/v1.6/).
- [Telegraf documentation](https://docs.influxdata.com/telegraf/v1.7/).
- [MQTT documentation](http://mqtt.org/documentation).
