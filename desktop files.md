 How to create a desktop entry in linux?
#linux
#desktop
#application

If you use Linux, you might often find yourself using the terminal to run programs and scripts for your daily tasks. But it can be a bit of a hassle. Luckily, there's a alternative – creating something called a "Desktop Entry." A desktop entry lets you start programs from your start menu with just a few clicks. All you have to do is follow these simple steps, and you're good to go:

To start with creating Desktop Entry for a program , you have to mess up with terminal for a while.

    All the desktop entries have .desktop as extension.

Create a new .desktop file

    Open your terminal or press Ctrl+Alt+T
    Create a new desktop file using a text editor. You can use nano or vim or any text editor you like.
    The syntax of the command should be something like this :

vim application_name.desktop

Define Entry Properties

    [Desktop Entry] - Every desktop entry starts with this keyword.
    Name : Name of the application.
    Exec : Path of the executable file.
    Type : Set it to application
    Icon : Path of the application logo.

Add optional information

    Comment : A brief description of the application.
    Categories : Categories that describe the application(e.g., Development, Office)
    Terminal : Set it to false if the application doesn't require terminal.
    StartupNotify : Set it to true to show a notification when the application starts.

Set permissions

    Make the .desktop file executable using the chmod command:

chmod +x application_name.desktop

Move the file

    For system-wide access : Move the file from current directory to /usr/share/applications
    For user-specific access : Move the file from current directy to ~/.local/share/applications

Refresh Desktop Environment

    If needed, refresh the desktop environment. Typically the command to refresh desktop is :

sudo update-desktop-database

Finally, your application_name.desktop would look like this:
Desktop Entry Properties
And there you have it! By following these steps, you'll have your very own application shortcut in the start menu using the magic of .desktop files.