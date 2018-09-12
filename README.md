# IoT sandbox

Blueprint of useful IoT software for the [Subutai Platform](https://subutai.io) 

## How to use this product

IoT sandbox allows you to spin up an online environment with simple steps. It's just a matter of inserting your desired usernames and passwords, and then clicking "next next finish".  Once the environment is up, everything is ready.

Data can then be sent from IoT devices via [mqtt](https://en.wikipedia.org/wiki/MQTT), a lightweight messaging protocol commonly supported by both DIY kits and professional equipment. Sensors, Raspberry Pis and other devices will be able to send data directly into the Subutai environment in which the BP is run. The data is gathered by [Telegraf](https://www.influxdata.com/time-series-platform/telegraf/) and automatically stored on [InfluxDB](https://www.influxdata.com/time-series-platform/influxdb/). The user can then create dashboards for data visualization using [Grafana](http://grafana.org/). All the software needed comes already installed and preconfigured by the Blueprint.

### 1. Run the Blueprint on Subutai

![Set your Blueprint variables](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP-02.png)

![Select a Peer](docs/BP03.png)

![Check the exposed port](docs/BP04.png)

![Build the Environment](docs/BP05.png)

![Wait some minutes](docs/BP06.png)

![Your environment is ready!](docs/BP07.png)

![Port mapping tab](docs/BP08.png)

### 2. Check Grafana

![Access Grafana](docs/BP09.png)

![Log in](docs/BP10.png)

![Go to the list of dashboards](docs/BP11.png)

![Access the default dashboard](docs/BP12.png)

![Empty panels](docs/BP13.png)

Now we will enable the environment to receive data.

### 3. Create a port mapping 

![Add new port](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP14.png)

![Define variables](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP15.png)

### 4. Start sending data!

![](https://github.com/subutai-blueprints/iot-sandbox/raw/master/docs/BP16.png)
