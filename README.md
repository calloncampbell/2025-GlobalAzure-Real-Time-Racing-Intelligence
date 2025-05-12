# Real-Time Racing Intelligence: Harnessing Azure Data Explorer & Event Hubs for Forza Motorsport / Formula 1 Telemetry

![](./assets/2025-global-azure-toronto.png)

## Overview
This is my presentation I did for the Global Azure 2025 event in Toronto. Real-Time Racing Intelligence: Harnessing Azure Data Explorer & Event Hubs for Forza Motorsport / F1 Telemetry.

  ![](./assets/Architecture-1.png)

Here is the medallion architecture for the telemetry data:

  ![](./assets/forza-motorsport-real-time-intelligence-architecture.png)

Here is the real-time dashboard in Azure Data Explorer to view the driver and track performance:

  ![](./assets/Dashboard.png)


## Requirements
- Forza Mortorsport - Xbox or PC (included with [XBox Game Pass](https://www.xbox.com/en-ca/xbox-game-pass))
- .NET 8
- Forza-Telemetry-Bridge (https://github.com/clemensv/forza-telemetry-bridge)
  - I added some additional telemetry channels, so demo is based on my fork (https://github.com/calloncampbell/forza-telemetry-bridge) 
- Azure Subscription (sign up for [free](https://azure.microsoft.com/en-us/free))
- Azure Data Explorer (get a [free personal cluster](https://dataexplorer.azure.com/))

## Setup
1. Download the Forza-Telemetry-Bridge and follow its installation and configuration.
1. Configurat Forza Mortorsport to emit telemetry by going into Settings and enableing the UDP Telemetry. Set the IP and Port and data format accordingly. See Forza-Telemtry-Bridge for details.
1. Create a free Azure Data Explorer Cluster and create a new database.
1. Run the KQL scripts from this repository `src` folder to create the tables, functions and materialized views.
1. Create an Azure Data Explorer Dashboard. There is a dashboard file in this repository `src` folder, just import it and update the data source accordingly.
1. Run the Forza-Telemetry-Bridge console application.
1. Start a race.
1. Analyze your results.

## YouTube
Here is a video I published for one of my racing sessions and then displaying the results in a real-time dashboard:
https://youtu.be/3URkoaY6ogc
