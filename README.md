# fluentd-pushover

If any Container is issuing an error or fails with some task you will get prompted with an Pushover notficitaion.

> Change User and Acc in the config file or pass the Vars to the container.

Exmaple on how to use:
```
version: '2'
services:
  ping:
      image: dockercloud/hello-world
      expose:
       - "80/tcp"
      logging:
       driver: "fluentd"
       options:
         fluentd-address: "10.0.0.10:24224"
```

You can test the stack by exec into the hello-world container and executing an "logger fail"
