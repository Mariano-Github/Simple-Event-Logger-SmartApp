# Privado
Temporalmente privado

*  Changelog:
 *
 *    1.6 (08/01/2021) Modified by Mariano  Colmenarejo
 *      -  Next get events Period calculation changed to avoid the loss of device event capture due to frequent delays or stops in the smatthings event history server in last month
 *      -  getNewEvents(startDate, endDate) peirod is calcualted "From" last event time downloaded + 1 sec (startDate) "To" logFrequency period seletec + now time (endDate)
 *
