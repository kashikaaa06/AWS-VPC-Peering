# EWB VPC Peering Project Report

**Name:** [Kashika Ghosh]
**Region:** Europe (Stockholm) / eu-north-1

## 1. Architecture and IP Plan
* **VPC A:** `10.10.0.0/16`
* **VPC B:** `10.20.0.0/16`
* **Design:** Non-overlapping CIDRs to allow VPC Peering.

![Architecture Diagram](images/00-architecture.png)
![Subnets](images/01-subnets.png)

## 2. Resource Inventory
* **Bastion:** `10.10.1.10` (Public IP enabled)
* **App-A:** `10.10.2.10` (No Public IP)
* **App-B:** `10.20.1.10` (No Public IP)

## 3. Route Table Configurations
![Public Route Table](images/02-route-table-public.png)
![Private Route Table A](images/03-route-table-a-private.png)
![Private Route Table B](images/04-route-table-b-private.png)

## 4. VPC Peering Connection
![Peering Connection](images/05-peering-active.png)

## 5. Security Groups
![Bastion SG](images/06-sg-bastion.png)
![App A SG](images/07-sg-app-a.png)
![App B SG](images/08-sg-app-b.png)

## 6. Verification and Testing Evidence

### Test 1: Forward Path (App-A to App-B)
![Ping Success](images/09-ping-success.png)

### Test 2: Controlled Failure
![Controlled Failure](images/10-controlled-failure.png)

### Test 3: Reverse Path (App-B to App-A)
![Reverse Ping](images/11-reverse-ping.png)

## 7. Conclusion
The project successfully demonstrated how to build a secure, multi-VPC architecture using AWS VPC Peering. By utilizing a Bastion host and strict Security Group rules, the private workloads were able to communicate securely without being exposed to the public internet.