# Task 2: Firewall (Security Groups)

## Description.

This stack creates 02 security groups for the Weather-based Solar Forecating App. 

- **PublicSecurityGroup** - Allows SSH, HTTP, HTTTPS from internet. 
- **PrivateSecurityGroup** - Allows access only from PublicSecurityGroup

## How to Deploy using AWS Console.

  1. Go to **AWS Console** &rarr; **CloudFormation** &rarr; Create Stack
  2. Upload "firewall-template.yaml"
  3. Enter **VPC ID** ftom task 1 Outputs.
  4. Review and Submit. 

## Verification

 - Go to **VPC** &rarr; **Security Groups**
 - Check inbound Rules for both security groups.

## Check my Output!!
 ![Firewall_Stack](/task2-firewall/Images/Firewall_stack.jpg)
 
 ![Security_Groups](/task2-firewall/Images/SecurityGroups.jpg)

 ![PrivateSG_InboundRules](/task2-firewall/Images/PrivateSG_InboundRule.jpg)

 ![PublicSG_InboundRules](/task2-firewall/Images/PublicSG_InboundRule.jpg)

 
