# Layer-4-Load-Balancing-using-AWS-NLB-with-TCP-and-Elastic-IP

**PROJECT OBJECTIVE :**

The objective of this project is to **design** and **implement** a **highly available** and **fault-tolerant** architecture using **AWS Network Load Balancer (NLB)** to distribute **TCP traffic** across **multiple EC2 instances** while ensuring a **static entry point using Elastic IP**.



















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

Step 9 :

Created **Network Load Balancer** to **distribute TCP traffic** across **servers**.

Assigned **Elastic IP** to provide **static entry point** for the application.

Connected **target group** to **load balancer**.

![Project Screenshot](screenshots/step7-nat-gateway.png)

Step 10 :

Verified **load balancing** by **accessing application** through **NLB DNS**.

![Project Screenshot](screenshots/step7-nat-gateway.png)

Step 11 :

Simulated **backend failure** by **stopping** the **web server** **(Server2)** on one EC2 instance. 

Observed that the **Network Load Balancer automatically** routed all incoming traffic to the **remaining healthy instance**, demonstrating **fault tolerance** and **high availability**.

- Server 2 (Stopped) :

![Project Screenshot](screenshots/step7-nat-gateway.png)

- Verified the traffic flow :

![Project Screenshot](screenshots/step7-nat-gateway.png)






