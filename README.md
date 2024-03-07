# SSM-Agent-Raspberry-Pi
AWS SSM Agent Raspberry Pi Installation arm architecture
```
AWS SSM Agent Raspberry Pi Installation
# Login to your server via SSH and run the following commans, entering the code, id and region values
mkdir /tmp/ssm
# Change depending on architecture
# sudo curl https://s3.amazonaws.com/ec2-downloads-windows/SSMAgent/latest/debian_arm/amazon-ssm-agent.deb -o /tmp/ssm/amazon-ssm-agent.deb
sudo curl https://s3.us-east-2.amazonaws.com/amazon-ssm-us-east-2/latest/debian_arm64/amazon-ssm-agent.deb -o /tmp/ssm/amazon-ssm-agent.deb
sudo dpkg -i /tmp/ssm/amazon-ssm-agent.deb
sudo service amazon-ssm-agent stop
sudo amazon-ssm-agent -register -code "activation-code" -id "activation-id" -region "region" 
sudo service amazon-ssm-agent start
```
