# MODULE 1
# MODULE 2
# MODULE 3
# MODULE 4
# MODULE 5 STORAGE
- S3
- DynamoDB
- Redshift

# MODULE 6
- DoS and DDoS: Denial of Service and Distributed Denial of Service
- AWS Shield: protection against DoS
- Inspector: suggests
- GuardDuty: intelligent threat detection

### Questions:
- Q1. describe IAM policy: document
- Q2. needs temporary access to S3 bucket: grant IAM role.
- Q3. least privilege: granting only permission needed to perform specific tasks
- Q4. defend DoS: AWS Shield
- Q5. describe AWS KMS: create cryptographic keys (manage and provide keys)

# MODULE 7 Security
- Amazon CloudWatch: monitor resources 
- AWS CloudTrail: track activities,
- AWS Trusted Advisor dashboard: receive recommendations and improve our environment
- AWS Budget: create budget abd forecasts
- AWS Cost Explorer: visualize understand costs
- AWS Support Plans: basic support, 

### Questions:
- Q1. describe cloudwatch: monitor / metrics
- Q2. describe AWS Trusted Advisor: performance / fault tolerance
- Q3. lowest cost with all aws trusted advisor checks: business. (basic/developer/business/enterprise)

# MODULE 8
# MODULE 9
- AWS CAF Cloud Adoption Framework: 6 
  - business capabilities: (business, people, governance)
  - technical capabilities: (platform, security, operations)
- Six migration strategies:
  - Rehost/Relocate -- cloud -- lift & shift -- lift from on-prem and move on-cloud -- EC2
  - Replatform -- cloud -- lift & tinker -- RDS
  - Refactor/Rearchitect -- cloud -- time consuming and more effort 
  - Repurchase -- cloud -- move on-prem to cloud -- shutdown hardware and setup on salesforce
  - Retain
  - Retire
- AWS Snow Family
  - AWS Snowcone -- small, 8TB
  - AWS Snowball -- storage optimized 80TB / compute optimized 40TB
  - AWS Snowmobile
- 5 Pillars of AWS Well Architected
  - Operations excellence
  - Security
  - Cost optimisation
  -

- Notes:
    - factors to consider while selecting region: 
      1. compliance
      2. proximity
      3. services_available
      4. pricing
- Example:
    - client > package > internet > IG > NACL > VPC > SG > EC2
- NACL
    - stateless (do NOT remember, auth REQUIRED on return)
-  SG Security Groups
    - stateful (remembers, no auth on return)