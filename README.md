                                            CCNA Cisco IOS operating system-Labs


In this lab session I'm going to perform the basic configuring of a Cisco device in this case a 2911 router cisco.

I am going to be using packet tracer to perform the configurations.


                                            Load the Startup Configuration
To load the startup configuration you will need a router or switch to operate on.
![Screenshot (69)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(69).png)

                                                Connect to the device
We then click on the router to access the CLI (Command Line Interface).
![Screenshot (70)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(70).png)

![Screenshot (71)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(71).png)

Next press the return(enter) button to get started, you will jump right into user exec mode.

you will know that you are in the User Exec mode with this command line 'Router0>'
![Screenshot (72)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(72).png)

Then enter Privileged Exec mode 'Router0#'
![Screenshot (73)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(73).png)

The Privileged mode allows you access not only to the commands listed above but also access to all the commands available on the switch to display, modify, and change all the features on the switch.

To reboot the device we write this command line:
Router0# reload
proceed with reload? [confirmation] (enter)
-At this point we are going to observe the device going through the reboot(bootup) process in the command line output.
-This is possible because we are using a console connection(virtually) (we could not see this if we connected to an IP Address on the device)
![Screenshot (74)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(74).png)

in the next screenshot you will be prompted to either confirm to start with the initial configurations or not, you enter NO.
--
display message - would you like to enter the initial configuration dialog? [yes/no]?
![Screenshot (75)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(75).png)

here the device has been rebooted.
![Screenshot (76)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(76).png)

                                          Explore user exec mode and cli command help
The moment we hit enter (return) in the cli we officially enter the user exec mode.

To see the available commands in the user exec mode we enter a question mark.

If we enter the 'Show run' commmand in the user exec mode we get this error:
  Router> show run
               ^
  % invalid input detected at '^' marker.

The 'show run' is a valid command but it's run at the privileged exec mode, not at user exec mode, so the command fails.

if you see the 'invalid input' error then check if you are at the correct level for the command you are trying to run.

if you are at the correct level then check for typos.
![Screenshot (77)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(77).png)

                                  Exploring Privileged exec mode (Enable) and context sensitive help
To enter the privileged exec mode we enter enable.
To drop back to user exec mode we enter disable.
Then there are certain command abbreviations which only work when you enter letters whic could only match one unique command.
If we attempt to return to user exec by entering 'di' we get an ambiguous command: di error.
to check to see possible commands which begin with 'di' we add a question mark.
![Screenshot (78)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(78).png)
So the only way to use the disable abbreviation is using 'disa' which will take us back to user exec mode.
we can access detailed information and debug output in privileged exec if we check to see all commands that beegin with 'sh'.
'show' is the only command that begins with 'sh' so we can use that as the abbreviation.
When we enter 'sh ?' to see all available show commands. 
![Screenshot (79)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(79).png)
Notice that we have now included a space before the question mark. This eneters context sensitive help for the 'show' command.
If we want to see more show commands we press the return button to display the commands one at a time. This could be very slow so there is another option.
We can press the space bar to display page by page commands.
![Screenshot (80)](https://raw.githubusercontent.com/AlexChirwa/CCNA-Cisco-IOS-operating-system/refs/heads/main/Screenshots/Screenshot%20(80).png)

