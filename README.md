# IaC

## 1. Initialize the resource using Terraform
![image](https://github.com/khkwon01/IaC/assets/8789421/41bf7fb4-b2f8-4589-a2b5-27dcf48be56d)
- Write a Terraform configuration that defines the infrastructure you want to create.
- Review the Terraform plan to ensure that the configuration will result in the expected state and infrastructure.
- Apply the configuration to create your Terraform state and infrastructure.

  ### 1.1 move state file from default to another path
  ```
  terraform {
    backend "local" {
      path = "terraform/state/terraform.tfstate"
    }
  }

  terraform init -migrate-state
  ```


## 2. Import terraform configuaration from resources made using other tools
![image](https://github.com/khkwon01/IaC/assets/8789421/b7b34db9-89fd-461e-9161-9f2c4fc9e620)
- Identify the existing infrastructure to be imported.
- Import the infrastructure into your Terraform state.
- Write a Terraform configuration that matches that infrastructure.
- Review the Terraform plan to ensure that the configuration matches the expected state and infrastructure.
- Apply the configuration to update your Terraform state.
- Importing Tools(don't supported by hashicorp) : https://github.com/GoogleCloudPlatform/terraformer
