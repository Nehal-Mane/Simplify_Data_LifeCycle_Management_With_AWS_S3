# Simplify Data LifeCycle Management With AWS S3

1. Sign in to the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3/.

2. In the navigation bar on the top of the page, choose the name of the currently displayed AWS Region. Next, choose the Region in which you want to create a bucket.

3. In the left navigation pane, choose Buckets.

4. Choose Create bucket.
 The Create bucket page opens.

5. Under General configuration, view the AWS Region where your bucket will be created.

6. Under Bucket type, choose General purpose.

7. For Bucket name, enter a name for your bucket.
The bucket name must:
- Be unique within a partition. A partition is a grouping of Regions. AWS currently has three partitions: aws (Standard Regions), aws-cn (China Regions), and aws-us-gov (AWS GovCloud (US) Regions).
- Be between 3 and 63 characters long.
- Consist only of lowercase letters, numbers, dots (.), and hyphens (-). For best compatibility, we recommend that you avoid using dots (.) in bucket names, except for buckets that are used only for static website hosting.
- Begin and end with a letter or number.After that create the bucket
8. Click on Bucket Name -> Management -> Create lifecycle rule
- `Lifecycle rule name: first-life-cycle-rule`
- `select Apply to all object in the bucket`
- `click checkbox of I acknowledge that this rule will apply to all`
- `click checkbox of Move current versions of object between storage classes`
- `Standard-IA : 30`
- `Glacier Instant Retrieval : 60`
- `Glacier Deep Archive : 150`
- `click checkbox of Move current versions of object between storage classes`
- `Standard-IA : 20`
- `Glacier Instant Retrieval : 40`
- `click checkbox of Expire current versions of object : 150`
- `Permanently delete noncurrent versions of object : 75 days`
- `click checkbox of Delete expired object delete markers or incomplete multipart upload`