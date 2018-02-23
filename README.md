# MPK261-Reason-Codecs
Reason Codecs for the MPK261, specifically for the endless encoders to output a delta value

-- Akai MPK261 Codec
-- Modified from Bob Snider version for the MPK61
-- http://audio.seekone.com/content/improved-akai-mpk-reason-codec
-- V 1.0.0
--
-- Tested and working on Windows 10 with Reason 10 V10.0.2d1 (build 8,956)

This codec file for the MPK261 has been created in order to be able to control reason 10. It was specifically designed to let reason understand the relative value change output from the MPK261. This is useful because it will prevent the controlled parameter from jumping from one value to the next but instead have a smooth change with acceleration.

The file also has the loop button working :) you just need to map it yourself and follow the last step of the modifications.

Before using the codec some change need to be done on the MPK itself, starting from the reason preset 07 on the MPK261:
- Change the "Type" of the knobs from MIDI CC to INC/DEC1
- Change the MSB to 20 for ALL knobs
- Change the Lsb to the knob number (e.g. 01 for knob01, 02 for knob02, etc...)
- Change the transport button "type" to MIDI CC (so the loop button and all other transport buttons work)

Once these changes have been made you can replace the lua file (AkaiMPK261_406.lua) in C:\ProgramData\Propellerhead Software\Remote\Codecs\Lua Codecs\Akai (for windows) 

I hope this help anyone that have trouble with reason's codecs !

Florent
