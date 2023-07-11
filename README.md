# Perform a Query With Splunk
This project is meant to demonstrate ability to use Splunk Cloud to upload data, perform searches on data and perform general operations within the tool.

<h2>Scenario</h2>
In this project, I act as a security analyst working at the fictional, e-commerce store, Buttercup Games. You've been tasked with identifying whether there are any possible security issues with the mail server. To do so, you must explore any failed SSH logins for the root account.  






<h2>Search for Failed Root Login</h2>
In this step we'll be narrowing our search even further to locate any failed SSH logins for the root account. <br />
We'll do this by simply adding the root words, "fail*" (the * being a wildcard allowing search results to include anything with 'fail' in the word) and "root". These will filter out any results that don't include both of these words within them. <br />
