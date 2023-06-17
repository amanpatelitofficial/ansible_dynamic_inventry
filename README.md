## ansible_dynamic_inventry

### To install some packages  -- install on local server 

 > Install ansible 

 > pip install boto
 
 > pip install boto3 
 
 #### To install aws ansible module 
 
 > ansible-galaxy collection install amazon.aws
 
 ### Now clone the GitHub repo in /home/aman/
 
 > git clone https://github.com/amanpatelitprofessional/ansible_dynamic_inventry.git

 > cd /ansible_dynamic_inventry/aws

 > chmod +x ec2.*

 ### Now create the IAM user with ec2 full access
 
 
 ### Now edit the file ec2.py 
  
  > vim ec2.py
    line number 37 comment this line 
    line number 64 elasticache false
  
  ### Now edit the file ec2.ini & put the aws access key & secrit keys
  
  
  ### Now configure the ansible inventory file
  
  > vim /etc/ansible/ansible.cfg
  
   [defaults]
   inventory = /home/aman/aws/ec2.py
   
   ### Now execute the ./ec2.py
   > ./ec2.py
   
   ### Now lunch an ec2 verify the ansible hosts 
   
   > ansible all --list-hosts     -  by local server 
   
   
  
