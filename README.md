# EKS Getting Started Guide Configuration

This is the full configuration from https://www.terraform.io/docs/providers/aws/guides/eks-getting-started.html

See that guide for additional information.

NOTE: This full configuration utilizes the [Terraform http provider](https://www.terraform.io/docs/providers/http/index.html) to call out to icanhazip.com to determine your local workstation external IP for easily configuring EC2 Security Group access to the Kubernetes servers. Feel free to replace this as necessary.

just do a terraform apply and it will make the eks ready with 3 nodes.
After that download the aws-iam-authenticator from below link 

wget curl -o aws-iam-authenticator https://amazon-eks.s3.us-west-2.amazonaws.com/1.16.8/2020-04-16/bin/linux/amd64/aws-iam-authenticator

chmod +x aws-iam-authenticator
mv aws-iam-authenticator /usr/bin

Now in the outputs you will get the kubeconfig file, just create a file in user's home directory

/home/user/.kube/config 

paste the contents in this file
