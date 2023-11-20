## Customize AWS Config resource tracking in AWS Control Tower environment
This github repository is part of AWS blog post https://aws.amazon.com/blogs/mt/customize-aws-config-resource-tracking-in-aws-control-tower-environment/

Please refer to the blog for what this sample code does and how to use it.

## Changes in this fork
This is a modified solution that accepts an include account list parameter for config customization. The original solution accepts an exclude account list.

## Steps to deploy this fork

1. Create an S3 bucket in your Management account and region where you intend to deploy this solution.
2. Create a folder inside this S3 bucket with name: 'ct-blogs-content'.
3. Upload the 2 .zip files from this repo to the S3 bucket folder from step #2.
4. Delpoy the CloudFormation template.yaml file.
5. Template Parameters:

	- **CloudFormationVersion**: Increment version when deploying an update. default is 1 for teh initial deploymemt.
	- **IncludedAccounts**: List of accounts where config customization is desired.
	- **ConfigRecorderExcludedResourceTypes**: List of all resource types to be excluded from Config Recorder.
	- **LambdaS3Bucket**: Name of the S3 bucket where lambda zips are uploaded. Do not enter the folder prefix.


## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

