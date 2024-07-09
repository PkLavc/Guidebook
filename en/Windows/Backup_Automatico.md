# How to Configure and Run Automatic Backup on Windows using xcopy

To automate the backup process in Windows, you can use the `xcopy` command in Command Prompt. Below is an example of how to configure and run a backup from a source to a specific destination.

## Steps to Configure Automatic Backup:

### 1. Define Origin and Destination:

Open Notepad or a text editor and set the variables for the backup source and destination:

@echo off
set origin=C:\Path\To\Origin
set destination=E:\Destination

### 2. Run the xcopy Command:

After defining the variables, add the `xcopy` command to copy the files from source to destination:

xcopy "%source%" "%destination%" /E /Y

### Example:

@echo off  
set origin_backup=C:\Documents\Backup  
set destination_backup=E:\Documents  

set origin_miscellaneous=C:\Users\MICRO\Desktop\Class  
set destination_diverse=E:\Class  

xcopy "%source_backup%" "%destination_backup%" /E /Y  
xcopy "%miscellaneous_source%" "%miscellaneous_destination%" /E /Y  

### 3. Explanation of Commands:

- `%origin%`: Replace this variable with the actual path of the folder you want to backup.
- `%destination%`: Replace this variable with the actual path of the destination folder where you want to store the backup.
- `/E`: Copies directories and subdirectories, including empty directories.
- `/Y`: Suppresses the request to confirm overwriting an existing file.
-
### 4. Save the Configuration File:

After defining the variables in Notepad or your preferred text editor, follow these steps to save the file with a `.bat` extension so that Windows recognizes and runs it correctly:

1. **Click on "File"** in the top menu of Notepad.
2. **Select "Save As..."** from the drop-down menu.
3. **Name the file** with a descriptive name, for example, `ScriptDeBackup.bat`.
4. **Choose the location** where you want to save the file.
5. In the **"Save as type"** field, select **"All files (\*.\*)"**.
6. **Click "Save"** to save the file.

Make sure the file extension is `.bat` so that Windows recognizes it as an executable script.

### Configuring Automatic Backup:

You can set the backup to start automatically using Windows Task Scheduler. Here are some common scenarios:

#### When Starting the Computer:

1. **Create a New Task in Task Scheduler**:
 - Open Task Scheduler (`taskschd.msc`).
 - Click "Create Task..." on the right panel.
 - In the "General" tab, configure a name for the task, for example, "Automatic Backup".
 - Check the option "Run with the highest permissions".

2. **Configure the Trigger**:
 - In the "Triggers" tab, click "New...".
 - Choose "When starting" under "Start task".
 - Confirm and adjust other settings as needed (e.g. delay).

3. **Configure the Action**:
 - In the "Actions" tab, click "New...".
 - Configure the action to launch the Command Prompt (`cmd.exe`).
 - In the "Add arguments (optional)" field, enter the full path of your backup script:
 ```batch
 /c "C:\Path\To\Your\BackupScript.bat"
 ```

#### 5 Minutes After Computer Starts:

1. **Create a New Task in Task Scheduler**:
 - Repeat the steps above to create a new task.

2. **Configure the Trigger**:
 - Choose "When starting" under "Start task".
 - In "Advanced Trigger Settings", set a delay of 5 minutes.

3. **Configure the Action**:
 - Repeat the steps above to configure the action with the backup script.

#### Every Day at 10:00:

1. **Create a New Task in Task Scheduler**:
 - Repeat the steps above to create a new task.

2. **Configure the Trigger**:
 - Choose "Daily" in "Start task".
 - Set the time to 10:00 am.

3. **Configure the Action**:
 - Repeat the steps above to configure the action with the backup script.

Be sure to save and test each task you create in Task Scheduler to ensure the automatic backup is running as expected.
