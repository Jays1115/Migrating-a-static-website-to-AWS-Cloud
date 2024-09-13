# Migrating A Static Website to AWS Cloud

<h2>Description</h2>
Request: The city required the migration of its beach wave size prediction page to AWS to enhance the reliability and availability of the service.
<br><br>
Solution: Implemented hosting of a static web page using Amazon S3, ensuring improved performance, scalability, and reliability. Configured the S3 bucket for static website hosting, enabled public access, and integrated appropriate permissions for secure and seamless operation. This solution optimized user access to real-time wave size predictions while reducing downtime and maintenance overhead.

<h2>Program walk-through:</h2>

<p align="center">
Navigating to the S3 Section within AWS. AWS has already populated the S3 instances needed for this lab: <br/>
<img src="Screenshot 2024-09-13 at 9.10.12 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Selecting the correct S3 bucket associated with the beach website (website-bucket-cfc90080):  <br/>
<img src="Screenshot 2024-09-13 at 8.15.48 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reviewing objects in the S3 bucket and renaming the text.html file to fit its function. This file contains the code for the error page, which opens whenever something goes wrong: <br/>
<img src="Screenshot 2024-09-13 at 8.20.29 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="Screenshot 2024-09-13 at 8.25.33 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ensuring that “block all public access” is set to “off” so that the static website’s visitors will be able to access the website when its launched:  <br/>
<img src="Screenshot 2024-09-13 at 8.29.36 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reviewing the bucket policy. <br/>
Policy details: <br/>
- This policy allows public access to the S3 bucket. <br/>
- Effect says this policy will Allow access. <br/>
- Principal defines who has access. In this case, * represents anyone. <br/>
- Action defines what users can do to objects in the bucket. In this case, users can only retrieve data with GetObject. <br/>
- Resource specifies that this policy applies to only this bucket. <br/>
<img src="Screenshot 2024-09-13 at 8.32.53 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Navigated to the S3 bucket properties section to enable static website hosting:  <br/>
<img src="Screenshot 2024-09-13 at 8.37.20 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Static website hosting is enabled:  <br/>
<img src="Screenshot 2024-09-13 at 8.42.52 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
Copy & pasted the bucket website endpoint into my internet browser to see if the website has been successfully enabled: 
<img src="Screenshot 2024-09-13 at 8.45.19 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
Renaming the S3 object to reflect its function within website:  <br/>
<img src="Screenshot 2024-09-13 at 8.48.14 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="Screenshot 2024-09-13 at 8.48.34 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
