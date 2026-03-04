Hi Muhammad,

Appreciate the follow-up. Here's where things stand:

The original request came in without several details we needed on our side — subscription, tagging info, access requirements, and the App Registration details. We worked through gathering all of that with your team and ours.

On our end, the process involves requesting a new repo (handled by a separate team) and a dedicated TFE workspace, then writing Terraform code for the workspace setup which goes through review and approval before deployment. Once the workspace is deployed, I build out the actual infrastructure code — referencing our existing Key Vault module and adding the certificate generation and role assignments on top of it — which goes through another round of review and approval before it gets deployed.

The repo and workspace are in place, and I'm actively working on the infrastructure code. I'll provide an update once things are submitted for review.

Best regards




Create Azure Key Vault for Netskope Teams API Data Protection
Key details
Description
Create an Azure Key Vault with a self-signed certificate and role assignment for the Netskope Microsoft 365 Teams Next Generation API Data Protection integration. This supports SCTASK3364895.
Key Requirements:

Create TFE workspace (CSPMProd-Netskope) in the HCP-Terraform-Workspaces repo
Reference existing key_vault module from TFE registry to create Key Vault
Reference existing resource_group module from TFE registry to create Resource Group
Add azurerm_key_vault_certificate resource to generate self-signed certificate in Key Vault
Add azurerm_role_assignment resource to assign Key Vault Certificate User role to the Netskope App Registration
Output Vault URI, Certificate Name, Certificate Thumbprint, and Private Key (sensitive) for the requester
Key Vault settings per Netskope documentation: RBAC authorization, public access enabled, soft delete 90 days, purge protection disabled

Acceptance Criteria

terraform validate passes
terraform plan shows Key Vault, certificate, and role assignment resources
Vault URI, Certificate Name, Certificate Thumbprint, and Private Key are available as outputs
Private Key output is marked sensitive
Tags follow enterprise standards (owner: cissoc@websterbank.com, appid: app-4968)

Definition of Done (DOD)

Workspace created and deployed
Key Vault created using existing module
Self-signed certificate generated in Key Vault
Role assignment configured for App Registration
Outputs shared with requester team
Documentation updated

Key Contact
Muhammad Azam (CIS Engineering)

Want me to adjust anything?
