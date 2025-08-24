Readme file for Github_users_with_access_list script

# GitHub Repository Collaborators Script

This repository contains a Bash script that lists all users who have **read access** to a specified GitHub repository within an organization.

---

## Features
- Fetches collaborators with read (`pull`) access for a given repository.
- Uses the GitHub API for authentication and data retrieval.
- Validates command-line arguments for proper usage.
- Displays meaningful error messages for ease of use.

---

## Prerequisites

Before running the script, ensure the following:

1. **Bash Shell**: Use a Linux/Unix environment or [WSL](https://learn.microsoft.com/en-us/windows/wsl/) on Windows.
2. **`jq` Installed**: This script uses `jq` for JSON parsing. Install it using:
   ```bash
   sudo apt-get install jq  # For Ubuntu/Debian
   brew install jq          # For macOS

GitHub Personal Access Token:
Go to your GitHub account: Settings > Developer Settings > Personal Access Tokens > Tokens (classic).
Generate a token with the following scope:
repo
Save the token securely.

1. Clone the Repository
Clone this repository to your local machine:
bash
git clone <repository-url>
cd <repository-directory>

2. Export Credentials
Export your GitHub username and personal access token as environment variables:
bash
export username="your-username"
export token="your-personal-access-token"

3. Make the Script Executable
Give execute permissions to the script:
bash
chmod +x list-users.sh

4. Run the Script
Execute the script with the required arguments:
bash
./list-users.sh <REPO_OWNER> <REPO_NAME>
REPO_OWNER: The owner of the repository (e.g., organization name).
REPO_NAME: The name of the repository.

Example:
bash
./list-users.sh my-org my-repo
Example Output
If users with read access are found:
Users with read access to my-org/my-repo:
user1
user2
user3

If no users have read access:
bash
No users with read access found for my-org/my-repo.
If there’s an error (e.g., invalid token or repository):
