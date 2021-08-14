# Simple Event Logger SmartApp
SmartApp Simple Event Logger version 1.6:

NOTE:
Kevin LaFramboise (krlaframboise) author of this smartapp says:
I don’t have time to review and test your version so I won’t be adding it to the SmartApp.

I’m sure there are others that are interested in the changes you made, but I’d rather not have 2 instances of the SmartApp linked to on this topic so I’d appreciate it if you could PM the code/link to any users that request it.

I put the Kevin smartthings community link:

https://community.smartthings.com/t/release-simple-event-logger/69879/568?u=mariano_colmenarejo



To avoid the loss of device event capture due to frequent delays or stops in the smatthings event history server during the month of July and possible future failures, I have modified the Simple Event Logger app to version 1.6, to set the start time of the next event capture period (startDate variable) at the time of the last event captured + 1 sec.
In this way, if the event history is stopped or delayed, the time of the last event captured will be kept as the startDate value and no events will be lost when the history is restored.

The end time of the capture period (endDate variable) remains to the current time + the time selected as the events capture frequency.

I’ve tested it and it works fine, no live logging errors and no duplicate or missing events on google sheet appears.

*  Changelog:
 *
 *    1.6 (08/01/2021) Modified by Mariano  Colmenarejo
 *      -  Next get events Period calculation changed to avoid the loss of device event capture due to frequent delays or stops in the smatthings event history server in last month
 *      -  getNewEvents(startDate, endDate) peirod is calcualted "From" last event time downloaded + 1 sec (startDate) "To" logFrequency period seletec + now time (endDate)
 *
