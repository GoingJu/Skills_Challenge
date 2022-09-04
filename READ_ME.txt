demo.conf -

	-Input:  The input portion of the config file is defining it's data source. One thing to note in this portion
		 is I have the 'sincedp_path' set to NUL. I was having issues where I wasn't getting any output. This may
		 not have been my problem, but included it to demonstrate that I understand the sincedb_path is used to
		 keep track of the current position of monitored files.
	
	-Filter: This is broken up into three plugins. The data provided to me provided two distinct patterns to parse. The
		 first of which is handled with the 'dissect' filter plugin. This defines the input as "message" and assigns variables
		 to individual sections determined by blank spaces. I included the variables "hyphen1" and "hyphen2"
		 It's at this point that I feel like I need to let you know that while reading into the different filters and
		 finding what might be most efficient, I stumbled upon a post online where someone was asking for advice on how to
		 complete this assignment here:
		 	https://discuss.elastic.co/t/logstash-plugins/282713
		 This far from gave me a "copy & paste" answer though. What it did do was tell me that the 'grok' filter likely wasn't ideal.
		 
		 Next is the kv filter. Following the hyphens in the log output was a new pattern "variable=output variable2=output". The kv
		 filter was able to break this down further into it's individual components.

		 Last is the mutuate filter. This was used to remove any redudant components to the final output. 	
		 
	-Output: The output portion of this is the one section I'm not sure I've done efficiently. I was unable to get a format that I has happy
		 with using the filter plugins alone. The output simply states that it is to be written to a file using specific variables from the
		 filters. Following the 'format =>' definition, I simply wrote out EXACTLY how I want it to appear.


OUTPUT.json - 
		This is the output produced by demo.conf

demodata.txt - 
		Is the data you provided for me to use.

Goings - Skills Assessment.png -

		This is a screenshot I took after I got it to work.

Tips.txt -
		Just some notes and issues I had to trouble shoot.




