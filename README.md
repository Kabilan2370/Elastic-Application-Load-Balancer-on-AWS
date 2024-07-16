# Elastic-Application-Load-Balancer-on-AWS
Simple AWS Elastic Load Balancer project. How a ELB handle the different types of user request and allocate to EC2 machine..  

![Alt text](1.1.png)

1. Here, I created a 3 Ec2 machine with Amazon Linux for ELB process. Every Ec2 machine has different subnet....
   To run this application,our security group should be enable http (port 80).
   
       #! /bin/bash
       yum install -y
       yum install -y httpd
       systemctl start httpd
       systemctl enable htppd
       echo "<h2>Welcome to the sample Elb application $(hostname -f)</h2>" >
       var/www/index.html
2. Create a application load balancer....

    ![Alt text](list/1.png)

3. Be sure, 3 Ec2 machine should have different subnet.

   ![Alt text](list/6.png)

4. In the network mapping session, attach your VPC and subnet details.

   ![Alt text](list/7.png)

5. Attach a security group with enabled http port....

   ![Alt text](list/8.png)

6. Here,We have to assign and create target group which information about out ec2 machine...

   ![Alt text](list/9.png)

7. Attache your 3 Ec2 machine ,do not forget to click " Include as pending below " evenby mistake.

   ![Alt text](list/10.png)
   ![Alt text](list/11.png)

8. After create a target group then, attach at the listeners and routing option correctly.

   ![Alt text](list/12.png)
   ![Alt text](list/13.png)

9. The result of successfully create a Application ELB.It take some time to active...

    ![Alt text](list/14.png)
   ![Alt text](list/15.png)

10. Now ,using ELB DNS address try to access on browser.....

    ![Alt text](list/16.png)

    We can access our  3 type ec2 machine.......ELB distribute the user request to different machine.....

11. Finally delete a ELB ,target group and ec2 machine properly. Otherwise they will put a charge for your usage.

                                     Thank you........................
   


    



