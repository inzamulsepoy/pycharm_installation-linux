# pycharm_installation-linux
Pycharm Installation and run from anywhere in linux

#Download Pycharm Community Version from its official website<br>
exctract from the /home/user/Downloads directory<br>
open the exctrated directory<br>
go to bin folder<br>
open terminal from there<br>
write the below command
```
./pycharm
```

#or create BASH file to run it from the homme directory


Here's a simple Bash script to navigate to the PyCharm directory and launch it:  

### Steps to create and use the script:
1. Open a terminal.
2. Create a new script file:
   ```bash
   nano launch_pycharm.sh
   ```
3. Copy and paste the following script into the file:

   ```bash
   #!/bin/bash

   # Navigate to the PyCharm bin directory
   cd /home/user/Downloads/pycharm-community-2024.3.2/bin || exit

   # Run PyCharm
   ./pycharm
   ```

4. Save the file (`CTRL+X`, then `Y`, then `Enter`).
5. Give the script execution permission:
   ```bash
   chmod +x launch_pycharm.sh
   ```
6. Run the script:
   ```bash
   ./launch_pycharm.sh
   ```

#or create BASH file to run it from any directory

This will open PyCharm automatically from the specified directory. 🚀

You can create a Bash script that allows you to run `pycharm.sh` from anywhere by adding an alias or modifying your `~/.profile` file. Here's a script for that:  

### Steps to Create the Script  

1. Open a terminal and create a new script:  
   ```bash
   nano run_pycharm.sh
   ```  

2. Add the following content:  

   ```bash
   #!/bin/bash

   # Navigate to the home directory and source ~/.profile
   cd ~ || exit
   source ~/.profile

   # Run the PyCharm script located in the home directory
   bash ~/pycharm.sh
   ```

3. Save the file (`CTRL+X`, then `Y`, then `Enter`).  

4. Give execution permission:  
   ```bash
   chmod +x run_pycharm.sh
   ```

5. Move the script to `/usr/local/bin/` so it can be run from anywhere:  
   ```bash
   sudo mv run_pycharm.sh /usr/local/bin/pycharm
   ```

6. Now you can run PyCharm from anywhere using:  
   ```bash
   pycharm
   ```

This script ensures that your `~/.profile` is sourced before running `pycharm.sh` from the home directory. 🚀
