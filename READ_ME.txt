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
		
		
I can explain how believe I demonstrated Cyderes's "Core Values" to this exercise.

Customer 1st: 
	This is probably the hardest value a new applicant can demonstrate. Inherently applicants are going to be working for themselves in this scenario.
	I believe demonstrating my thought process can provide a clear picture as to the kind of work I would be putting into the customer. The first thing I 	      noticed when reading over the challenge assesssment was that there was no clearly defined format that the output needed to be displayed in. In order 	   to maximize my chances of success I reasearched the format of the data sample to try and determine it's orgin. Understanding where the data came from 	 provides insight into why it was collected. Ultimately this knowledge would be used for determining what information to keep, and if there is any 	   supplemental data enrichment I could provide.

Raise your Hand: 
	Understandably from your point of view, you might say I asked a single question in regards to the environment logstash should be deployed in. From my
	perspective however, If what I said above has any truth to it: "Inherently applicants are going to be working for themselves in this scenario.", then 	      it is understandable that an applicant may feel pressured to appear entirely independent. Initially I felt that I needed to deploy logstash within a  	    Linuxenvironment in order to better demonstrate my familiarity with the Linux syntax. Thruth be told I was having a bear of a time getting it to work 	  at all in Linux. Had I not swallowed my pride and asked for advice, it is feasable that I may have continued to waste effort only to turn in the same  	 result. In the real world understanding that my current approach may not be the best way, and knowing when to ask for help not only saves my 		resources, but the companies resources as well. Embracing the "team" like environment within my current position has been critical towards my 		education/success.

Contstant Improvement: 
	I think this where my submission may differ from that of others. Anyone with a basic understanding of scripting can eventually come to a solution
	to your problem. Especially when given a week to do so. The first thing I did after submitting my task to github was read over everything again and 	    make minor edits. Following that I immediatly began searching for input. I knew my solution provided the answer you were looking for, but I also knew 	  it could be done more efficiently. I was excited to get the opportunity to talk through the problem with someone. If I am not offered a position with 	Cyderes, I am very interested in every way I could make future attempts successful.

Finally there was the issue of stumbling upon a poster asking specifically about your challenge assessment. It felt like cheating to use the help provided there, but when the answer of what I should do about it seemed easy after thinking back on the values listed above. I used the answer because I determined that would be most efficient.It is exactly what I would do working out any problem for you, I would not hesitate to use whatever information or tools at my disposal to get the task completed (within ethical reason). So instead attempting to just take an easy answer and submit an acceptable solution, I saw it as an opportunity to apply the values Cyderes tells me they reward. 
	- I delivered a solution to the problem at hand by first "Making it work"
	- Reached out for input on ways that I could "Make it work better"
	- Discovered a possible flaw within the hiring process that may undermine the spirit of the Challenge Assessment.
	- Passed my solution and discoveries to the interested parties for further evaluation, and waited for further input.
		
I do believe there are many topics within Cyderes's "Group Values" that I have demonstrated positively, but it feels pedantic to point out where I may have been "respectful","honest", "ethical". These are probably qualities that should shine through without much explanation though.







