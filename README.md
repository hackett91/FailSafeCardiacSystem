# FailSafeCardiacSystem

login to AWS
ssh
Open an SSH client. (find out how to connect using PuTTY)
Locate your private key file (ssh.pem). The wizard automatically detects the key you used to launch the instance.
Your key must not be publicly viewable for SSH to work. Use this command if needed:
chmod 400 ssh.pem
Connect to your instance using its Public DNS:
ec2-63-34-8-221.eu-west-1.compute.amazonaws.com
Example:
ssh -i "ssh.pem" ec2-user@ec2-63-34-8-221.eu-west-1.compute.amazonaws.com


ainsible depends on python and boto3 needs to used to comunicate with AWS
pip install boto boto3

After creating the IAM account, we’ll need to store the AWS keys. Since they are sensitive data, we should use Ansible vault for this:

ansible-vault create aws_keys.yml
Once open, add the following to it:

aws_access_key: AKIAJLHNMCBOITV643UA
aws_secret_key: iMcMw4TB7cv9k+bdLqMGHKSTQIsZD43RVuSKFnU

switch user linux
sudo -i -u kafka

influxdb and grafna dashboards
