# Azure Stream Analytics

### Create hub
```bash
# environments
export rg="ectrainstreamrg"
export loc="northeurope"
export evtns="ecstreaming01"
export evthn="myhub01"

az group create -n $rg -l $loc

#Create eventhub namespace (endpoint)
az eventhubs namespace create -n $evtns -g $rg -l $loc

#create event hub or iot hub
az eventhubs eventhub create -n $evthn -g $rg --namespace-name $evtns
```

### Pyhton script to send some events
Microsoft docs [link](https://docs.microsoft.com/en-us/azure/event-hubs/event-hubs-python-get-started-send)

#### Install library

```bash
pip install azure-eventhub
```

#### Sample
Run nano from bash and create send.py file

```python
import sys
import logging
import datetime
import time
import os
import json
import random

from azure.eventhub import EventHubClient, Sender, EventData

logger = logging.getLogger("azure")

# Address can be in either of these formats:
# "amqps://<URL-encoded-SAS-policy>:<URL-encoded-SAS-key>@<mynamespace>.servicebus.windows.net/myeventhub"
# "amqps://<mynamespace>.servicebus.windows.net/myeventhub"
# For example:
ADDRESS = "amqps://<EVENTHUBS NAMESPACE NAME>.servicebus.windows.net/<EVENTHUB NAME>"

# SAS policy and key are not required if they are encoded in the URL
USER = "RootManageSharedAccessKey"
KEY = "<SHARED ACCESS KEY FOR THE EVENT HUBS NAMESPACE>"

try:
    if not ADDRESS:
        raise ValueError("No EventHubs URL supplied.")

    # Create Event Hubs client
    client = EventHubClient(ADDRESS, debug=False, username=USER, password=KEY)
    sender = client.add_sender(partition="0")
    client.run()
    try:
        start_time = time.time()
        for i in range(100):
          reading = {'source': 'myStaticSensor', 'id': 1, 'timestamp': str(datetime.datetime.utcnow()), 'uv': random.random(), 'temperature': random.randint(0, 100), 'humidity': random.randint(70, 100)}
          message = json.dumps(reading)
            print("Sending message: {}".format(i))
            # message = "Message {}".format(i)
            sender.send(EventData(s))
    except:
        raise
    finally:
        end_time = time.time()
        client.stop()
        run_time = end_time - start_time
        logger.info("Runtime: {} seconds".format(run_time))

except KeyboardInterrupt:
    pass
```

Run sample
```bash
start python send.py
```


## Labs
Courseware lab ingest and analyze data from blobstorage [link](https://github.com/MicrosoftLearning/DP-200-Implementing-an-Azure-Data-Solution/blob/master/instructions/dp-200-06_instructions.md)
IoT and Stream Analytics [link](https://github.com/microsoft/computerscience/tree/master/Labs/Internet-of-Things)

