# Introduction

!!! abstract "Introduction to Power Shell 7"

You have already learned how to use the old command prompt (CLI) in Windows, and you should appreciate that it is a bit archaic and unintuitive. In an OS which has been in use for over 30 years, Microsoft must maintain consistency with the bad and uninformed decisions of a generation ago.

Not just that; the DOS/Windows command was originally designed to be simple for the average non-technical user to operate a computer. In the 1970s and 80s, for the first time is history, people who were not computer scientists were working directly with computers.

A CLI has no built-in menus, no way to provide hints and assistance to users as to what commands exist and how to use them. Microsoft knew they needed something more powerful and flexible, to give the sort of functionality Linux administrators were used to. 

In the post MS-DOS era, all the development effort of Microsoft went into making an intuitive graphical user interface (GUI), not into enhancing the command prompt. In Windows, you interface with the system through the Application Programmers Interface (API), which was intended for calling from C and C++, not from a command line. Windows is tough to program even in C! Yet the CLI is how most administrators want to configure things; it is repeatable, predictable, and economical. Another problem is that Windows, most modern operating system, and programming languages, are object oriented. CLIs do not manipulate objects, they manipulate text files.

Around 2000, Microsoft ran an internal study to see what it most needed to do to improve its server products. Management tools, in particular the CLI, was one of the priorities identified and the issues mentioned above had to be considered. The obvious and easy thing to do would be to use existing shell commands and an existing language like the Unix Bash shell. However, none of these shells were object based. Every platform had to deal with these issues, and this led to the Distributed Management Task Force [1] being set up and the establishment of a Common Information Model (CIM) for management objects. Microsoft implemented this as Windows Management Instrumentation (WMI )and as you get into PowerShell, you will use this extensively.

Microsoft had already moved their entire platform to .NET, and it made sense to base the new language around the same concepts. The .NET framework is self-describing; that is the objects have a definition of their structure within them. It also meant the new language already had access to the entire set of libraries within .NET. 

In more recent years, PowerShell has become cross-platform, running on Windows, Linux and MacOS. 

The public cloud platform Azure also uses PowerShell.