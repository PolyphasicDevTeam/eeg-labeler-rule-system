# eeg-labeler-rule-system

Post-processes EEG graphs outputted from Yinsei's EEG labeler using the following general rules:

* Shift Light sleep within REM or SWS to closest edge
* REM <= 15m within SWS treated as SWS
* SWS <= 15m within REM treated as REM
* REM at start of recording is actually NREM1
* SWS at start of recording is actually Awake
* Wakes <= 15m within REM or SWS are are treated as REM or SWS
* Discard anything with an interrupted wake time of 20 minutes or more

Output is a `.csv` in the same format as the EEG labeling project ran on the polyphasic Discord

Usage:

* Windows: Drag Yinsei's output file to `rules.cmd`
* or `python3 rules.py <file>`
