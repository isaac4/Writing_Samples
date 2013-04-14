#Bash Shell Configuration File

The Bash shell is the interactive command line interpreter most commonly used on Linux systems. It's useful to begin a command line session by executing a series of commands that initialize and customize the user's environment. Most initialization commands set environment variables to configuration data used by the shell and by other software.  Environment variables tell software where to find crucial files, specify user options, and provide similar useful facts.

Another use of initialization files is to define customized commands called aliases.

Most shell configuration files are stored in the user's home directory and have names beginning the "." character. The use of "dot" files is a Unix/Linux convention for files that can be omitted from normal directory listings.

The use of configuration files is affected by the bash command line option `-l`. This option indicates a login shell created by the user logging into the system. The process tree that begins with the login shell might contain additional shell instances created when the user runs a script, opens a terminal window, or otherwise does something that requires a new shell instance. For these shells, the `-l` command is omitted, allowing the shell to skip initialization commands that should not be repeated.

These are the configuration files used in typical bash setups. Except when a fully qualified path name is given, the file is stored in the user's home directory.

<dl>
    <dt><tt>.bash_profile</tt></dt>
    <dd>Invoked automatically when a login shell is created. Contains commands that should be run when the user logs in. </dd>
    <dt><tt>.bashrc</tt></dt>
    <dd>Invoked automatically when a non-login shell process is created. User accounts are normally provisioned so that the <tt>.bash_profile</tt> invokes the <tt>.bashrc</tt> file. Thus commands that should be executed by both login and non-login shells belong in <tt>.bashrc</tt>.
    <dt><tt>/etc/bashrc</tt></dd>
    <dd>Contains commands that should be executed by all users on a system. This file is not invoked automatically by the shell. Instead, user accounts are normally provisioned so that <tt>.bashrc</tt> invokes <tt>/etc/bashrc</tt>.
    <dt><tt>.bash_logout</tt></dd>
    <dd>Invoked automatically just before the exit of a login shell. Since the environment of a terminated shell is lost, this file has limited function. Typically it contains a single command that clears the screen.</dd>
</dl>
