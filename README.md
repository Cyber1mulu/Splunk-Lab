
<h3> Project:SSH Log Analysis using Splunk </h3>

<h3>Object</h3>
  The goal of this project is to analyze SSH authentication logs to detect:

  - Successful logins (who connected, from where)
  - Failed login attempts (possible brute-force or password spraying)
  - Multiple failed authentication attempts (indicators of brute-force)
  - Connections without authentication (potential scanning or incomplete sessions)
  
<h3>Lab Set Up and Perparations </h3>

<h6> 1 Go to Apps > Search & Reporting.</h6>
<h6> 2 Click Add Data → Upload.</h6>
<h6> 3 Select the provided ssh_log.json file and upload it.</h6>
<h6> 4 Choose sourcetype = _json so Splunk automatically extracts fields.</h6>
<h6> 5 Index it under a new index, e.g., ssh_logs.</h6>
<h6> 6 Review and click on start searching </h6>





 
