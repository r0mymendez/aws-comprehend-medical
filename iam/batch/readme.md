## AWS Comprehend Medical

This project uses AWS Comprehend Medical to analyze medical notes and extract relevant medical entities. To run the process in batch mode, the service must assume a role with the appropriate permissions. Below are the steps to configure the necessary policies and roles.

### Create the IAM Role
First, you need to create an IAM role that AWS Comprehend Medical can assume. This role should have the following policies:

- **policy.json**: Includes permissions to read and write to the S3 bucket where the notes to be processed are stored.
- **ComprehendDataAccessRolePolicy**: Allows AWS Comprehend Medical to assume the role with the necessary permissions.

### Trust Policy
Create a trust policy that allows AWS Comprehend Medical to assume the role. Refer to the `policy_trust_policy.json` file for specific details.