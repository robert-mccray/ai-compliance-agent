# ai-compliance-agent
This system reads heavy compliance documents (like SOC2 requirements) and directly compares them to your infrastructure code (like Terraform). It uses an LLM to identify gaps, such as a contract requiring TLS 1.2 while your Terraform code allows TLS 1.0.
