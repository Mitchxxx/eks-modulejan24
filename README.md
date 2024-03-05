# MY AWESOME TERRAFORM MODULE TO PROVISION EKS CLUSTER WITH CUSTOM NETWORKING  ----->

# Sample usage:

~~~ 

module "modulejan24" {
  source                 = "github.com/Mitchxxx/terraform-eks-modulejan24"
  region                 = "Enter your Providers region here"
  vpc_cidr_block         = "10.0.0.0/16"
  vpc_dns_hostnames      = true
  vpc_dns_support        = true
  public_sub1_cidr_bock  = "10.0.1.0/24"
  public_sub2_cidr_bock  = "10.0.2.0/24"
  private_sub1_cidr_bock = "10.0.3.0/24"
  private_sub2_cidr_bock = "10.0.4.0/24"
  dest_cidr_bock         = "0.0.0.0/0"
  availability_zone_1    = "Enter your first az"
  availability_zone_2    = "Enter your second az"
  eks_version            = "1.27"
  ami_type               = "AL2_x86_64"
  cluster_name           = "Enter Name of cluster here"
  capacity_type          = "ON_DEMAND"
  node_group_name        = "Enter name of NodeGroup here"

}

~~~
