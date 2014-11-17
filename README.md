RCE
===

Remote Code Execution for InterSystems Caché.<br>
Can execute code on:<br>
Windows -> Windows, Linux<br>
Linux -> Linux

Installation
===
1. Import and compile all classes (any namespace).
2. (Non-required) Set following global values:<br>
set ^settings("exec") = {path to psexec (only for windows sysytems, to manage other windows systems) - or add to PATH and leave empty}

The following settings are for test server (set to use do ##class(RCE.Tests).TestConnection() method):<br>
set ^settings("test description") = {Server description}<br>
set ^settings("test ip")= {Server ip (host)}<br>
set ^settings("test username") = {OS username}<br>
set ^settings("test password") = {OS password{<br>
set ^settings("test osbit") =  {OS bit: x64 or x86}<br>
set ^settings("test osname") = {OS "windows" or "linux"}<br>
set ^settings("test cache name") = {Caché instance name}<br>
set ^settings("test cache version") = {Caché version}<br>
set ^settings("test cache security") = {Security settings, may be "Minimal","Normal","Locked Down"}<br>
set ^settings("test cache user") = {Caché username if required}<br>
set ^settings("test cache password") = {Caché user password, if required}<br>
set ^settings("test cache dir") = {Caché installation directory}<br>

Usage
===
See RCE.Tests class for usage example.
