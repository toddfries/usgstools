If you live in an area that experiences earthquakes, you might
wish to have some information about them.

But lets face it, all the multimedia websites are rather mind numbing
when trying to search for what you want.

Conveniently, the USGS provides this data via JSON format.

This utility 'showeq' shows earthquake data in a human
understandable format.

For example:

    perl ./showeq -f 1.0_week -a 35.5635277 -o -97.5437221 Oklahoma

Parses the one week feed to get the distance of quakes from me in Oklahoma.

The feed names are as found at https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php:

 {all,1.0,2.5,4.5,significant}_{hour,day,week,month}

One can combine them to produce a combined output:

    perl ./showeq -f all_day,1.0_week,2.5_month -a 35.5635277 -o -97.5437221 Oklahoma

Example output is below:

<pre>
                    Date|     Eq Id| Mag|From Home|Location
Thu Aug  3 11:11:46 2017|us2000a45d| 3.3|  10.55mi|  3.78mi ENE of Edmond, Oklahoma
Thu Aug  3 09:50:10 2017|us2000a437| 3.2|  52.39mi| 11.26mi N of Stroud, Oklahoma
Thu Aug  3 06:05:41 2017|us2000a41p| 2.9|  20.55mi|  3.15mi SSE of Guthrie, Oklahoma
Thu Aug  3 01:40:44 2017|us2000a3za| 3.5|  10.63mi|  3.78mi ENE of Edmond, Oklahoma
Wed Aug  2 23:37:59 2017|us2000a3yv| 3.2|  95.01mi| 31.89mi E of Mooreland, Oklahoma
Wed Aug  2 23:33:52 2017|us2000a3yu| 3.2|  93.14mi| 32.52mi NW of Fairview, Oklahoma
Wed Aug  2 21:56:37 2017|us2000a3y4| 4.2|  10.69mi|  3.78mi ENE of Edmond, Oklahoma
Wed Aug  2 18:51:03 2017|us2000a3x3| 2.6| 104.03mi| 10.63mi ESE of Mooreland, Oklahoma
Wed Aug  2 17:16:38 2017|us2000a3vx| 2.6|  10.83mi|  4.41mi ENE of Edmond, Oklahoma
Wed Aug  2 02:49:33 2017|us2000a3k5| 3.0|  10.96mi|  3.78mi ENE of Edmond, Oklahoma
Wed Aug  2 00:18:53 2017|us2000a3ja| 3.5|  11.07mi|  4.41mi ENE of Edmond, Oklahoma
Tue Aug  1 21:42:17 2017|us2000a3im| 3.0|  10.94mi|  4.41mi ENE of Edmond, Oklahoma
Tue Aug  1 14:43:48 2017|us2000a3eb| 3.3| 104.01mi| 22.52mi ENE of Mooreland, Oklahoma
Tue Aug  1 02:42:22 2017|us2000a353| 2.9|  92.60mi| 32.52mi NW of Fairview, Oklahoma
Mon Jul 31 02:49:30 2017|us2000a2uh| 2.6|  92.37mi| 31.89mi NW of Fairview, Oklahoma
Sun Jul 30 21:12:32 2017|us2000a2sr| 2.5| 141.15mi| 23.78mi NE of Buffalo, Oklahoma
Sun Jul 30 10:54:43 2017|us2000a2q9| 2.2| 103.56mi| 21.89mi ENE of Mooreland, Oklahoma
Sat Jul 29 16:09:03 2017|us2000a2kh| 2.6|  49.43mi| 15.67mi W of Perry, Oklahoma
Sat Jul 29 07:32:47 2017|us2000a2hx| 2.5|  49.28mi| 20.00mi W of Perry, Oklahoma
Wed Jul 26 06:21:17 2017|us2000a18u| 2.7|  52.67mi|  2.52mi NNE of Stroud, Oklahoma
Tue Jul 25 21:55:31 2017|us2000a16j| 2.6| 140.38mi| 24.41mi ENE of Buffalo, Oklahoma
Tue Jul 25 19:01:37 2017|us2000a15u| 2.6|  46.77mi|  4.41mi NE of Lindsay, Oklahoma
Sun Jul 23 20:59:00 2017|us2000a09y| 2.9| 141.38mi| 23.78mi NE of Buffalo, Oklahoma
Sun Jul 23 12:11:24 2017|us2000a03i| 3.1|  85.95mi| 25.04mi E of Cherokee, Oklahoma
Fri Jul 21 19:20:04 2017|us20009zj7| 2.6|  53.31mi| 11.26mi N of Stroud, Oklahoma
Fri Jul 21 14:39:38 2017|us20009zdd| 2.7| 140.59mi| 23.15mi ENE of Buffalo, Oklahoma
Fri Jul 21 07:52:38 2017|us20009yzc| 2.9|  52.10mi|  3.15mi N of Stroud, Oklahoma
Fri Jul 21 06:58:59 2017|us20009yxs| 2.9| 143.25mi| 22.52mi NE of Buffalo, Oklahoma
Tue Jul 18 19:20:05 2017|us20009xry| 3.6|  40.44mi| 10.00mi SW of Stillwater, Oklahoma
Tue Jul 18 16:59:51 2017|us20009xqw| 3.2|  52.52mi| 11.89mi N of Stroud, Oklahoma
Tue Jul 18 14:35:39 2017|us20009xna| 2.6|  30.51mi|  5.67mi SW of Tuttle, Oklahoma
Mon Jul 17 21:32:30 2017|us20009x85| 3.6|  88.31mi| 13.78mi SSW of Cherokee, Oklahoma
Mon Jul 17 16:06:34 2017|us20009x2c| 3.3|  66.60mi| 23.15mi S of McCord, Oklahoma
Sun Jul 16 22:51:18 2017|us20009wux| 3.2|  52.58mi| 11.26mi N of Stroud, Oklahoma
Sun Jul 16 22:29:22 2017|us20009wut| 3.2|  68.81mi|  2.52mi ESE of Fairview, Oklahoma
Sat Jul  8 15:20:45 2017|us20009wt3| 2.8|  68.95mi| 11.89mi NW of Pawnee, Oklahoma
Sat Jul 15 18:47:00 2017|us20009wpw| 2.7|  38.95mi| 15.67mi N of Crescent, Oklahoma
Sat Jul 15 18:11:24 2017|us20009wph| 3.0|  52.17mi| 11.26mi NNW of Stroud, Oklahoma
Sat Jul 15 03:44:40 2017|us20009wj3| 2.6|  39.62mi| 12.52mi WSW of Stillwater, Oklahoma
Sat Jul 15 01:28:15 2017|us20009wit| 2.5|  11.11mi|  5.04mi E of Edmond, Oklahoma
Fri Jul 14 10:39:30 2017|us20009wcb| 2.7|  38.15mi|  5.04mi S of Hennessey, Oklahoma
Fri Jul 14 10:11:32 2017|us20009wbx| 3.0|  38.31mi|  5.04mi S of Hennessey, Oklahoma
Fri Jul 14 10:04:22 2017|us20009wbv| 3.4|  51.61mi| 11.26mi NNW of Stroud, Oklahoma
Fri Jul 14 09:55:51 2017|us20009wbt| 2.7|  51.99mi| 11.26mi NNW of Stroud, Oklahoma
Fri Jul 14 09:17:50 2017|us20009wbj| 3.7|  52.15mi| 11.26mi NNW of Stroud, Oklahoma
Fri Jul 14 09:04:50 2017|us20009wbh| 3.5|  52.36mi| 11.26mi N of Stroud, Oklahoma
Fri Jul 14 09:03:30 2017|us20009wbg| 2.9|  51.93mi| 11.26mi NNW of Stroud, Oklahoma
Fri Jul 14 08:47:35 2017|us20009wba| 4.2|  52.41mi| 11.26mi N of Stroud, Oklahoma
Thu Jul 13 19:45:47 2017|us20009w6v| 2.6|  76.31mi| 22.52mi ENE of Taloga, Oklahoma
Thu Jul 13 03:06:24 2017|us20009vx0| 2.6|  69.32mi| 10.63mi ESE of Pawnee, Oklahoma
Wed Jul 12 22:16:56 2017|us20009vvg| 3.5|  49.79mi| 15.67mi W of Perry, Oklahoma
Tue Jul 11 10:27:55 2017|us20009vsm| 2.6|  92.20mi| 31.89mi NW of Fairview, Oklahoma
Wed Aug  2 15:45:26 2017|us10009j1h| 3.3|  10.78mi|  4.41mi ENE of Edmond, Oklahoma
Tue Jul 11 13:59:22 2017|us100098wz| 2.6|  52.66mi| 21.26mi W of Perry, Oklahoma
Tue Jul 11 03:37:35 2017|us100098r6| 2.9|  71.17mi| 11.89mi ESE of Pawnee, Oklahoma
Mon Jul 10 00:08:57 2017|us100098ha| 2.7|  90.05mi| 10.00mi SSW of Cherokee, Oklahoma
Sun Jul  9 20:13:42 2017|us100098g5| 2.5|  76.02mi| 21.89mi ENE of Taloga, Oklahoma
Sun Jul  9 03:59:43 2017|us100098ck| 3.0|  76.09mi| 21.89mi ENE of Taloga, Oklahoma
Sun Jul  9 01:27:41 2017|us100098c2| 2.6|  78.00mi|  4.41mi SW of Helena, Oklahoma
Sat Jul  8 15:20:25 2017|us1000988n| 2.8|  68.41mi| 11.89mi NW of Pawnee, Oklahoma
Fri Jul  7 21:51:23 2017|us10009821| 3.4|  70.63mi| 11.26mi ESE of Pawnee, Oklahoma
Thu Jul  6 18:53:08 2017|us100097ii| 2.8|  73.83mi| 22.52mi SW of Fairview, Oklahoma
Thu Jul  6 10:22:11 2017|us100097bq| 3.1|  83.97mi|  3.15mi SSW of Medford, Oklahoma
Thu Jul  6 03:52:51 2017|us1000976q| 2.5|  69.96mi| 10.63mi NW of Pawnee, Oklahoma
Wed Jul  5 21:36:12 2017|us10009741| 2.6|  82.58mi|  4.41mi SSW of Medford, Oklahoma
</pre>


If you find this app useful, I accept bitcoin donations at:

<a href="bitcoin:1H1t15fNXtNEgZQBbdVimqZJ4xgpqfAvSd">1H1t15fNXtNEgZQBbdVimqZJ4xgpqfAvSd</a>
