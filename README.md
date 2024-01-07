<h1>Cloud Resume Project</h1>

<h2>Description</h2>
 The goal of this project was to leverage the power of the Cloud (in my case AWS) and some of it's key services to create a fully functioning serverless web application that "serves" (no pun intended) as a resume or portfolio.

In summary, I setup an S3 bucket that stores all of my HTML, CSS, and JavaScript files for the website, and linked it as an origin to my CloudFront distribution to host the website. I set this up to be a secure site by reddirecting traffic to HTTPS and using AWS Certificate Manager (ACM) for the SSL certs. I also bought a domain to use with Route53 as my domain registrar, and created the A records to point my new awesome domain name (dillonmeacham.net) to my CloudFront distro.

I then created a visitor counter for the site using a DynamoDB table and Lamda function in Python for the API that gets the viewer count from the table, and displays it on the site after adding the necessary script tags in my HTML.

After the site was functional and in production, I integrated CI/CD using GitHub actions to run a YAML workflow that updates my S3 bucket automatically after I commit and sync any code changes I make to my site via VSCode. <br />


<h2>Environments Used </h2>

- <b>AWS Route 53</b>
- <b>AWS CloudFront</b>
- <b>AWS Certificate Manager</b>
- <b>Amazon S3</b>
- <b>AWS Lambda</b>
- <b>AWS DynamoDB</b>
- <b>GitHub Actions</b>

<h2>Architecture Diagram</h2>

<p align="center">
<img src="https://ibb.co/74XXVK6" height="100%" width="100%" />
<br />
<br />
