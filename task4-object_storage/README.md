# Task 4: Object Storage

## Description.

Goal is to create and configure Public and Protected Object Storage Containers (S3 buckets) for hosting and storing application resources. 

- **Public S3 bucket** - Host the front end static website. (HTML,CSS, JS) 
- **Protected S3 bucket** - Store logs / model data / AI forecast results. 

## How to Deploy using AWS Console.

### Bucket policies.

Public bucket policy allows ```GetObject``` for everyone.
![Bucket_policy](/task4-object_storage/Images/bucket-policy.jpg)


Protected bucket policy retains default Block-public-access settings. 

![Protected bucket policy](/task4-object_storage/Images/bucket-policy-protected.jpg)

--------------------------------------------------------------

### CloudFront stack & S3 bucket.

Uploaded the yaml file to the cloudfront stack. 
![S3_bucket_template](/task4-object_storage/Images/s3-bucket-template.jpg)

  - Create S3 bucket &rarr; **weather-app-public-bucket**
    1. Files uploaded: index.html, style.css, app.js
    2. Enable Static website hosting. 

![S3_public_bucket_files](/task4-object_storage/Images/publicbucket_file_upload.jpg) 

  - Create S3 bucket &rarr; **weather-app-protected-bucket**
    1. No public ACLs.
    2. Intended for backend data. 

Public URL: 
``` http://weather-app-public-bucket.s3-website.eu-north-1.amazonaws.com ```

---------------------------------------------------------------

### Connect Frontend to Backend.

Updated ```app.js``` to use EC2 public IP
![Protected bucket policy](/task4-object_storage/Images/app.js_update.jpg)

### Check my Output!!

Frontend site loads successfully.
Protected bucket access denied from public. 
Fetching live JSON from Flask backend on EC2.

![Webpage loaded successfully!](/task4-object_storage/Images/frontend_site.jpg)





 
