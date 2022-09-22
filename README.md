# Ansible-WSUS-GetNeededUpdate
Get All Needed Update from remote Windows Server 

# Vars Needed
ansible_path: /source/tower/wsus
windows_path : C:\Temp
windows_file_name: wsus_extract

# Step by Step
1/ Executes a powershell script on the remote host to retrieve the list of updates installed on the host and stores the result in a file
2/ Creates a folder on the node to accommodate the next two files
3/ Read the file stored on the remote host
4/ Creates the header of the csv file for the installed KBs
5/ Adds the lines to the csv file
6/ Deletes the file on the remote host
7/ Retrieves & stock the status of the WSUS service
8/ Enables the wsus service if necessary
9/ Start the wsus service if necessary
10/ Execute a powershell script that retrieves the number of updates needed from the remote server & stock it
11/ Retrieves the target group in WSUS
12/ Retrieves the uptime server
13/ Creates the header of the csv file for the Needed Update file
14/ Adds the lines to the csv file
15/ Stop the wsus service if necessary
16/ Disable the wsus service if necessary
