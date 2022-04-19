# DD2482-Demo-Terraform
Repo for the DD2482 demo done in week 5 (Terraform with Jetbrains)

## Slides
Here is the link to the slides:  
https://docs.google.com/presentation/d/1QAi4fUww1lCSKpa1PNqtQRfNj-3Uge6wzx1O4wWyZb8/edit?usp=sharing

## Replicate the demo
### Requirements
You need:  
- a AWS account (with a set of keys so you can connect to it). A free one should be enough
- Terraform installed (downloadable at www.terraform.io) and having the path to it correctly set up
- Have a Intellij installed (if you want to do it as well with Intellij)

### Set up
- **Step 1 :** On your AWS account, on the EC2 window, in the keypair subwindow, you need to create a key pair (in pem format) and download it.
- **Step 2 :** In the main.tf, change the values in the provider field to your AWS key (not EC2)
- **Step 3 :** In the main.tf, change the values in the provisioner and then connection with the path to your EC2 key.
- **Step 4 :** With Intellij, install the first plugin for Terraform; then you can add to the run configurations the different terraform commands (apply and plan already exist by default)

### Run it
- You first need to tell terraform which provider it will need. You do that thanks to the `terraform init` commande. You can do it in the terminal or with the run config.
- You can see the expected changes to the state with `terraform plan`
- To actually perform them, you need to run `terraform apply` and confirm you want to apply the changes.
- It will then print the public ip of the server. You can then go to it and see what it does! (with http)
- Feel free to try things out and change them to see what they do! The Auto completion of the plugin and the documentation of the service/provider will be your friend for that. Just apply the changes and terraform will only perform the necessary actions to go from the previous state to the next.
- Don't forget to destroy it with `terraform destroy`

### Sources
The demo was largely inspired by the following video: https://www.youtube.com/watch?v=SLB_c_ayRMo  
It will explain more in detail the required steps, and why we do the infrastructure in the way we do.
We highly recommend watching it if you want to dig deeper into terraform

### Contact
Feel free to contact us at:  
gatien@kth.se or ddnadjar@kth.se
