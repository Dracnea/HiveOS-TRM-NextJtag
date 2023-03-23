Information

Use the HiveOS hive/etc/crontab.root

Add lines
@startup sleep XX && /NextJtag/bin/nextjtag -a -B --disable-voltage-limit --set-voltage 0.XXX
@reboot sleep XX && /NextJtag/bin/nextjtag -a -B --disable-voltage-limit --set-voltage 0.XXX

Ensure that Hiveroot root directory has NextJtag folder added
Within this folder at the bin/nextjtag level ensure that you have your license file

Within HiveOS Website Access for Miner, under the Settings tab ensure that Miner delay is set to (15s + 15s x FPGA Units Count)
This means start with 15s and for each fpga added include an additional 15 seconds to ensure that NextJtag has time to set Voltages for each device.
