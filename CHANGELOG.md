Parallec Change Log
==========

## Version 0.9.1

_2015-11-03_

* Chnage: maven pom: maven-compiler-plugin version to 1.7.



## Version 0.9.0

_2015-11-01_

* Add: Late initialize CapacityAwareTaskScheduler only when it is used. Added shutdown for the scheduler.
* Test: Update some tests on variable replacements.
* Doc: Update javadoc.

## Version 0.8.12-beta

_2015-10-29_

* Javadoc: refine javadoc. Fixed errors in javadoc.  
* Coverage: add code coverage.
* Maven: setup with maven central deployment. Added codecov and travis CI.


## Version 0.8.11-beta 
## Version 0.8.10 

_2015-10-27_

* Change: refactor and removed command director. Renamed command manager to execution manager. 
* Change: remove duplicated functions of prepareHttp* in builder and client classes.   Refactor internal type of http method.
* Add: ParallelTask add getAggregatedResultHumanStr() to display human readable results.
* Change: enforce safeguard of concurrency limit for SSH as 400.

## Version 0.8.9

_2015-10-25_

* Remove: Remove apache http client

## Version 0.8.8

_2015-10-24_


* Change: Refactor validation for httpMeta and move the async http client to httpMeta. Refactor Various package structures. Passed test with 93.6 coverage.


## Version 0.8.7

_2015-10-20_

* Add: Option to execute response handler in either Manager thread (after aggregation) or operation worker thread (before aggregation; in parallel). 
* Change: Refactor poller information into httpMeta for better composition.


## Version 0.8.6

_2015-10-15_

* Add: Added Parallel Ping feature. able to due 2 types. added retries and unit tests
* Add  Added Parallel TCP feature based on netty. able to handle idle connections. Added the unit testing with sample TCP server. 
* Change: added the log interval to give options to trim logs


## Version 0.8.5

_2015-10-15_

* Fix: change from single thread executor to pool executor in SSH/Ping worker to significantly reduce the thread size.
* Add: Add scalable PING with InetAddress and process based. 
* Fix: replace all tab by spaces for consistency.
* Fix: Fix when response received in operation worker, timeoutFuture is not canceled. 
* Change: remove unnecessary response from manager. Remove redundant sent 


## Version 0.8.4

_2015-10-13_

* Add: Change cancel ont target hosts from single to a list.
* Fix: Fix 3 sonar critical ones.


## Version 0.8.3

_2015-10-12_

* Add: several unit tests case for corner cases.
* Add: parallel task api to cancel task on single target. 

## Version 0.8.2

_2015-10-11b_

* Add: status code 
* Change: when not save response: will still save metadata about the task. 
* Add: map of completeness of each. add function to cancel each worker.
* Add: parallel task submit/execution start/end time and duration in seconds:view in logs.
* Fix: parallel task cancel in command manager now wait for all op workers to come back. Fix issues when the op sender is not set. Cleaned up 3 duplicated data in response. 
* Add: response map now properly show canceled single host response status; and the PTask status. 

## Version 0.8.1

_2015-10-11a_

 * Add: Add status aggregation
 * Add: Add the monitoring on memory/java thread APIs
 * Add: Sample 10K, 2K websites to hit tests
 * Fix: Fixed the auto save log not working issue
 * Fix: Removed the structure of SSH Meta when it is not SSH.
 * Enhance: Refined the logic to get error message summary.
 * Add: Add Aggregation on return status code with list and count.
 * Understand: socket connection exception. Change to google DNS will resolve the issue.
 

## Version 0.8.0

_2015-10-04_

 * Add: Add log ability and pretty print log
 * Add: Now config can be changed on each task, rather than the global level.
 * Add: Option to save the log, save the response into results, enable scheduler.
 * Fix: change the visibility of the config/parallel task.
 * Fix: reduced solar critical from 9 to 2.
 * Fix: change HTTP Store to be singleton from static functions
 * Test: Test passed JDK 1.7 and JDK 1.8.0_60