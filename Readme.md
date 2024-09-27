## Exercise_9-Keyboard_Automation-Simulate_Keystrokes

## Aim:

To simulate typing and keyboard shortcuts in a desktop application (Notepad) using Start Process, Type Into, and Send Hotkey activities in UiPath Studio.

## Equipment Required:

UiPath Studio installed on your computer.<br>
Notepad application (pre-installed on Windows).<br>
Computer with:<br>
Minimum 4 GB RAM.<br>
Minimum 2.0 GHz CPU.<br>
Windows operating system.

## Procedure:

### Create a New Process in UiPath Studio:

Open UiPath Studio and create a new project by selecting Process under the New Project tab.<br>
Name the process (e.g., Notepad Automation) and click Create.

### Start the Notepad Application:

Search for the Start Process activity in the Activities panel and drag it into the Main sequence.<br>
In the FileName property of Start Process, enter the path to the Notepad executable (notepad.exe):<br>

```
notepad.exe
```

This activity will launch Notepad when the automation runs.

### Simulate Typing Text into Notepad:

After launching Notepad, use the Type Into activity to simulate typing.<br>
Drag the Type Into activity into the sequence under the Start Process activity.<br>
Click Indicate on Screen and select the main text area of Notepad.<br>
In the Text property, enter the text you want to simulate typing, such as:<br>

```
This is a sample text.
```

Make sure to check the SimulateType option in the Properties panel for faster, invisible typing.

### Simulate Save Shortcut (Ctrl + S):

To simulate the Save keyboard shortcut (Ctrl + S), use the Send Hotkey activity.<br>
Drag the Send Hotkey activity below the Type Into activity.<br>
Click Indicate on Screen and select the Notepad window again.<br>
Set the Key property to Ctrl + S, which will open the Save As dialog.

### Simulate Typing the File Name:

After pressing Ctrl + S, the Save As dialog will appear where you can type the file name.<br>
Use another Type Into activity to enter the filename.<br>
Click Indicate on Screen and select the filename input field in the Save As dialog box.<br>
In the Text property, enter the desired file path and name.<br>
Check the SimulateType option to type the filename faster.

### Press Enter to Save the File:

To confirm saving, use another Send Hotkey activity for the Enter key.<br>
Drag the Send Hotkey activity under the Type Into activity for the filename.<br>
Click Indicate on Screen and select the Save As dialog box.<br>
Set the Key property to Enter, which will save the file.

### Save and Run the Workflow:

Press CTRL+S to save the workflow.<br>
Click the Run button to execute the automation.<br>
UiPath will launch Notepad, type the text, save the file, and close the application automatically.

## UiPath WorkFlow:

![alt text](<img/Screenshot 2024-09-27 183413.png>)
![alt text](<img/Screenshot 2024-09-27 183646.png>)
![alt text](<img/Screenshot 2024-09-27 183814.png>)
![alt text](<img/Screenshot 2024-09-27 183914.png>)
![alt text](<img/Screenshot 2024-09-27 183958.png>)
![alt text](<img/Screenshot 2024-09-27 184103.png>)
![alt text](<img/Screenshot 2024-09-27 184156.png>)
![alt text](<img/Screenshot 2024-09-27 184314.png>)
![alt text](<img/Screenshot 2024-09-27 184350.png>)
![alt text](<img/Screenshot 2024-09-27 190008.png>)

## Result:

The text is typed into Notepad, saved with a given filename, and Notepad is closed using keyboard shortcuts, all simulated through UiPath automation.
