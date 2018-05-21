# Hive

Jupyter Notebooks for the Coursera course "Big Data Analysis: Hive, Spark SQL, DataFrames and GraphFrames".

Notes for the assignment tasks

Asisgnment 1 - Task 1
add before running the first time
CREATE DATABASE demodb LOCATION '/user/jovyan/af_store';
and remove before submission.

Asisgnment 1 - Task 2


Compare most popular tags in year 2016 with tags in 2009. Tag popularity is the number of questions (post_type_id=1) with this tag. Output top 10 tags in format:

tag <tab> rank in 2016 <tab> rank in 2009 <tag> tag popularity in 2016 <tag> tag popularity in 2009

Example:

php 5 3 1234 5678

For 'rank' in each year use rank() function. Order by 'rank in 2016'. 

For the tasks 2, 3, etc. use the tables 'posts' and 'users' from the database 'stackoverflow_'. 'Posts' is partitioned by year and by month, columns correspond to the fields of the lines described above:

    id INT
    post_type_id TINYINT
    date STRING
    owner_user_id INT
    parent_id INT
    score INT
    favorite_count INT
    tags ARRAY<STRING>
    year STRING (partition)
    month STRING (partition)

'Users' contains the following columns:

    id INT
    reputation INT
    creation_date STRING
    display_name STRING
    location STRING
    age INT

Proceed with Hive assignment tasks.


In this task all top 10 tags of 2016 exist in 2009. So you don't need to care about NULL-s.

Notebook "demos/course02_week02-Demo.ipynb" is a very good starting point. You just need to modify query.hql.

You don't need to write any regex. Use stackoverflow_ database (details in demo notebook mentioned above).

Using WITH helps to make query code clean and readable.

Here is third result from correct response, it should help You with debugging: 
android	3	65	183269	1997


Lines from 'posts'
    45	2	2008-08-01T12:56:37.920	39	39	34	NULL	NULL	2008	2008-08
    243	2	2008-08-01T22:31:36.137	71	234	12	NULL	NULL	2008	2008-08
    304	2	2008-08-02T01:38:14.077	91	109	2	NULL	NULL	2008	2008-08
    629	2	2008-08-03T07:28:54.070	122	626	38	NULL	NULL	2008	2008-08
    893	2	2008-08-03T23:38:05.113	234	871	6	NULL	NULL	2008	2008-08
    1394	2	2008-08-04T16:38:03.667	91	1390	16	NULL	NULL	2008	2008-08
    1686	2	2008-08-04T23:08:18.603	316	1669	43	NULL	NULL	2008	2008-08
    2069	2	2008-08-05T10:22:55.653	307	2056	23	NULL	NULL	2008	2008-08
    2712	2	2008-08-05T19:09:08.213	350	2639	10	NULL	NULL	2008	2008-08
    2799	2	2008-08-05T20:26:08.103	308	2767	34	NULL	NULL	2008	2008-08
    2822	2	2008-08-05T20:46:22.930	75	2815	2	NULL	NULL	2008	2008-08
    2924	2	2008-08-05T22:13:16.517	25	2898	2	NULL	NULL	2008	2008-08
    3066	2	2008-08-06T03:43:58.563	430	3033	3	NULL	NULL	2008	2008-08
    3449	2	2008-08-06T14:22:37.837	115	3432	-4	NULL	NULL	2008	2008-08
    3543	2	2008-08-06T15:24:00.787	399	3530	37	NULL	NULL	2008	2008-08
    3860	2	2008-08-06T18:59:36.467	431	3839	11	NULL	NULL	2008	2008-08
    4004	1	2008-08-06T21:18:47.357	525	NULL	31	16	[".net","authentication","encryption","ssl"]	2008	2008-08
    4071	2	2008-08-06T22:29:57.073	525	4004	6	NULL	NULL	2008	2008-08
    4395	2	2008-08-07T04:47:45.830	60	4392	6	NULL	NULL	2008	2008-08
    4403	2	2008-08-07T04:54:27.937	389	4371	30	NULL	NULL	2008	2008-08
