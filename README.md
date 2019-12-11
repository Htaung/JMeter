# JMeter
Note about Jmeter 


Performance Testing with JMeter 3 Third Edition
page 100

Overriding properties
One way is to
directly edit jmeter.properties, which resides in the JMETER_HOME/bin


An	example	of	running	in	non-GUI	mode

//On Unix
./jmeter	-n	-t	[path	to	test	script]	-l	[path	to	results	files]

//On Window
jmeter.bat	-n	-t	[path	to	test	script]	-l	[path	to	results	files]


jmeter -n -t google_maps.jmx -l google_maps_result.csv


View result files as aggregate report 
Open jmetergui
Create new test plan 
Test Plan > Add > listener > Aggregate Report

In aggregate report > Click Browse the result file and open


Recording	scripts	is	where	you	will	spend	most	of	your	time.	It	is	often	the	first	step	to
develop	test	plans	for	applications.	

<h4>Recording	scripts	via	the	Chrome	browser extension </h4>
by using BlazeMeter browser plugin can record user interaction into JMX, Selenium format.

<h4>Converting	HTTP	web	archives	(HAR)	to JMeter	test	plans </h4>
Go to browser developer tool => R+click inspect elements
Click Network Tab > Preserve Log
browse website
and in the network tab => R click and select copy > all as HAR or save all as HAR with content
then go to HAR to JMX converter and convert to jmeter script (JMX)

<h4> Feeding	data	into	a	script </h4>
The way to accomplish this is by supplying an input datafile to the test script. The file is
normally in the form of comma-separated values (CSV)

<code>
CSV Data Set Config to the test plan by navigating to Test Plan | Add | Config
Element | CSV Data Set Config. Let’s configure it:
1. In the Filename box, enter input.txt.
2. Leave the rest of the entries blank
</code>

Using timers
By default, when test scripts are recorded in JMeter, they contain no pauses between page
requests. This is sometimes known as the think time in test scripts
 In JMeter, the ways to achieve these pauses are through
timers. JMeter comes with a wealth of timers to achieve this purpose.

<h4> Manageing HTTP Session </h4>
For instance, a user called Joe could be given admin privileges while Susan is only given user privileges.
Whatever the case, JMeter has a way to maintain HTTP user sessions for your test scripts.

Add HTTP Cookie Manager to the test plan by navigating to Test plan | Add |
Config Element | HTTP Cookie Manager.
Save and run the test plan.

How it works…
The HTTP Cookie Manager stores and sends cookies like a web browser does. The cookie
of any request that contains one is automatically extracted and stored by the component to
be used for all future requests from that particular thread. Each JMeter thread gets its own
session just like in a regular web browser to prevent users’ sessions from overlapping with
each other.
