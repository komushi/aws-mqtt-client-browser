# AWS Websocket Pub/Sub client - browserified and babelified version

## Build from ES2016 and node.js module to browser-enabled ES5 module
```
$ npm run build
```


## Basic usage

```
<html>
  <body>
      <script src="./aws-mqtt-client-browser.js"></script>

        <script type="text/javascript">


            const mqttClient = new AWSMqtt({
                accessKeyId: AWS_ACCESS_KEY,
                secretAccessKey: AWS_SECRET_ACCESS_KEY,
                sessionToken: AWS_SESSION_TOKEN,
                endpointAddress: AWS_IOT_ENDPOINT_HOST,
                region: 'ap-northeast-1'
            });

            mqttClient.on('connect', () => {
                mqttClient.subscribe('iotbutton/001');
                console.log('connected to iot mqtt websocket');
            });

            mqttClient.on('message', (topic, message) => {
                console.log(message.toString());
            });


        </script> 
  </body>
</html>
```

## TODO: Installing it from bower

````

````

### Complete [MQTT.js API](https://github.com/mqttjs/MQTT.js#api)

## Credits
Based on [AWS Websocket Pub/Sub client](https://github.com/jimmyn/aws-mqtt-client).