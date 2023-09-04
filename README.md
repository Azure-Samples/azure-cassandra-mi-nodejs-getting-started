---
page_type: sample
languages:
- javascript
products:
- azure
description: "Azure Managed Instance for Apache Cassandra provides automated deployment and scaling operations for managed open-source Apache Cassandra datacenters."
urlFragment: azure-cassandra-mi-nodejs-getting-started
---

# Accessing Azure Managed Instance for Apache Cassandra using Node.js
Azure Managed Instance for Apache Cassandra provides automated deployment and scaling operations for managed open-source Apache Cassandra datacenters. It accelerates hybrid scenarios and reduces ongoing maintenance.

This quick start demonstrates how to connect to a Cassandra Managed instance cluster with Node.js. You'll then build a user profile console app, output as shown in the following image, with sample data.


## Running this sample
* Before you can run this sample, you must have the following pre-requisites:
	* An Azure Managed Instance for Apache Cassandra cluster. Check out our Quickstart guide [here](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/create-cluster-portal).
    * Networking access from this application to your Azure Managed Instance for Apache Cassandra cluster (the service only deploys private IP addresses injected into a Virtual network).
	* [Node.js](https://nodejs.org/en/) version v0.10.29 or higher.
	* [Git](http://git-scm.com/).
  * [Node.js driver for apache cassandra](https://github.com/datastax/nodejs-driver) // to install the driver - run npm install cassandra-driver.


1. Clone this repository:

    ```bash
	git clone git@github.com:Azure-Samples/Azure-Samples/azure-cassandra-mi-node-getting-started.git cassandrami
    ```

1. Change directories to the repo:

    ```bash
    cd cassandrami
    ```

1. Install npm dependencies:

    ```bash
    npm install
    ```

1. Next, substitute the contactPoint, username, password, and localDataCenter values in `config.js` with your corresponding Azure Managed Instance for Apache Cassandra values.

    ```javascript
    module.exports = {
            username: "Cassandra cluster username",
            password: "Cassandra cluster password",
            contactPoint: "I.P. address of a node in your cluster",
            keySpace: "uprofile",
            localDataCenter: "datacenter-1"
    };
    ```

1. Run `uprofile.js` in a terminal to start your start your node application:

    ```bash
	npm start
	```

## About the code
The code included in this sample is intended to get you quickly started with a Node.js console application that connects to Azure Managed Instance for Apache Cassandra.
