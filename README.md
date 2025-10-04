Python Alarm Clock using Tkinter
This project is a desktop-based alarm clock application built using Python and Tkinter, designed to help users set alarms, view the current time, and snooze alarms. It demonstrates how to create interactive GUI applications with real-time features using Python.

How It Works

1. Graphical User Interface (GUI)
The application is built using Tkinter and provides an intuitive and responsive interface:
Displays the current time, updating every second.
Includes dropdown menus to select the alarm hour, minute, second, and AM/PM.
Provides buttons to set the alarm and to snooze it.
The GUI layout is simple and user-friendly, making it easy to interact with the clock.

2. Current Time Display
The update_time function updates the current system time every second using Tkinter’s after() method.
This ensures the displayed time is always accurate without freezing the GUI.

3. Alarm Functionality
The user sets an alarm using the dropdown menus.
Clicking Set Alarm starts a new thread (Threading function) that continuously checks the current time in the background.
The myalarm function compares the current system time with the user-set alarm time.

4. Snooze Feature
Clicking Snooze +2 min adds 2 minutes to the currently set alarm.
Handles minute and hour overflow, and updates the AM/PM period if needed.
After snoozing, the alarm thread restarts, so the alarm rings again at the new time.

5. Threading for Responsiveness
The alarm check runs in a separate thread using Python’s threading module.
This keeps the GUI responsive while continuously checking the time in the background.


Key Components

Tkinter Widgets: Labels, Buttons, Frames, OptionMenu for building the GUI.
StringVar: Stores and updates values of hours, minutes, seconds, and AM/PM dynamically.
Winsound: Plays the alarm sound when the alarm time is reached.
Threading: Runs the alarm check in parallel so the GUI does not freeze.
Datetime & Time Modules: Used for fetching and comparing the current time with the set alarm time.
