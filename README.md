This Project is fully un attended and has 3 automation that call each other using "start process" activity.

1-The 1st automation: On EventTriger on google drive, if a file is added the first automation starts:

Download the excel file, send notification of the process status that the automation started and starts the next automation.

2- The 2nd automation: REFramework_Dispatcher starts and gets the data from the excel file, pushes it to a queue, sends notifications and starts the performer.

3- The 3rd automation: REFramework_Performer gets the data from the queue, processes it and writes it to the excel file and send notifications.

*The SendNotifications is a separate Library puplished to orchestrator and only called at the end of each automation.

*The descriptors/selectors that the performer uses are all and only in ObjectRepository.
