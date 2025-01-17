### Prerequisites:

Before running the script, ensure the following:

1. **AWS CLI Configuration**:
   - Install the AWS Command Line Interface (CLI) on your system. You can download it from the official AWS site: [AWS CLI Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).
   
2. **Configure AWS CLI**:
   - After installing the AWS CLI, configure it by running the following command:
     aws configure
     
   - You will be prompted to enter your AWS credentials:
     - **AWS Access Key ID**: Your access key from the AWS IAM user.
     - **AWS Secret Access Key**: Your secret key associated with the access key.
     - **Default region name**: The AWS region where your resources are hosted (e.g., `us-east-1`).
     - **Default output format**: You can choose `json`, `text`, or `table`.

3. **Install jq (for JSON parsing)**:
   - This script uses `jq` to parse and format JSON output from AWS CLI commands. Make sure `jq` is installed on your system. You can install it via your package manager:
     - **For macOS**: `brew install jq`
     - **For Ubuntu**: `sudo apt-get install jq`
     - **For Windows**: Download from the official site [jq Download](https://stedolan.github.io/jq/download/).

Once the AWS CLI is configured and `jq` is installed, you’re ready to run the script.

