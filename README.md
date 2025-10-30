https://my-cloud-demo-website.s3.us-east-1.amazonaws.com/add.html.txt 
THIS IS MY WEBSITE ENDPOINT URL

☁️ Task 6: Host and Deploy a Web Application on the Cloud

🎯 Objective

The aim of this task is to deploy a static web application (a simple HTML-based website) on a cloud platform, making it accessible publicly through the internet.
This helps in understanding cloud hosting, public access configuration, and web deployment using services like AWS S3.


---

🧰 Tools Used

Amazon Web Services (AWS S3) – For hosting the static website

VS Code / Notepad – For creating the HTML file

Web Browser – To test and verify the website

AWS Console – For managing the bucket and configuration



---

⚙️ Implementation Steps

Step 1: Create Project Folder

A new folder was created on the local computer named “my-cloud-demo-website” to store the HTML files for deployment.

Step 2: Create a Simple Web Page

A basic HTML file named index.html was created with the following content:

<!DOCTYPE html>
<html>
<head>
  <title>My Cloud App</title>
</head>
<body>
  <h1>Hello Cloud!</h1>
  <p>This is my first web app hosted on the cloud.</p>
</body>
</html>

This file serves as the home page of the web app.

Step 3: Create an S3 Bucket

Logged in to the AWS Management Console.

Opened Amazon S3 and clicked on Create bucket.

Gave a unique name (e.g., my-cloud-demo-website) and selected a region (e.g., us-east-1).

Left default settings and created the bucket successfully.


Step 4: Upload Website Files

Opened the created bucket → Upload section.

Uploaded the index.html file into the bucket.

Confirmed that the file appeared under the Objects tab.


Step 5: Enable Static Website Hosting

Opened the Properties tab of the bucket.

Scrolled down to Static website hosting and clicked Edit.

Selected Enable → chose Host a static website.

Set Index document: index.html.

Saved the settings and copied the Website endpoint URL provided by AWS.


Step 6: Set Public Permissions

Went to the Permissions tab.

Disabled “Block all public access” to allow visitors to view the website.

Added a Bucket Policy allowing public read access:


{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-cloud-demo-website/*"
    }
  ]
}

Saved the policy to make all files inside the bucket publicly accessible.

Step 7: Test the Hosted Web App

Copied the Website endpoint from the Static website hosting section.

Opened the link in a browser — the webpage displayed “Hello Cloud!”, confirming successful deployment.

Took screenshots showing:

The live website in the browser

The AWS S3 bucket console with hosting enabled




---

🧠 Outcome

By completing this task:

A static web app was successfully hosted and deployed on AWS Cloud.

The app is now accessible publicly through a cloud-generated URL.

Gained practical understanding of:

Creating and managing AWS S3 buckets

Setting permissions and bucket policies

Hosting and testing static web content online




---

📸 Deliverables

Screenshot of the live website in a browser

Screenshot of the AWS S3 console showing the bucket with static website hosting enabled

Source code (index.html) file



---

Would you like me to make a shorter version (around 1 paragraph) of this same description — for writing in your Excel sheet or summary report?
