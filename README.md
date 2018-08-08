# check_sap_scc4.py
Nagios plugin for checking SAP SCC4 settings

![](/images/check_sap_scc42.png)

![](/images/check_sap_scc4.png)


Usage:./check_sap_scc4.py \<SID\> \<client\> \<settings eg: P23XX\> \<warning|critical\>

Example:

root@:~/github# /usr/lib/nagios/plugins/check_sap_scc4.py SBX 200 "P23XX" warning

WARNING: SCC4 settings in System are NOT as expected C12   != P23XX - 200;SCustomizing;C;1;2;;;SAP*;20171201|num=0


                                                                      
### Prerequisite:
https://github.com/piersharding/python-sapnwrfc

### Wiki:
Installation of sapnwrfc for python on Linux and Unix
https://wiki.scn.sap.com/wiki/display/EmTech/Installation+of+sapnwrfc+for+python+on+Linux+and+Unix






To prepare a script, you'll need a 'yml' file similar to the 'sap.yml' file included with the sapnwrfc download. The file looks 

like this:
#### Example of SID.yml file

ashost: gecko.local.net

sysnr: "01"

client: "001"

user: developer

passwd: developer

lang: EN

trace: 3

loglevel: warn
