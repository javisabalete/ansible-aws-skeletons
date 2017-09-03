# ansible-aws-skeletons
A group of skeletons to manage AWS via ansible playbooks.

## Usage

All playbooks require export AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY before execute.

### Available Playbooks
* ec2-sg: A skeleton to create, list and terminate EC2 instances and Security Groups.

        ```
        ansible-playbook -i hosts/local playbooks/ec2-sg.yml --tags create
        ansible-playbook -i hosts/local playbooks/ec2-sg.yml --tags list
        ansible-playbook -i hosts/local playbooks/ec2-sg.yml --tags terminate --extra-vars "instances=i-XXXXXXXXXXXXXXXXX"
        ansible-playbook -i hosts/local playbooks/ec2-sg.yml --tags create-group
        ansible-playbook -i hosts/local playbooks/ec2-sg.yml --tags list-groups
        ansible-playbook -i hosts/local playbooks/ec2-sg.yml --tags delete-group
        ```

        Extra vars are available to override default vars. See var_ec2-sg for possible extra vars.

### Available Hosts Files
* local: Hostfile for local_action

