---
title: All is Well?
order: 7
requirements:
  build: vertice
  plan: free
---

Now that you have configured to your hearts content, its time to see if the `individual` and the `sum of individual` are up and ready to go.

---

### Console (UI - Nilavu)

- https://localhost:3000

You'll see a cool UI.

The log files are located in */var/log/verticenilavu/unicorn.log*


### API - gateway

- http://localhost:9000

~~~json
{
  "about" : {
    "git_version" : "cd06b88e292f4141c000a28a5a4e89fedc4be9e8",
    "git_branch" : "1.5"
  },
  "status" : {
    "nsq" : "up",
    "cassandra" : "up"
  },
  "runtime" : {
    "total_mem" : "900 MB",
    "freemem" : "654 MB",
    "cores" : "8",
    "freespace" : "35 of 93 GB"
  }
}
~~~

The log files are located in  */var/log/verticegateway/*


### Omnischeduler

- http://localhost:7777

You'll see a web page.

The log files are located in */var/log/vertice*

#### *optional* Cassandra

Please replace `192.168.0.116` with  your ip address.

~~~bash

$ cqlsh <192.168.0.116> -u vertadmin -p vertadmin
Connected to Test Cluster at 192.168.0.116:9042.
[cqlsh 5.0.1 | Cassandra 3.7 | CQL spec 3.4.2 | Native protocol v4]
Use HELP for help.
vertadmin@cqlsh>

~~~

#### *optional* NSQ

- http://localhost:7777

You'll see a web page.

#### OpenNebula

- http://localhost:9869

You'll see a web page.

If you reach this steps then, it truly is ~ALL is Well.
{: .info}
