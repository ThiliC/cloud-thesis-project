# Task 1: Networking

## Description.

This CloudFormation stack creates the base network infrastructure for the Weather based Solar Foreacasting Application. 
This includes, 
 - 1 VPC (10.25.60.0/22)
 - 2 Public subnets
 - 2 Private subnets
 - 1 Internet Gateway
 - 1 Public route table with a default route to the IGW.  

 ## Architecture Components.
  - VPC: WeatherVPC
  - Subnets: 2 Public (AZ1,AZ2), 2 Private (AZ1, AZ2)
  - Route Table: PublicRouteTable
  - Internet Gateway: WeatherIGW

  ## How to Deploy using AWS Console.

  1. Go to **AWS Console** &rarr; **CloudFormation**
  2. **Create stack** &rarr;**with new resources (standard)**
  3. Uploaded *my template.yaml* file
  4. Set stack name: *cloudporject-networking*
  5. Review and **create stack**

  ### Check my output!!

  ![CloudFormation](/task1-networking/Images/CloudFormation_networking_stack.jpg)

  ![MyVPC](/task1-networking/Images/MyVPC.jpg)

  ![WeatherVPC](/task1-networking/Images/WeatherVPC.jpg)

  *Default VPC also created automatically.*











[def]: i