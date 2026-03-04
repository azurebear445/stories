Hi Muhammad,

Appreciate the follow-up. Here's where things stand:

The original request came in without several details we needed on our side — subscription, tagging info, access requirements, and the App Registration details. We worked through gathering all of that with your team and ours.

On our end, the process involves requesting a new repo (handled by a separate team) and a dedicated TFE workspace, then writing Terraform code for the workspace setup which goes through review and approval before deployment. Once the workspace is deployed, I build out the actual infrastructure code — referencing our existing Key Vault module and adding the certificate generation and role assignments on top of it — which goes through another round of review and approval before it gets deployed.

The repo and workspace are in place, and I'm actively working on the infrastructure code. I'll provide an update once things are submitted for review.

Best regards
