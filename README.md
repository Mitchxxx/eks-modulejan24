..... PUBLISH TO GITHUB .....

1. Create an empty repo with just MIT License or create another directory using mkdir in your main working directory, you can call it my eks module, this will be your official published module on github

2. Copy all the files from your modules directory onto this new clone repo or directory (main, vars, outputs, and data etc)

3. cd into the new folder and add a README.md file also, to tell or instruct people on how to use your EKS Module. see sample readme file below. copy and paste.


# MY AWESOME TERRAFORM MODULE TO PROVISION EKS CLUSTER WITH CUSTOM NETWORKING  ----->

# Sample usage:

~~~ 

module "eks-module" {
  source         = "github.com/Mitchxxx/eks-modulejan24"
  region         = "Enter your Providers region here"
  vpc_cidr       = "10.0.0.0/16"
  dns_hostnames  = true
  dns_support    = true
  pub_one_cidr   = "10.0.1.0/24"
  pub_two_cidr   = "10.0.2.0/24"
  priv_one_cidr  = "10.0.3.0/24"
  priv_two_cidr  = "10.0.4.0/24"
  az_one         = "Enter your first az"
  az_two         = "Enter your second az"
  vpc_id         = "aws_vpc.eks_vpc.id"
  eks_version    = "1.26"
  ami_type       = "AL2_x86_64"
  instance_types = ["m5.large", "m5.large", "m5.large"]
  capacity_type  = "ON_DEMAND"

}

~~~