After adding the macro and updsating the firmware, the following lines will need to be added to your config files.  The location will be based on how you have your printer set up.  Generally, this will be where you have your homing or homing override set up and where you have your BED_MESH_CALIBRATE set up.

For Bed Mesh, add this before and after your gcode macro

SET_GCODE_VARIABLE MACRO=_KNOMI_STATUS VARIABLE=homing VALUE=True
SET_GCODE_VARIABLE MACRO=_KNOMI_STATUS VARIABLE=homing VALUE=False

For Homing, add this before aned after your gcone macro

SET_GCODE_VARIABLE MACRO=_KNOMI_STATUS VARIABLE=homing VALUE=True
SET_GCODE_VARIABLE MACRO=_KNOMI_STATUS VARIABLE=homing VALUE=False

IMPORTANT: These will not work if the firmware is not updated to use the _KNOMI_STATUS Macro to trigger Knomi to display the appropriate information.