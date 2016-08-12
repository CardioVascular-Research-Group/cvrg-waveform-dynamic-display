# cvrg-waveform-dynamic-display
Sandbox for Dynamic display of Waveform data

This branch contains code customized for use with the "new" openTSDB instance rather than the "old" Waveform instance. A non-exhaustive list of changed files is below. 

1. TSDBBacking.java
  1. line 46, changed ip address
  2. line 61-63, added or condition to put the 'tag' on vitals metric as well. Also had to change static 'subject id' value to conform to new system
  3. line 121-125, had to disable adugain calculation and parselong method which makes it possible. New TSD is returning decimal values which broke this. Will need repair before ecgs can be implemented again in same way.
2. AutofillJavascript.js
  1. created new 'leadDefaults' and 'elementArray' utilizing metrics I recorded as available on the new test subject
3. /waveform/index.jsp
  1. just updated default query values in static fields
