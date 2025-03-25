# Starting Ansible on Windows

```
wsl --install
sudo apt update
sudo apt install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt update
sudo apt install ansible -y
```

# Running Ansible in WSL connecting to AWS
As you connect to an EC2 Instance by SSH, I created a new key pair named "aws_ec2_ed25519.pem".
Connecting in a Linux Environment via SSH requires resticted access to the key.
You can archieve this by running `chmod 400 FILE_NAME`, but you cannot alter windows permissions.

Solution: Copy the key to the WSL environment: `cp /mnt/c/Users/jonas.hoerl/.ssh/aws_ec2_ed25519.pem`
and set proper permissions: `chmod 400 ~/.ssh/aws_ec2_ed25519.pem`

Lastly the host file needs to be adjusted.