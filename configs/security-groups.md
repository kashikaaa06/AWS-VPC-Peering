# Security Groups

## ewb-sg-bastion
* Inbound: SSH (22) from My IP

## ewb-sg-app-a
* Inbound: SSH (22) from 10.10.1.10 (Bastion)
* Inbound: ICMP from 10.20.1.10 (App-B)

## ewb-sg-app-b
* Inbound: SSH (22) from 10.10.1.10 (Bastion)
* Inbound: ICMP from 10.10.2.10 (App-A)