# ARM Template for Event Hub

This is an ARM template for deploying an Azure Event Hub and its namespace. The Event Hub is used to process and store large amounts of data and messages.

## Parameters

The following parameters are used in this template:

- `eventHubNamespaceName`: The name of the Event Hub namespace.
- `eventHubName`: The name of the Event Hub.
- `eventHubPartitionCount`: The number of partitions for the Event Hub.
- `eventHubConnectionString`: The connection string for the Event Hub.
- `eventHubSASToken`: The shared access token for the Event Hub.
- `location`: The location of the Event Hub and namespace.

## Resources

This template deploys the following resources:

- An Azure Event Hub namespace with the specified name and location.
- An Azure Event Hub with the specified name and partition count, within the previously deployed namespace.

## Outputs

This template returns the following outputs:

- `eventHubConnectionString`: The connection string for the Event Hub.
- `eventHubSASToken`: The shared access token for the Event Hub.

## Usage

az deployment group create --resource-group <resource-group-name> --template-file <template-file-name>.json --parameters eventHubNamespaceName=<value> eventHubName=<value> eventHubPartitionCount=<value> eventHubConnectionString=<value> eventHubSASToken=<value> location=<value>


