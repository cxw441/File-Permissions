# File-Permissions

The chmod (short for change mode) command is used to manage file system access permissions on Unix and Unix-like systems. Effect of Permissions on Files: 

| Permission    |  Character            | Meaning on File                                                             |
| ------------- | ----------------------| --------------------------------------------------------------------------- |
| Read          | r                     | The file is readable                                                        |
|               | -                     | The file is not readable. You cannot view the file contents.                |
| Write         | w                     | The file can be changed or modified.                                        |
|               | -                     | The file cannot be changed or modified.                                     |
| Execute       | e                     | The file can be executed.                                                   |
|               | -                     | The file cannot be executed.                                                |

In the example above (rw-r--r--) means that the file owner has read and write permissions (rw-), the group and others have only read permissions (r--).
