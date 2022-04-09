+++
title = "15 Useful Visual Studio Keyboard Shortcuts I Love"
description = "15 Visual Studio shortcuts which will make everything easier and encreasse your productivity"
author = "Jordy Deweer"
date = 2022-04-08T16:27:43+02:00
tags = [
    "Visual Studio",
    "IDE",
    "Keyboard Shortcuts"
]
+++

Here you find 15 useful Visual Studio keyboard commands that make life much easier in that IDE.


The following list of fifteen keyboard shortcuts for visual studio was randomly put together and afterwards split into categories.

## Debugging
1. F5 – Start or continue debugging
While developing software, you often want to run a debug session. You run your code easily by pressing the F5 Key. Then it will launch in Debug mode.

When you already are in Debug mode and hit a breakpoint, you can continue execution of the code without steppin through it by pressing F5 again.

2. Shift-F5 – Stop debugging
It is as simple as that: pressing this shortcut will kill all debugging processes and stop the execution of your code.

3. CTRL-Shift-F5 – Restart your code
When you are debugging, you might want to restart your debug session. Either with or without Hot Restart/Reload functionality, this shortcut will restart the debugging session.

In both cases it will rebuild the code, but with that difference that when Hot Reload/Hot Restart is available, the code only changed will be recompiled and injected in the existing code.

When Hot Reload is available, you’ll be thrown in the app where you left off.

 

4. F10 – Step over
When debugging after hitting a breakpoint, you’ll pass several elements like variables, properties, fields, objects, methods, etc.

To skip the initialization of something or the execution of a method, you can press F10. It will bring you to the next line of the current code block, without entering the to be executed part.

5. F11 – Step into
This does exactly the opposite. Instead of skipping the execution, it will enter the execution and show what happens.

This only works for self-written code. Microsoft or third-party libraries/code are not supported.

## Refactoring and code suggestions
6. CTRL-. – Quick actions
You surely know about it. The suggestions you get when clicking the light bulb icon? Like adding a using statement.

It is possible to get these suggestions from the keyboard while pressing CTRL-.

7. CTRL-Space – Show IntelliCode suggestions
Code completion like method names is done with IntelliCode in Visual Studio. Sometimes, the pop-up showing its suggestions does not appear automatically, or you might have closed it already and wanting it again.

You can (re)open it by pressing CTRL-Space. Navigate the options with your arrow keys and press the Tab key to accept a suggestion or press Escape to close the pop-up (again).

## Windows
8. CTRL-\, CTRL-E – Open the error list
Focusing the error list is for sighted users not that useful, but for visually impaired programmers, it could make a world’s difference.

Pressing this shortcut brings the focus to the Error List, where the errors can be navigated using the up and down arrows. Close the list using the Escape key.

TIP! When you press enter on a selected error, you are taken to the place where the error is showing.

9. Alt-T, Alt-N, Alt-O – Open the Package Management Console
This shortcut, which navigates through the Visual Studio main menu, opens the NuGet Package Management Console window, where commands can be entered.

The window can be closed using CTRL-F4.

10. Shift…Alt – Focus contextual toolbar
This will bring the focus to the toolbar of the currently active window. For example, when the package management console is opened and this special shortcut is pressed, it will bring you to the combobox to select the working project.

This shortcut is pressed in a special way. You first press the Shift key and keep it pressed for about a second, then you press the Alt key, which you can release immediately after pressing and when the Alt key is clear, you can release the Shift key.

It took me some practicing, but it’s a very useful shortcut to alter certain otherwise not alterable settings.

11. Alt, CTRL-Tab – Open the main toolbar with the play button
It is possible to open the main toolbar which contains the Play button. You can, after focusing it, move around it using the Tab and Shift-Tab keys known for Windows navigation shortcuts.

To focus this toolbar, you open the Main Menu of Visual Studio by pressing and releasing the Alt key. When the File menu option (top level) is selected (not opened), press CTRL-Tab to go to the mentioned toolbar.

## Various keystrokes
12. F12 – Go to definition
This is extremely handy. In many cases, it shows how a class, constructor, method,… is implemented. to use it, place the cursof on the element of which you want to see the definition and simply press F12. You might need to change some outlining before seeing omments or code.

Good to know is that this function also works on various third-party libraries and even built-in functions of .NET. Though, not all…

13. CTRL-M, CTRL-M – Toggle outlining of code block
It is possible to show or hide a code block. To toggle that, press this shortcut.

It is possible to collapse or expand classes, methods, constructors entire properties and getters and setters.

14. CTRL-K, CTRL-M – Show line annotation
This is mainly useful for screen reader users, I recon, as this shows the amount of errors, warnings and other useful information of that particular line of code.

The informqation is given through a simple, fastly-disappearing message.

15. CTRL-Shift-B – Build the solution
It’s a straight forward keystroke. It’ll build all projects in the solution.

I often use it to check whether my code builds without compilation errors. That’s for me, as a user of a screen reader sometimes faster than checking the error list. Though, it depends on the kind of solution and the amount of projects inside it.

## Conclusion
There are many keystrokes to easily use Visual Studio without leaving the keyboard. Of course, there are much more keyboard shortcuts available and they’re even configurable. So, you can create your own keymap!

In this blog post however, I gave fifteen shortcuts I use often, divided in a few categories:

* Debugging
* Code refactoring and completion
* Windows and navigation
* Others

Got any suggestions or questions? Feel free to leave them in the comments below.

Also, share this article with friends and colleagues. They might be happy with these keyboard hacks too.