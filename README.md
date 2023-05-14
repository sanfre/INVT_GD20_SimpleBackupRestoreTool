# INVT_GD20_SimpleBackupRestoreTool
Simple Java tool for backing up and restoring parameters from INVT GD20 VFDs.

WARNING THIS IS A BETA TOOL, use at your own risk.

This tool is intended for technicians who need to maintain such VFDs. The tool is able to backup and restore parameters through the RS485 interface. It is a command-line interface (CLI) tool that receives parameters from the command line in order to perform a specified action.

For example, to back up an inverter, the user needs to supply the following parameters:
PARAM1: BKP
PARAM2: INVERTER ADDRESS
PARAM3: PATH to the FOLDER WHERE THE FILES REFERRED TO IN PARAM4 and PARAM5 ARE LOCATED.
PARAM4: NAME OF THE CSV FILE WHICH CONTAINS THE PARAMETERS THAT NEED TO BE BACKED UP (See example file attached)
PARAM5: NAME OF THE CSV BACKUP FILE GENERATED
PARAM6: NAME OF THE SERIAL PORT CONFIG FILE (See example file attached)

For instance, to back up the parameters from the inverter with an RS485 address of 1, the user would input the following command:
BKP 1 C:\temp ParamsToBackup.csv bkp_result.csv conf_serial.txt

Now to restore the parameters back to the inverter, the user needs to supply the following parameters:
PARAM1: RES
PARAM2: INVERTER ADDRESS
PARAM3: PATH to the FOLDER WHERE THE FILES REFERRED TO IN PARAM4 and PARAM5 ARE LOCATED.
PARAM4: NAME OF THE CSV FILE WHICH CONTAINS THE PARAMETERS THAT NEED TO BE BACKED UP (See example file attached)
PARAM5: NAME OF THE SERIAL PORT CONFIG FILE (See example file attached)

For instance, to restore the parameters from the inverter with an RS485 address of 1, the user would input the following command:
BKP 1 C:\temp bkp_result.csv conf_serial.txt
