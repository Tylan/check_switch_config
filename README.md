# check_switch_config
Perl script to backup as well as check switch configs for changes and notify of any


In order for the script to do an OS detection nmap requires root privileges to run.  Using visudo put these in with the already defined section at the bottom.  This gives the script root permissions so that it may do the OS detection.  You may need to modify slightly for Icinga2 installations.

NAGIOSXI ALL = NOPASSWD:/usr/local/nagios/libexec/check_switch_config<br>
NAGIOSXIWEB ALL = NOPASSWD:/usr/local/nagios/libexec/check_switch_config<br>


FAQ:

Q: I receive this when I run the script:<br>
   Received disconnect message: SSH file transfer is not enabled on the switch.

A: On Aruba / HPE switches:<br>
   ip ssh filetransfer

