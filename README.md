# s3-deletion

If you create the versioning enabled s3 bucket using cloud formation. After that if objects are uploaded and Access points created manually for that bucket. when you try to delete the cloudformation stack it wont get deleted because its non-empty and access points are associated with the bucket.

For deleting it you must have to empty the bucket manually and delete its access points which are created manually.

Custom Resources

Custom resources enable you to write custom provisioning logic in templates that AWS CloudFormation runs anytime you create, update (if you change the custom resource), or delete stacks. For example, you might want to include resources that aren’t available as AWS CloudFormation resource types. You can include those resources by using custom resources. That way you can still manage all your related resources in a single stack.


Validation
After creating the template i uploaded the file sample.txt to the bucket you can see the version of that file as well

You can read further information on Custom Resource.
