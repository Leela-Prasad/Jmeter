JMeter is a Performance testing tool

Why JMeter?
It is an open source testing tool.
we can test performance of web applications, API’s and databases.
No limit on maximum number of concurrent users.

Test Plan:
Test plan contains all actions and components required for executing performance test script.

Workbench:
It contains components for practice area or temporary storage and are not saved along with Test plan.

Thread Group:
This element is used to configure number of threads(users) on a particular website or endpoint.
Using this element we can configure
1. Number of Users.
2. Simulation time - Duration(seconds)
3. No.of Requests per user - Loop count
4. Rampup period - which describes after how many seconds total number of users defined in the thread group should come.

To view Load test Results we can use below listeners.
1. ViewResultsTree
2. View Results in Table.
3. Graph Results.

Sample Time/Response Time/Load Time/Elapsed time:
It is the difference between time when request was sent and time when response has been fully received.

Latency:
It is the difference between time when request was sent and time when response has started to be received.
so sample time > Latency
   sample time = Latency + Processing Time.

Bytes:
It represents quantity of data in the sample response returned from the server.

Sent Bytest:
It represents quantity of data in the sample request that is invoked from the client.

Connect Time:
It is the time taken to establish TCP connection between client and server using TCP Handshake.

Throughput:
It represents No.of Requests/sec (or) min (or) hr
Throughput - No.of Requests/TimeUnit.

Controller
Controller is a block which contains set of requests.
This block can be executed on a condition also.

1. Simple Controller
It is just a block/folder which contains set of requests.
2. Loop Controller
This will run all the requests inside this controller for a specific number of times.
3. While Controller
This will run all the requests inside this controller until condition is satisfied.
4. If Controller
This will run all the requests inside this controller if condition is satisfied.
5. Interleave Controller
This controller will run the requests alternatively
suppose if a 4 requests
for 1 run it will run 1 request and remaining 3 requests are ignored
for 2 run it will run 2 request
for 3 run it will run 3 request
for 4 run it will run 4 request
for 5 run it will run 1 request
6. Random Controller 
This controller will execute requests randomly.
7. Recording Controller
when we run sample requests in workbench we will select Test Script controller by default so that all requests will come under that, but if we mention as recording controller then this will search recording controller in the thread group and put all requests in that controller.
8. Runtime Controller
This controller is similar to Loop controller, but this controller will run requests until specified time( like 50 sec), where as loop controller it will run requests for specified number of times.
9. Transaction Controller
This controller will give aggregation results of all requests that are present in transaction controller, like response time for all requests, status code, response size for all responses.

Timers:
======
1. Constant Timer
If we want to have some pause after execution of some requests then we can use this constant timer.
some requests will be executed		pause		next requests will be executed

2. Gaussian Timer
This is similar to constant timer but here we will have deviation where this deviation is added to constant timer value, so the pause time will be different because deviation will be different for every pause.

3. Constant Throughput timer
suppose a server is having a throughput of serving 100 requests per minute
and if 200 requests came then first 100 requests will be served and a constant timer is applied and then again it will serve next 100 requests.

Regular Expresssions
====================
Regular Expressions are used to get dynamic values from the websites, so that we can pass these dynamic values for subsequent operations.

Regular Expression Pane consists of below properties.
1 .Apply to - This field represents whether regular expression we defined should apply to only Main sample(or Parent Sample) or to sub samples also.
2. Field to check - This field represents in which part of request this regular expression  applies like body,request Headers,response Headers,Response code,response etc.
3. Name of created variable - variable name which stores regex result.
4. Regular Expression - Regular expression that we need to apply
   Here in Jmeter regular expression must be written in ()
   (.*?) - Matches 1 or more characters(Non greedy Approach)
   (.*) - Matches 1 or more characters(Greedy Approach)

eeeAiiZuuuuAoooZeeee
A.*Z yields 1 match: AiiZuuuuAoooZ
A.*?Z yields 2 matches: AiiZ and AoooZ

5. Template($i$) - we can have multiple regular expressions in a single one resulting in multiple results or groups, so $i$ will tell you from i group you have to take the result.
$2$ - will tell you take result from second regular expression.

6. Match No - Regular expression may match multiple times for a single regex. so to tell which one we need to take we need to mention in Match No


7. Default Value - If the regular expression does not match then created variable will assign with default value.

Cookie Manager
==============
If an application is storing any data in cookies like session id then we have to add cookie manager to get those details.

Html Link Parser
================
In General a page contains links to many other pages, like home page contains links to the entire application if we want to test these links without explicitly recording in test script recorder then we need to use Html Link Parser.
*This should be added as a pre processor to a link whose path is “.*”
Then Html Link Parser will randomly choose one link from the parent response and executes, loop it multiple times if we want to test multiple links.

Http Request
============
To test rest apis we don’t have anything to play and record, so we have to manually create http request and fill the required fields for the endpoint.

Aggregate Report
================
Aggregate Report Listener will give following parameters.
1. Average
2. Median.
3. 90% Line - How much time taken for 90% of requests.
4. Min - minimum time taken in all the requests.
5. Max - maximum time taken in all the requests.
6. Throughput - No of requests per second.
