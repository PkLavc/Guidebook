# How to Create a Shortcut in Kali Linux to Execute a Command

To create a shortcut in Kali Linux that executes a specific command, you can use the `sh -c` command. This command allows you to run a sequence of commands directly in the terminal.

## Example Shortcut to Execute a Game

Suppose you want to create a shortcut to run the game "Grand Theft Auto," which is located in `/home/pc/Documents/Games/GrandTheftAuto/`.

### Steps to Create the Shortcut:

1. **Open the Terminal:**

   Open the terminal in Kali Linux.

2. **Create the Shortcut Using `sh -c`:**

   Use the following `sh -c` command to create a shortcut that navigates to the game directory and executes the executable file:

   ```bash
   sh -c 'cd "/home/pc/Documents/Games/GrandTheftAuto/" && ./GrandTheftAuto'
