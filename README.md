
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

<h2>Step-by-Step Guide </h2>

<h4> Task 1: Ingest and Parse Logs </h4>


<h7> 1. Upload <i> `ssh_log.json` </i> into Splunk.</h7>

<h7> 2. Ensure the following fields are extracted correctly</h7>

<h7>  - <i> `event_type` </i> <em>(Successful SSH Login, Failed SSH Login, Multiple Failed Authentication Attempts, Connection Without Authentication) auth_success (true/false/null)</em></h7>

<h7>  - <i> `ssh_log.json` </i> into Splunk.</h7>

<h7>  - <i> `event_type ` </i>  </h7>

<h7>  - <i> `auth_attempts` </i>  </h7>

<h7>  - <i> `id.orig_h (source IP)` </i>  </h7>


<h7>  - <i> `id.resp_h (destination host)` </i>  </h7>


<h7> 3. Run a validation search:</h7>

<table>
     <thead>
       
          index=ssh_log | stats count by event_type
</thead> 
</table>







 
