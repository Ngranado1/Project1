## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

C:\Users\ngran\Documents\GitPP

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

install-elk.yml_

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly _efficient____, in addition to restricting _traffic____ to the network.
- 

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the __metrics___ and system __logs___.
- Log files.
- Records metric from specific OS, & stores them to your desired folder.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| Web1     |     VM   | 10.0.0.11  | Linux            |
| Web2     |     VM   | 10.0.0.12  | Linux            |
| Web3     |     VM   | 10.0.0.10  | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the __jump box___ machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 10.0.0.10 - 10.0.0.11 - 10.0.0.12

Machines within the network can only be accessed by __whitelisted IPs___.
- Ansible VM - 10.1.0.4

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes/No              | 10.0.0.1 10.0.0.2    |
|          |                     |                      |
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- Efficiency, & any errors that occur will be listed.

The playbook implements the following tasks:
- Installs filebeat, enables docker
- Installs metricbeat, enables docker
- Configures elk using prewritten conf. file

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

- C:\Users\ngran\OneDrive\Desktop\Lightshot Screenshots

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- 10.0.0.10 - 10.0.0.11 - 10.0.0.12

We have installed the following Beats on these machines:
- Filebeats & metricbeats

These Beats allow us to collect the following information from each machine:
- The beats allow us to collect data from logs, as well as metrics from any OS system across our VM.

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- myfirstplaybook.yml
- enter the private IPs of the servers you want it installed on
- Elk server's public IP:5601/app/kibana

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
