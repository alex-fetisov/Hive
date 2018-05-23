Compare most popular tags in year 2016 with tags in 2009. Tag popularity is the number of questions (post_type_id=1) with this tag. Output top 10 tags in format:

    tag <tab> rank in 2016 <tab> rank in 2009 <tag> tag popularity in 2016 <tag> tag popularity in 2009

Example:

    php 5 3 1234 5678

For 'rank' in each year use rank() function. Order by 'rank in 2016'. 


LAST error:

	 ===== Testing (num. 902): STARTING =====
	Executing notebook with kernel: python2
	Testing (num. 902): test CRS902_1 failed on line "javascript	1	5	2771	192"!
		CRS902_1 description: Checking the format
	Testing (num. 902): test CRS902_9 failed on line "javascript	1	5	2771	192"!
		CRS902_9 description: Checking the correctness of tags' rank in 2009
	Testing (num. 902): test CRS902_4 failed!
		CRS902_4 description: Checking Top-1 rank in 2009 and the last of Top-10
	Testing (num. 902): test CRS902_5 failed!
		CRS902_5 description: Checking Top-1 popularity in 2016 and the last of Top-10
	Testing (num. 902): test CRS902_6 failed!
		CRS902_6 description: Checking Top-1 popularity in 2009 and the last of Top-10

	 ===== Testing (num. 902): SUMMARY =====
		Tests passed: crs902_7 crs902_8 crs902_2 crs902_3 mrb17 sp7_1 res1_5 res2_4
		Tests failed: crs902_1 crs902_9 crs902_4 crs902_5 crs902_6
	 ==================================================
	 Duration: 101.0 sec
	 VCoreSeconds: 259 sec 

	 0
