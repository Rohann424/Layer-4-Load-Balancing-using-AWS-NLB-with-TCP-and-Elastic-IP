# Layer-4-Load-Balancing-using-AWS-NLB-with-TCP-and-Elastic-IP

Step 1 : 

Created a **custom VPC** with **CIDR block 10.0.0.0/16** to **isolate** and **manage networking** for the **load balancing setup**.


![Project Screenshot](screenshots/step7-nat-gateway.png)

Step 2 :

Created **two** **public subnets** across **different availability zones** to ensure **high availability** and **fault tolerance**.

![Project Screenshot](screenshots/step7-nat-gateway.png)

Step 3 :

Created and attached an **Internet Gateway** to **enable** **internet connectivity** for resources inside the VPC.

![Project Screenshot](screenshots/step7-nat-gateway.png)

Step 4 :

Configured **route table** to allow **internet traffic** through the **Internet Gateway**.

![Project Screenshot](screenshots/step7-nat-gateway.png)

Step 5 :

Configured **security group** to allow **HTTP** and **SSH** access to EC2 instances.

![Project Screenshot](screenshots/step7-nat-gateway.png)

Step 6 :

Launched **two EC2 instances** in **separate subnets** to act as **backend servers**.

- Instance / Server 1 :
  
![Project Screenshot](screenshots/step7-nat-gateway.png)

- Instance / Server 2 :

![Project Screenshot](screenshots/step7-nat-gateway.png)

Step 7 :

Installed **Apache web server** to handle **incoming TCP requests**.

Configured **unique responses** on **each server** to **validate load balancing**.

- Server 1 :
  
![Project Screenshot](screenshots/step7-nat-gateway.png)

- Server 2 :

 ![Project Screenshot](screenshots/step7-nat-gateway.png)

Step 8 :

Created **TCP-based target group** to **route traffic to EC2 instances**.


Registered **EC2 instances** into **target group**.

![Project Screenshot](screenshots/step7-nat-gateway.png)






