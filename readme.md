AWS Network Firewall Module
AWS Network Firewall Module which creates

Network Firewall rule group 
Network Firewall Policy with attached above rule group
Network Firewall 
Network Firewall logging
Customer Master Key
Network Firewall S3 buket and store logs
Network Firewall S3 bucket policy

Usage
 module "networkfirewall" {
 
    source                  = "../networkfirewall/"
    networkfirewall-name    = "koho-datalake-nfw"
    firewall-subnet-b       = module.firewall-subnet-2.subnet_id
    networkfirewall-group   = var.networkfirewall-group
    firewall-subnet-a       = module.firewall-subnet-1.subnet_id
    vpc_id                  = module.vpc.vpc_id
    env                     = var.env
    capacity                = var.capacity
 }


