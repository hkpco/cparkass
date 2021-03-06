< CPARKASS Manual >
===================

0. The origin of tool name
--------------------------

Chanam Park is my name and this tool has been developed to assessment of software security.

So, Chanam PARK's ASSessment -> CPARKASS

This is just in case that you would think the word "ASS" as a strange means. You know. ;-)


1. Introduction
---------------

Cparkass is a convenient tool for the security assessment or fuzzing which is developed by python.

The concept is very simple.

Suppose someone wants to verify the software's vulnerability which is processing some file formats.

In that case, you can use this tool.

Cparkass is using crafted files as a database that was succeeded either to occur crash or to exploit particular software before.

For example, if you want to find or to check the vulnerability in specific movie player,

cparkass can perform the security assessment of the software with own database which is composed of crafted files like an avi, wmv, pdf, etc.

To sum up, cparkass conducts such a high probability fuzz testing by the pattern-based database.

FYI, this is only for Windows platform yet.


2. Help
-------

You can see the help message as follows.
+ ./cparkass -h
+ ./cparkass --help


2. Update
---------

####Update all patterns
+ ./cparkass -u

####Update specific pattern
+ ./cparkass -u [pattern]<br>
`Ex> ./cparkass -u pdf`

####Update more than one pattern
+ ./cparkass -u [pattern/pattern/pattern/...]<br>
`Ex> ./cparkass -u avi/wmv`


3. Assessment software
----------------------

####Assessment with all patterns
+ ./cparkass -t [target path]<br>
`Ex> ./cparkass -t C:\music_player\listen.exe`

####Assessment with specific pattern
+ ./cparkass -t [target path] -p [pattern]<br>
`Ex> ./cparkass -t C:\doc_editor\mx_office.exe -p doc`

####Assessment with more than one pattern
+ ./cparkass -t [target path] -p [pattern]<br>
`Ex> ./cparkass -t C:\doc_editor\mx_office.exe -p doc/ppt/xls`


4. Other options
----------------

####-l (--lapse) option
+ To Set the waiting time in seconds before to exit the target program(default value is 5).
<br>
*- All of the computers are not having a same time to run specific software. That's why this option is provided.*
`Ex> ./cparkass -t C:\music_player\listen.exe -l 3`

####-v (--verbose) option
+ To get detailed information.<br>
`Ex> ./cparkass -t C:\music_player\listen.exe -v`

