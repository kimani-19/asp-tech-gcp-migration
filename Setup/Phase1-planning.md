Simple Migration Plan Document Demo for Asp Technologies

Current Infrastructure (On-prem / Physical Layer):
1 web Server ( Host company Website) - Frontend
1 Application Server (Runs backend logic)
1 Database Server (MyDQL Database)
Local network (no cloud)

Target Architecture (GCP) along with services that will be used:
Compute engine VM - Web+APP server
Cloud SQL - Managed database
VPC Network - secure networking
Firewall rules - control traffic
Cloud load balancer - traffic distribution
Cloud monitoring and logging - observability

Architecture in working users on the internet then the load balance then the compute engine VM then the cloud SQL DB. Then inside you have a VPC Network which has the subnet(Public) and firewall rules.

Migration Strategy: lift and shift
Move app as is to cloud VM
Later improve architecture to (containers and scaling)

Basic Security Plan
Use IAM roles (least privilege)
Restrict SSH access
Only allow HTTP/HTTPS traffic
Database not publicly exposed

Cost Considerations
Use free tier eligible resources
Use small VM (e2 micro)
Stop resources when not in use
