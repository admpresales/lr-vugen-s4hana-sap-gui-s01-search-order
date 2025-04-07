Updated: 04.2025  
Script created by Salvador Camacho

This SAP script requires SoftEther VPN Client Manager to connect to DEMONET

Go to Runtime Settings > SAPGUI > General > Performance  if you want to disable SAP Client during replay

This script was created with best practices, so it is more resilient, such as:
* Transaction naming
* No third party
* One validation per transaction
* Think times at the end of each transaction to better simulate user behavior
* SAP credentials parametrized

This SAP script logs in, enters Tcode /nva03 to search for an order, searches an order, goes to it, then logs off

Runtime Settings were set to log only on errors and generate snapshot on errors, think times 75% to 150%

This script has 4 transactions:  
S4HANA-SAP GUI-S01-01 Log In  
S4HANA-SAP GUI-S01-02 Enter Tcode  
S4HANA-SAP GUI-S01-03 Search Order  
S4HANA-SAP GUI-S01-04 Log Off