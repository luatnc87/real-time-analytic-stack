# real-time-analytic-stack
Welcome to Real Time Analytics Stack! This repo showcases a complete real-time analytic stack using popular open-source tools.

In this tutorial, I demonstrate how to use Docker Compose to quickly set up a real time data analytic stack using Apache SeaTunnel, Doris and Superset. The pipeline uses SeaTunnel to ingest real-time CDC event from MySQL database into Doris data warehouse (You can transform the data with dbt) and visualize the data with Superset.

# Components of the Real Time Analytic Data Stack
Before we set up the project, let’s briefly look at each tool used in this example of a real-time data analytic stack to make sure you understand their responsibilities.

# Apache SeaTunnel

# Apache Doris

# Apache Superset
Apache Superset is a modern business intelligence, data exploration and visualization platform. Superset connects with a variety of databases and provides an intuitive interface for visualizing datasets. It offers a wide choice of visualizations as well as a no-code visualization builder. You can run Superset locally with Docker Compose or in the cloud using Preset. Superset sits at the end of this modern data stack example and is used to visualize the data stored in Apache Doris.

# Pre-requisites
To follow along, you need to: 

**Install Docker and Docker Compose in your machine**. You can follow [this guide](https://docs.docker.com/engine/install/?_gl=1*187dp4*_ga*MTAzNDgyNDI0My4xNjkzNDY2NDcy) to install Docker and [this one](https://docs.docker.com/compose/install/?_gl=1*187dp4*_ga*MTAzNDgyNDI0My4xNjkzNDY2NDcy) to install Docker Compose.

# Using Docker Compose to Bootstrap a Real Time Data Analytic Stack
This tutorial uses Docker Compose and a shell script to set up the required resources. Docker saves you from installing additional dependencies locall. You can quickly start and stop the instances.

The shell script **setup.sh** provides two commands, *up* and *down*, to start and stop the instances. The compose files are stored in *seatunnel/docker-compose-seatunnel.yaml*, *doris/docker-compose-doris.yaml*, and *superset/docker-compose-superset.yaml*. You can go through these files and make any necessary customization, for example, changing the ports where the instances start or installing additional dependencies.

## Setting up Apache SeaTunnel

## Setting up Apache Doris

## Setting up Apache Superset
One the *setup.sh* command has completed, visit *http://localhost:8088* to access the Superset UI. Enter *admin* as username and password. Choose Apache Doris from the supported database drop-down, then provide information to finish connection configuration.

# Using the Real Time Data Analytic Stack
One the stack is ready and running, you can start using it to ingest and process your data.

## Sync real-time CDC event from MySQL database into Apache Doris DWH

## Create a materialized view to near real-time aggregate data

## Visualize data on dashboard using Superset


## Cleaning up


# Conclusion


## About the author



