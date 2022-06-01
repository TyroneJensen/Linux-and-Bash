# SSH connection for AWS cloud9 to github

launch aws cloud9

create a .ssh folder:

- mkdir home/ec2user/.ssh
- cd home/ec2user/.ssh

create key:

- ssh-keygen -t rsa

copy public key:

- /home/username/.ssh/id_rsa.pub

github profile / settings / SSH and GPG keys / new SSH key / paste copied public key

git clone repo

# Using SSH to Connect local env to Remote Server in AWS Cloud

launch aws cloud9

find cloud9 ec2 instance, go to security, edit inbound rules, add new SSH rule

get public IP of instance, add to variable

- export HOST="54.89.238.83"
- echo $HOST

go to .ssh directory and copy public key OR create a key and copy public key:

- ssh-keygen -t rsa

in aws cloud9 paste key to ~/.ssh/authorized_keys:

- nano ~/.ssh/authorized_keys

in local terminal, .ssh directory:

- echo $HOST
- ssh -v ec2-user@54.89.238.83

# Port forwarding

- ssh -N -L 8080:127.0.0.1:8080 ec2-user@54.89.238.83 (127.0.0.1 is your local ip)
