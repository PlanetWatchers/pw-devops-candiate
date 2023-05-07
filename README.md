## Task Description
Create an Argo workflow that downloads a random quote from `https://thesimpsonsquoteapi.glitch.me/` and saves it to an S3 bucket. Then trigger another step in the workflow that will download an image from the quote JSON and store it on the same S3 bucket.
## Requirements
1. Use AWS infrastructure and Terraform to provision and manage the required resources (e.g., EC2, S3, IAM, etc.).
2. Use Argo workflow YAML to define the workflow.
3. Use Kubernetes to run the Argo workflow.
4. Use S3 server-side encryption with a KMS key to secure the stored data.
5. Use S3 lifecycle policies to optimize costs by transitioning objects to cheaper storage classes over time.
## Steps
1. Use Terraform to provision the following resources in AWS:
   - An S3 bucket with server-side encryption and a KMS key.
   - An IAM user with programmatic access to AWS and limited permissions to the S3 bucket and KMS key.
   - A Kubernetes cluster with Argo Workflow installed.
2. Create an Argo workflow that performs the following steps:
   - Download a random quote from `https://thesimpsonsquoteapi.glitch.me/` and save it to a local file.
   - Use the AWS CLI to extract the image URL from the quote JSON and download the image.
   - Use the AWS CLI to copy the quote file and the image file to the S3 bucket with server-side encryption.
3. Use Kubernetes to run the Argo workflow.
4. Configure S3 lifecycle policies to transition objects to cheaper storage classes (e.g., from Standard to Infrequent Access) after a certain period of time (e.g., 30 days).
## Evaluation Criteria
The devops test task will be evaluated based on the following criteria:
1. Completeness: The task should be completed fully and correctly according to the requirements.
2. Security: The task should follow security best practices, especially regarding IAM, S3 encryption, and KMS key management.
3. Optimization: The task should optimize costs by using S3 lifecycle policies to transition objects to cheaper storage classes over time.
4. Maintainability: The task should be easy to understand and maintain in the future, with clear documentation and comments where appropriate.
5. Creativity: The task should show creativity and originality in solving the problem, especially regarding the implementation of the workflow and the use of AWS services and Terraform.
