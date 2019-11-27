# JMeter
Note about Jmeter 


Performance Testing with JMeter 3 Third Edition
page 60

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
