The actual Prove repository is invite-only, but I have included some of the code I wrote for Prove in this repository.
The code has two main purposes:

1. Allow sensor nodes to collect and send their data in a consistent way using CAN Bus. To add a new sensor, you only need to:
   
   a. Define parameters for it in a text file (sensors.def)
   
   b. Run codeGen_main.py to generate files and place them in the sensors folder.
   
   c. Fill in the collect<Name of Data> functions in the main file for your new sensors to collect the data.

2. Allow Vitals, a node responsible for ensuring everything is running as expected, to monitor the data and send heartbeat messages to each node.
 Vitals will raise a warning, potentially disconnecting the high-voltage battery if it identifies a problem
