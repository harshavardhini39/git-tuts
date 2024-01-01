# Infrastructure as Code (IaC) with Terraform

## Step-01: Understand Problems with Traditional way of Managing Infrastructure
- Time it takes for building multiple environments
- Issues we face with different environments
- Scale-Up and Scale-Down On-Demand

---

## Step-02: Discuss how IaC with Terraform Solves them
- Visibility
- Stability
- Scalability
- Security
- Audit

### Step-02-1: Introduction
- Understand basic Terraform Commands
  - `terraform init`
  - `terraform validate`
  - `terraform plan`
  - `terraform apply`
  - `terraform destroy`

### Step-02-2: In versions.tf
```hcl
<!-- Copy Button -->
<button class="copy-button" onclick="copyToClipboard('versionsTfCode')">Copy Code</button>

<!-- Code Block -->
<pre id="versionsTfCode"><code>
# Terraform Settings Block
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
    }
  }
}

# Provider Block
provider "aws" {
  profile = "default" # AWS Credentials Profile configured on your local desktop terminal $HOME/.aws/credentials
  region  = "us-east-1"
}
</code></pre>

<script>
// Copy to Clipboard Function
function copyToClipboard(id) {
    var copyText = document.getElementById(id);
    var textArea = document.createElement("textarea");
    textArea.value = copyText.textContent;
    document.body.appendChild(textArea);
    textArea.select();
    document.execCommand('copy');
    document.body.removeChild(textArea);
    alert("Code Copied!");
}
</script>
