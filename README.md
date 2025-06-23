The actual Prove repo is invite only, but have I put some of the code I have written for Prove on this repo.
The code has two main purposes:

1. Allow sensors nodes to collect and send their data in a consistent way using CAN Bus. To add a new sensor, you only need to:
  1. define parameters for it in a text file (sensors.def)
  2. Run codeGen_main.py to make files, and place them into the sensors folder.
  3. Fill in the collect<Name of Data> functions in the main file for your new sensors

2. Allow vitals, a node responsible for ensuring everything is running as expected, too moniter the data, and send heartbeat messages to each node.
 Vitals will raise warning, potentially disconnecting the high-voltage battery if it identifies a problem
