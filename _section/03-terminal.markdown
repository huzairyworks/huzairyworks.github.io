---
title:  "Terminal"
date: 2015-04-25
hashlink: terminal
---

Terminal commands for UNIX platform.

### Encrypt / decrypt single file using OpenSSL

{% highlight c %}
$ openssl aes-256-cbc -salt -in <file_name> -out <file_name>.aes # Encrypt
$ openssl aes-256-cbc -d -salt -in <file_name>.aes -out <file_name> # Decrypt
{% endhighlight %}

### Tar and encrypt / decrypt a whole directory

{% highlight c %}
$ tar -cf - <directory_name> | openssl aes-256-cbc -salt -out <directory_name>.tar.aes # Encrypt
$ openssl aes-256-cbc -d -salt -in <directory_name>.tar.aes | tar -x -f - # Decrypt
{% endhighlight %}

### Tar zip and encrypt / decrypt a whole directory

{% highlight c %}
$ tar -zcf - <directory_name> | openssl aes-256-cbc -salt -out <directory_name>.tar.gz.aes # Encrypt
$ openssl aes-256-cbc -d -salt -in <directory_name>.tar.gz.aes | tar -xz -f - # Decrypt
{% endhighlight %}

### Vi Editor commands

{% highlight c %}
# The Basics
# Press [ESC] button to access command mode.

# Insert
$ a # Append new text after the cursor
$ i # Insert new text before the cursor
$ o # Insert a new line below the line you're currently on and start entering text
$ O # Insert a new line above the line you're currently on and start entering text

# Quit
$ :w new_file_name # Save the file to new_file_name
$ :wq or :x # Save and quit
$ :q! # Quit without saving

# Search and Move
$ /string # Search forward for string
$ ?string # Search back for string
$ n # Search for next instance of string
$ N # Search for previous instance of string
$ { # Move a paragraph back
$ } # Move a paragraph forward
$ 1G # Move to the first line of the file
$ nG # Move to the n th line of the file
$ G # Move to the last line of the file
$ :%s/OLD/NEW/g # Search and replace every occurrence

# Delete text
$ dd # Delete current line
$ D # Delete to the end of the line
$ dw # Delete word
$ x # Delete character

# Editing
$ yy # Copy the line the cursor is on
$ p # Paste the copied line after the line the cursor is currently on
$ u # Undo last
$ U # Undo all changes to current line
{% endhighlight %}

### Check file hashes with OpenSSL

{% highlight c %}
$ openssl md5 file.tar.gz # Generate an md5 checksum from file
$ openssl sha1 file.tar.gz # Generate an sha1 checksum from file
$ openssl rmd160 file.tar.gz # Generate a RIPEMD-160 checksum from file
{% endhighlight %}

### Miscellaneous commands

{% highlight c %}
$ which command # Show full path name of command
$ time command # See how long a command takes to execute
$ time cat # Use time as stopwatch. Ctrl-c to stop
$ set | grep $USER # List the current environment
$ cal -3 # Display a three month calendar
$ date 10022155 # Set date and time
$ whatis grep # Display a short info on the command or word
$ whereis java # Search path and standard directories for word
$ setenv varname value # Set env. variable varname to value (csh/tcsh)
$ export varname="value" # set env. variable varname to value (sh/ksh/bash)
$ pwd # Print working directory
$ mkdir -p /path/to/dir # no error if existing, make parent dirs as needed
$ rmdir /path/to/dir # Remove directory
$ rm -rf /path/to/dir # Remove directory and its content (force)
$ cp -la /dir1 /dir2 # Archive and hard link files instead of copy
$ cp -lpR /dir1 /dir2 # Same for FreeBSD
$ cp unixtoolbox.xhtml{,.bak} # Short way to copy the file with a new extension
$ mv /dir1 /dir2 # Rename a directory
$ ls -1 # list one file per line
$ history | tail -50 # Display the last 50 used commands
$ alias pi="ssh 192.168.1.5 -l pi" # Use alias to quickly execute frequent task/command
$ sudo -i # To run as root
{% endhighlight %}

### Terminal resources:

<ul>
	<li><a href="http://www.nparikh.org/notes/TerminalBasics.pdf">Terminal Basics PDF by Neal Parikh</a></li>
	<li><a href="http://cb.vu/unixtoolbox.xhtml">UNIX Toolbox by Colin Barschel</a></li>
	<li><a href="http://cli.learncodethehardway.org/book/">The Command Line Crash Course by Zed. A. Shaw</a></li>
	<li><a href="https://github.com/alebcay/awesome-shell">A curated list of awesome command-line frameworks, toolkits, guides and gizmos.</a></li>
</ul>
