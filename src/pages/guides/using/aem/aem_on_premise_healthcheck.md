# Adobe I/O Events Sling Health Checks

## Bundle configuration health heck 

In order to verify your configurations, you can use the AEM Web Console Sling Health Check
and execute the health check tagged with `conf-events`.

   ![Health check for eventproxy,conf](../../img/events_aem_21.png "Health check for conf-events")


## IMS health check 

In order to check that the AEM instance is able to exchange JWT tokens 
with Adobe I/O Identity Management System (IMS), you may execute a sling health check using the `ims-events` tag.

This verifies that your IMS related configurations are correct and working.

   ![Health check for eventproxy,ims](../../img/events_aem_22.png "Health check for ims-events")


## IO Events registration health check 

In order to check that the AEM instance registered itself as an Adobe I/O Events Provider,
 execute a sling health check using the `csm-events` tag.

   ![Health check for eventproxy,csm](../../img/events_aem_23.png "Health check for csm-events")


## Checks events emitting

In order to check that the AEM instance is able to emit events:
* trigger an event 
   * for instance an asset update event by editing an asset
   * or POST a (custom/ping) osgi events through the `system/console/events` UI.
* and watch 
  * your AEM logs 
  * your webhook registration endpoint


If for some reason, your webhook is failing, note that the Adobe Developer Console holds a `Debug Tracing` feature:
It allows you to watch all the events payloads emitted by Adobe I/O towards your webhook and the associated webhook response.
