# AWS IAM Least Privilege Lab

## Project Objective

Create an AWS IAM solution using least privilege principles that allows users to read objects from a specific S3 bucket while preventing modification or deletion of resources.

## Services Used

- AWS IAM
- Amazon S3

## Concepts Demonstrated

- IAM Users
- IAM Groups
- Custom IAM Policies
- Least Privilege Access Control
- Resource-Based Permissions

## Lessons Learned

During testing, the AWS Management Console required the `s3:ListAllMyBuckets` permission in order for the user to view available buckets. Without this permission, the user received an error stating they did not have permission to list buckets.

This demonstrated how AWS console permissions can differ from direct API permissions and highlighted the importance of testing IAM policies from the end-user perspective.

The final policy allowed:

* View bucket contents
* Read objects

The final policy prevented:

* Uploading objects
* Deleting objects
* Modifying bucket settings

This implementation follows the Principle of Least Privilege.
