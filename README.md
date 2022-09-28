# s3-deletion

If you create the versioning enabled s3 bucket using cloud formation. After that if objects are uploaded and Access points created manually for that bucket. when you try to delete the cloudformation stack it wont get deleted because its non-empty and access points are associated with the bucket.

For deleting it you must have to empty the bucket manually and delete its access points which are created manually.


Custom Resources

Custom resources enable you to write custom provisioning logic in templates that AWS CloudFormation runs anytime you create, update (if you change the custom resource), or delete stacks. For example, you might want to include resources that aren’t available as AWS CloudFormation resource types. You can include those resources by using custom resources. That way you can still manage all your related resources in a single stack.


Am passing the BucketName and the Account Id to the custom resource lambda function which I created during the stack creation time. Lambda will take these inputs and delete the bucket contents and associated access points.

Custom resource will trigger and delete the layer once i’ll receive the Request Type is delete from CFT.

You can read further on this on my blog

[https://medium.com/@shashavalijetty/automate-the-deletion-of-non-empty-s3-bucket-created-using-cloudformation-by-deleting-its-access-3f575a539d4e](url)

