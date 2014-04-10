If you live in an area that experiences earthquakes, you might
wish to have some information about them.

But lets face it, all the multimedia websites are rather mind numbing
when trying to search for what you want.

Conveniently, the USGS provides this data via JSON format.

For now, this utility 'showeq' shows earthquake data in a human
understandable format.

For example:

    perl ./showeq -a 35.5635277 -o -97.5437221 Oklahoma

Parses the one week feed to get the distance of quakes from me in Oklahoma.

Abbreviated example output is below:

<pre>
Quake usc000pe90 at 11.26mi SSW of Guthrie, Oklahoma
magnitude: 2.8
time: Thu Apr 10 08:18:47 2014
distance: 2472.28mi

Quake usc000pdzw at 10.63mi SW of Guthrie, Oklahoma
magnitude: 3.7
time: Thu Apr 10 03:19:43 2014
distance: 2473.10mi

Quake usc000pdy4 at 10mi SSW of Guthrie, Oklahoma
magnitude: 4.1
time: Thu Apr 10 02:33:57 2014
distance: 2472.82mi

Quake usc000pdwa at 1.26mi ESE of Perry, Oklahoma
magnitude: 2.6
time: Thu Apr 10 01:40:52 2014
distance: 2506.76mi

...
</pre>


If you find this app useful, I accept bitcoin donations at:

<a href="bitcoin:1H1t15fNXtNEgZQBbdVimqZJ4xgpqfAvSd">1H1t15fNXtNEgZQBbdVimqZJ4xgpqfAvSd</a>
