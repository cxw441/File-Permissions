# File-Permissions

The chmod (short for change mode) command is used to manage file system access permissions on Unix and Unix-like systems. 

| Mode          |  Character            | Meaning on File                                                             |
| ------------- | ----------------------| --------------------------------------------------------------------------- |
| Read          | r                     | The file is readable                                                        |
|               | -                     | The file is not readable. You cannot view the file contents.                |
| Write         | w                     | The file can be changed or modified.                                        |
|               | -                     | The file cannot be changed or modified.                                     |
| Execute       | e                     | The file can be executed.                                                   |
|               | -                     | The file cannot be executed.                                                |

In the example above (rw-r--r--) means that the file owner has read and write permissions (rw-), the group and others have only read permissions (r--).


Effect of Permissions on Files: 

chmod [references][operator][modes] FILENAME...

| Reference   |  Class             | Description                                                           |
| ----------- | -------------------| --------------------------------------------------------------------- |
| u           |  user              | file owner                                                            |
| g           |  group             | members of the file's group                                           |
| o           |  others            | users who are neither the file's owner nor members of the file's group|
| a           |  all               | all three of the above, same as ugo                                   |

| Operator   |  Description                                                                    |
| -----------| --------------------------------------------------------------------- --------- |
| +          |  adds the specified modes to the specified classes                              |
| -          |  removes the specified modes from the specified classes                         |
| =          |  the modes specified are to be made the exact modes for the specified classes   |


To add the execute permission for the user: chmod u+x FILENAME 

To remove the write permission for others: chmod o-w FILENAME


Effect of Permissions on Directories (Folders): 

chmod [references][operator][modes] DIRECTORYNAME...

chmod -R u+rw,g-,o-rx DIRECTORYNAME means that Recursively (i.e. on all files and directories in DIRECTORYNAME) adds read, write permissions for User, removes read, write, and execution permissions for Group, and removes read and execution permissions for Others

Task: chmod uog-w -R Michael_MDM2*



