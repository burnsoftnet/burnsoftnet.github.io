[<--Home](README.md)
# Using Autorun for your CD or USB application Install

The autorun.inf file is the key to getting your USB drive or CD-ROM drive to perform certain actions automatically and customize it’s look in My Computer. The purpose of this article is to shed some light on how this can be done.

The autorun.inf file is a simple text file that can be opened up in any text editor (e.g. notepad). It always starts with a section header of:

`‌[autorun]`

If you wanted to set the default icon, all you have to do is add the following line.

`‌ICON=cd.ico`

Just change the cd.ico with the name of the icon that you wish to use.

If you wanted to set a default label, then add the following line:

`LABEL=My_Gun_Collection`

**This is the line that you need to run the application on the CD-ROM or USB drive:**

`OPEN=final.exe`

With Windows XP and Vista, when you put in a USB stick, it will give you a list of options on what you wish to do with the data on the drive. you can create your own option as the default by adding the following lines:

`action=Run My Gun Collection Setup`

Usually, if you went to My Computer and clicked on your USB Drive, it will open it up in explorer, well if you wanted it to run the program instead then just add the following lines:

`shell\final\command=final.exe`

`Shell=final`

This is something that we do with our application the we distribute via CD-ROM or USB, the ending file that is copied looks like this:

`[autorun]`
`ICON=cd.ico`
`LABEL=My_Gun_Collection`
`OPEN=final.exe`
`action=Run My Gun Collection Setup`
`shell\final\command=final.exe`
`Shell=final`

The only thing that we have to change is the Label and action to the name of the application that is is for.
