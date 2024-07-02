Microsoft Azure Predictive Maintenance Simulation Data

########################################################################################################################################################
### 														Context / Background																	 ###
########################################################################################################################################################

This an example data source which can be used for Predictive Maintenance Model Building. It consists of the following data:
- total of 5 csv files
- Machine conditions and usage: The operating conditions of a machine e.g. data collected from sensors.
- Failure history: The failure history of a machine or component within the machine.
- Maintenance history: The repair history of a machine, e.g. error codes, previous maintenance activities or component replacements.
- Machine features: The features of a machine, e.g. engine size, make and model, location.

########################################################################################################################################################
### 														Data / File Descriptions   																 ###
########################################################################################################################################################

- **Telemetry Time Series Data (PdM_telemetry.csv)**: It consists of hourly average of voltage, rotation, pressure, vibration collected from 100 machines for the year 2015.

- **Error (PdM_errors.csv)**: These are errors encountered by the machines while in operating condition. Since, these errors don't shut down the machines, these are not considered as failures. The error date and times are rounded to the closest hour since the telemetry data is collected at an hourly rate.

- **Maintenance (PdM_maint.csv)**: If a component of a machine is replaced, that is captured as a record in this table. Components are replaced under two situations: 1. During the regular scheduled visit, the technician replaced it (Proactive Maintenance) 2. A component breaks down and then the technician does an unscheduled maintenance to replace the component (Reactive Maintenance). This is considered as a failure and corresponding data is captured under Failures. Maintenance data has both 2014 and 2015 records. This data is rounded to the closest hour since the telemetry data is collected at an hourly rate.

- **Failures (PdM_failures.csv)**: Each record represents replacement of a component due to failure. This data is a subset of Maintenance data. This data is rounded to the closest hour since the telemetry data is collected at an hourly rate.

- **Metadata of Machines (PdM_Machines.csv)**: Model type & age of the Machines.

########################################################################################################################################################
### 														Technical Assessment Tasks 																 ###
########################################################################################################################################################
- prepare a presentation (can be Powerpoint / Google Slides / Jupyter Notebook / Markdown) to provide your finding with the following results

- ** Part 1 Hypothesis testing ** - derive 2 hypothesis of your choice using the 5 csv provided
Example hypothesis 1 -- 60% of the machine exhibited Error 1 90% of the time from 2015 to 2018
Example hypothesis 2 -- 80% of machine type 2 failed within the first 50% of their "life span"

- ** Part 2 model building and evaluation ** - forecast the voltage ('volt') of machineID = 68 (provide the forecasting uncertainty) for 6 hour after '2015-12-13 00:00:00' (i.e. between '2015-12-13 00:00:00' to '2015-12-13 06:00:00')

########################################################################################################################################################
### 														Technical Assessment Factors															 ###
########################################################################################################################################################
- ** Part 1 Hypothesis testing ** - your capability in hypothesis formation, statistics, visualization and exploratory data analysis approach
- ** Part 2 model building and evaluation ** your thought process to select proper forecasting techniques, how you evaluate their performance, what assumption(s) do you use to draw conclusion about the result
- the practicality of your approach on both parts (e.g. balancing interpretability vs predictability vs model robustness) 
- any next step you are proposing?

### Acknowledgements
This dataset was available as a part of **Azure AI Notebooks for Predictive Maintenance**. 


### Inspiration

Try to use this data to build Machine Learning models related to Predictive Maintenance.