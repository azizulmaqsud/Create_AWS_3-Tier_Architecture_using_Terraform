# Create_AWS_3-tier_Architecture_using_Terraform

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


## Thank You!
# Stay Connected !!

https://www.youtube.com/channel/UCNwP7KEElaJ7cdDTLP-KbBg

https://www.linkedin.com/in/azizul-maqsud/

https://azizulmaqsud-1684501031000.hashnode.dev/

https://medium.com/@azizulmaqsud

https://twitter.com/Sohail2me

https://github.com/azizulmaqsud


<a href="https://www.buymeacoffee.com/azizulmaqsud"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee&emoji=&slug=scaleupsaas&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff" /></a>
