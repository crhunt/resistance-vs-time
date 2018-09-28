# resistance-vs-time

RvsTime_Tektronix_Vbias_crh.vi

This LabView software was developed for recording resistivity vs time using a Tektronix oscilloscope, Keithley sourcemeter, and LakeShore temperature controller.

The program records the oscilloscope output and writes it to a file, while controlling temperature and applied bias voltage.

The temperature and heater settings, including ramping, can be controlled via the LabView interface.

A voltage bias can be applied via the Keithley sourcemeter. A ramping mode can be set to record at a series of bias values.

Note that communication with either device can be toggled on and off. (Useful for debugging communication issues.)

Hardware Requirements
---------------------

Temperature Control: LakeShore 331

SourceMeter: Keithley 26XX series (tested with 2635A)

Oscilloscope: Tektronix 7xxx series

Labview vi Requirements
-----------------------

Included sub-vi's:
- Find-Average-CRH.vi (Calculate running average)
- create-time-array.vi (Create array)
- Save-OsciVsTime.vi (Saving data)

Source: Included in this repository

Communicating with LakeShore 331 temperature controller:
- lsci331u.llb
- lsci331.llb
- LS331-temp-cntrlvi.vi
- Lake Shore Cryotronics 331.lvlib

Source: (Labview 8.2) http://sine.ni.com/apps/utf8/niid_web_display.download_page?p_id_guid=7094CC81B2146DD9E04400144FB7D21D

Communicating with Keithley 26XX sourcemeter:
- KE26XX.lvlib
- KE26XX-SM-close.vi
- KE26xx-SM-2W-init.vi

Source: https://www.tek.com/source-measure-units/2635-software/keithley-series-2600-2600a-2600b-native-labview-2009-instrument-d

Communicating with Tektronix 7xxx oscilloscope:
- Tek7xxx-ReadScope.vi
- Tektronix 7000 Series.lvlib

Source: (Labview 8.2) http://sine.ni.com/apps/utf8/niid_web_display.download_page?p_id_guid=6566BC3787B433D2E0440003BA7CCD71
