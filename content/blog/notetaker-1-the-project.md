+++
title = "Notetaker 1: The Project"
description = ""
author = "Jordy Deweer"
date = 2022-04-17T22:03:34+02:00
tags = ["projects","Notetaker"]
+++

Now, it is time for a first project. As you may know, I'm visually impaired and sometimes, it is hard to take notes. I want to build a simple note taking application and I will share the process in my blog with you.

This post will not contain any code, but it will explain the purpose of the application, as well as how I will implement everything and how I see certain parts of it.

The code of the note taking application can be found in [this GitHub repository](https://github.com/dewsystems-dev/ds-notetaker).

## The app: an overview.

There are various notebooks possible: file-based databases using LiteDB.
When opening a .dsnb (DewSystems Notebook) file, a list of various folders is shown, wherein you find all notes.
By clicking a note's title, it's possible to edit or delete it.

Everywhere in the app, it'll be possible to add a new note. When the folder list is shown, it'll be possible to add a new folder.

## Notes: their look

Notes will be saved in the Markdown format. They can be edited in Markdown as well.

They at first will only be shown in Markdown, but in a future release, it will be possible to show data in WYSIWYG mode also.

The WYSIWYG mode will at first only support bold, italic and underlined fonts, headings, lists, links and tables. However, in the future, it should be possible to show images too. These images will then be saved to the notebook as well.

In one of the future releases, it should be possible to record and/or save audio and video to the notebooks too, so audio fragments can make notes easier to understand or quicker to make. When and how this will be implemented is not known by now.

## Data storage

All data, including the notes, will be stored in one document-oriented database management system: LiteDB. It is an embedded NoSQL database for .NET, that makes it possible to store non-relational data easily.

In a future release, it will be possible to encrypt the entire data with just one password, which will then decrypt a file which contains the encryption key for the notebooks. It will be important to set the file stream and so its contents in memory to null after using a key, forcing to re-enter the password every time needed.

## The technology stack

Of course the app will be written in .NET 6. Moreover, .NET MAUI will be used. At the time of writing, .NET MAUI is not released as a general availability release yet, but it's functional enough to write a decend app in.

Using .NET MAUI, the application will run on Windows, MacOS, Android and iOS easily. Perhaps in the future, depending on Microsoft's roadmap, even on Linux flavors. That makes the app usable for a wide range of users.

For data storing, I'll use LiteDB, as I mentioned before. That .NET native embedded NoSQL database is very similar to SQLite, but then for document-oriented databases. It can also store attachments in database, which makes it possible to have one (large) file. It might be necessary to compress the file upon saving, to  spare file storage and to increase loading times.

<hr />

Want to contribute? Feel free to do so in the repository mentioned above.

Otherwise, share this blog or leave your comments below.