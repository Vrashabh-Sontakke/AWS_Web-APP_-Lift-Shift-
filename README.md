# AWS_Web-APP_-Lift-Shift-
Shifting a Java web app from local environment to AWS cloud

## Project Architecture :
![Project Architecture](https://user-images.githubusercontent.com/86019029/212285310-fe98057d-231a-4883-8426-92e222a6b149.png)

## Flow of Execution :
1. LOGIN INTO AWS CONSOLE
2. CREATE KEY PAIRS AND SAVE THE CREDENTIALS
3. CREATE 3 SECURITY GROUPS:
- Tomact EC2 instance
- Backend EC2 instance(memcache,rabbitmq,Mysql)
- Load Balancer
4. Launch instance with user data from bash scripts
5. Update IP to name mapping in Route 53
6. Building app from source code
7. Upoadling artifacts to S3 bucket
8. Download artifacts to Tomact EC2 instance
9. Setup ELB with HTTPS (with certificates from AMAZON CERTIFICATE MANAGER)
10. Mapping ELB endpoints to website name in Godaddy DNS
11. Buildauto Scaling Group for Tomcat instace
