
see: https://aws.amazon.com/jp/blogs/networking-and-content-delivery/resizing-images-with-amazon-cloudfront-lambdaedge-aws-cdn-blog/

deploy:

```
aws s3 cp --recursive dist/ s3://<code-bucket>/

aws cloudformation deploy \
--capabilities CAPABILITY_IAM \
--template-file resizing-images-with-amazon-cloudfront-lambdaedge-aws-cdn.yaml \
--stack-name resizing-images-cf \
--parameter-overrides LambdaSourceBucketName=<code-bucket>
```

