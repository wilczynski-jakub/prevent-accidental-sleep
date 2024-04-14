# Tasker: Prevent accidental sleep
If you have ever felt so tired in the evening that you fell asleep accidentally, without setting a wake-up alarm - then this Tasker project is for you!


## Prerequisites
Make sure you have [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en_US) installed on your device _(it is available on Android)_.
<br>
![Tasker](screenshots/tasker.png)


## Main project files

### [.prf.xml](.prf.xml)
It is a Tasker ***Profile*** that initializes the _%DISPLAY_OFF_TIME_ variable - each evening, in order to activate the [Prevent accidental sleep Profile](.prf.xml).

#### ![Profile](screenshots/profile.png)
![Profile](screenshots/profile.png)

### [.prf.xml](.prf.xml)
It is a Tasker ***Profile*** that runs the [Prevent accidental sleep Task](.tsk.xml) each 2 minutes in the evening, when the _%DISPLAY_OFF_TIME_ variable is initialized (assuming that the variable is cleared once you've gone to sleep *intentionally*).

#### ![Profile](screenshots/profile.png)

### [.tsk.xml](.tsk.xml)

This is the main project task, that calculates for how long the phone has been locked but only when you're at your home location. It assumes that having it locked for more than _%MAX_DISP_OFF_TIME minutes (at home, in the evening) means you're falling asleep *unintentionally*.
<br>
Once the *accidental sleep* is detected, the [Evening Routine Task](.tsk.xml) is run.

### [.tsk.xml](.tsk.xml)

The Evening Routine Task might perform any custom actions. In this example, it asks you to:
* set a wake up alarm,
* brush your teeth.

#### ![Profile](screenshots/profile.png)


## Helper tasks

### [Task_1.tsk.xml](Task_1.tsk.xml)
#### ![Task 1](screenshots/task-1.png)

### [Task_2.tsk.xml](Task_2.tsk.xml)
#### ![Task 2](screenshots/task-2.png)

### [Task_3.tsk.xml](Task_3.tsk.xml)
#### ![Task 3](screenshots/task-3.png)