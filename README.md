# Perform a Query With Splunk
This project is meant to demonstrate ability to use Splunk Cloud to upload data, perform searches on data and perform general operations within the tool.

<h2>Scenario</h2>
In this project, I act as a security analyst working at the fictional, e-commerce store, Buttercup Games. You've been tasked with identifying whether there are any possible security issues with the mail server. To do so, you must explore any failed SSH logins for the root account.  

<br />
<br />

<h2>Perform Basic Search</h2>
In this step, we'll be navigating to the 'Search & Reporting' section of Splunk Cloud and beginning our search query "index=main". This query indicates that the results shown, should only come from the data repository, "main". We will also change our timeline filter to "All time". <br />
<img src="https://i.imgur.com/1h5YrUD.png" height="80%" alt="Basic Search"/> 
To properly analyze the results, it is very important to take note of the host, source, and sourcetype fields. These provide essential information that will need to be utilized to properly perform any data evaluations. <br />

<br />
<br />

<h2>Narrow The Search</h2>
In this scenario, it is essential to narrow the search results for events from the mail server to explore any failed SSH login for the root account on the mail server. <br />
We can do this by simply adding "host=mailsv" to our search bar. <br />
<img src="https://i.imgur.com/3o2gnPo.png" height="80%" alt="Narrow Search 1"/> <br />
Notice that the search result amount lowers from 219,728 results, down to 9,829 in this instance.<br />
We can also narrow our search like this by clicking "host" in the "SELECTED FIELDS" and selecting "mailsv". <br />
<img src="https://i.imgur.com/TXaSIdh.png" height="80%" alt="Narrow Search 2"/> <br />

<br />
<br />

<h2>Search For and Evaluate Failed Root Logins</h2>
In this step we'll be narrowing our search even further to locate any failed SSH logins for the root account. <br />
We'll do this by simply adding the root words, "fail*" (the * being a wildcard allowing search results to include anything with 'fail' in the word) and "root". These will filter out any results that don't include both of these words within them. <br />
<img src="https://i.imgur.com/1gol3gf.png" height="80%" alt="Failed Root Login 1"/> <br />

Note that the occurence of the specified keywords are highlighted within the search results. <br />
It should also be noted and reported that there are over 300 results after our filtering, which may very well be cause for alarm for Buttercup Games as each result eludes to a failed login attempt for the root user within the "mailsv" host. <br />

<br />
<br />

<h4>End of Project</h4>
