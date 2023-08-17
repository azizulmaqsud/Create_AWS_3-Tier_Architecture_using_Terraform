# Create_AWS_3-Tier_Architecture_using_Terraform

module "autoscaling" {

   - source      = "./modules/autoscaling"
  
   - namespace   = var.namespace
  
   - ssh_keypair = var.ssh_keypair

   - vpc       = module.networking.vpc
  
   - sg        = module.networking.sg
  
   - db_config = module.database.db_config
  
}

module "database" {

   - source    = "./modules/database"
  
   - namespace = var.namespace

   - vpc = module.networking.vpc
  
   - sg  = module.networking.sg
  
}

module "networking" {

   - source    = "./modules/networking"
  
   - namespace = var.namespace
  
}

# Thank You!
# Stay Connected !!

https://www.youtube.com/channel/UCNwP7KEElaJ7cdDTLP-KbBg

https://www.linkedin.com/in/azizul-maqsud/

https://azizulmaqsud-1684501031000.hashnode.dev/

https://medium.com/@azizulmaqsud

https://twitter.com/Sohail2me

https://github.com/azizulmaqsud
