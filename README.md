# aws-google-scripts
An interface with the aws api that you can use from google scripts!

How to use:

1. Create a new project in google scripts.

2. Copy paste crypto.js, sha256-hmac.js, and aws.js each into their own file and save them.

3. Open up a new a file and setup the AWS variable with AWS.init.

4. Use AWS.request with whatever AWS API request you need! Make sure the headers and parameters are right though. This repo doesn't do much checking.

Example:

```
function myFunction() {
  AWS.init("MY_ACCESS_KEY", "MY_SECRET_KEY");
  var instanceXML = AWS.request('ec2', 'us-east-1', 'DescribeInstances', {"Version":"2015-10-01"});
  ...
}
```
