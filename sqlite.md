---
layout: site
title: SQLite Installation Tutorial
---

[SQLite](https://www.sqlite.org/index.html) is a small, fast, self-contained, and reliable SQL database engine. It's commonly used in small applications as well as mobile applications due to how easy it is to use and how self-contained it is. In this course, we will be using SQLite for some exercises / assignments

---

### Windows Installation Instructions

SQLite is kind of a pain to get working on Windows (as is most development technologies). I would personally highly recommend you use a more robust UNIX-based development environment such as Linux or Mac OS as it will save you a lot of headaches in the long run.

Firstly, go to the [download page](https://www.sqlite.org/download.html) on the SQLite website

For the command-line shell program, download the file shown below or cilck [here](https://www.sqlite.org/2018/sqlite-tools-win32-x86-3260000.zip)
- Do not download any of the other options. They do not have the actual program (are only DLL files)

<img src="http://www.sqlitetutorial.net/wp-content/uploads/2018/04/SQLite3-Help-command.png">

Save the download somewhere convenient and unzip the file and run the file `sqlite3.exe` to run SQLite

Running SQLite through the physical file is rather cumbersome and you may want to add it as a command line program. To do so:
1. Create a new folder in your `C:\` drive (e.g. `C:\sqlite`)
2. Extract the contents of the zip file you downloaded into `C:\sqlite`
    - If you've done this correctly, you should see that `sqlite3.exe` is in `C:sqlite`

Generally, Windows will not recognize that you've added the file and you will be required to add SQLite as a PATH environment varaible
1. Go to `Control Panel > System > Advanced System Settings > Environment Variables`
2. Dobule click the `Path` item from `User variables`
3. Click on `New` on the right hand side
4. Add the path `C:\sqlite`
5. Save it

At this point, you should be able to run SQLite from Command Prompt using the command `sqlite3`. To run a database file, run the command `sqlite3 <database>` where `<database>` is the name of your database file

---

### Linux / Mac Installation Instructions

SQLite comes installed by default on Mac. If for some reason you don't have it installed, you can install it in one of two ways:

If you have homebrew installed, run the folloiwng command:
```
brew install sqlite3
```

If you do not have homebrew, you can install it from source:
1. Download `sqlite-autoconf-*.tar.gz` under the **Source Code** section of the SQLite website under the **Download** section
2. In the Terminal app, run the following commands
```
cd ~/Downloads      # cd to wherever you saved the tar file
tar xvfz sqlite-autoconf-3240000.tar.gz
cd sqlite-autoconf-3240000
./configure --prefix=/usr/local
make
make install
```

SQLite also comes installed by default on Linux. It is also available on all the lab computers. If you're running a Linux machine and you don't have SQLite installed for some reason, you can install it using the same steps as above

---

### SQLite Browser

[SQLite Browser](https://sqlitebrowser.org/) is a graphical user interface to create, design, and edit database files that are compatible with SQLite. It is **NOT** a visual shell for the command-line tool and is **NOT** a replacement for the command-line tool. The browser makes it easier to visualize operations on large tables however it should not be used as an alternative to the actual program. Becoming overly reliant on using the browser is a crutch and will make you worse at writing and coming up with queries yourself.

The installation for SQLite browser is relatively straightforward from the website. You do not need the actual SQLite program to run the browser