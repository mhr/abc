# Kafka

The [Kafka](https://kafka.apache.org/) adaptor is capable of tailing in realtime one or more topics.

Here is how a configuration file looks like:

```ini
src_type=kafka
src_uri=kafka://user:pass@SERVER:PORT/TOPIC1,TOPIC2
tail=false

dest_type=elasticsearch
dest_uri=APP_NAME
# dest_uri=https://USER:PASSWORD@SERVER/INDEX
```

The equivalent CLI command looks like:

```sh
abc import --src_type=kafka --src_uri="kafka://localhost:9200/newtopic" myAppbaseApp
```

If no topic is specified in the `src_uri` path either in the config or in the CLI switch, data from all topics will be tailed.

**Note:** `myAppbaseApp` should already exist. Or you can create a new app with the [`abc create`](https://github.com/appbaseio/abc/blob/dev/docs/appbase/create.md) command and use that.
