<h1>On-Premise to Cloud Data Migration Project</h1>

<h2>Description</h2>
This project revolves around executing a seamless migration of data from on-premise servers to the cloud, employing Amazon Web Services (AWS) cloud services and principles of Infrastructure as Code (IaC). By implementing robust infrastructure management techniques, the goal is to ensure secure, scalable, and efficient data transfer while minimizing downtime and maximizing resource utilization.
<br />


<h2>Language and Libraries Used</h2>

- <b>Bash Scripting</b> 


<h2>Environments/Cloud Services Used </h2>

- <b>RDP Client</b>
- <b>SSH Client</b>
- <b>AWS CloudFormation</b>
- <b>AWS IAM</b>
- <b>AWS CloudFormation</b>
- <b>AWS Storage Gateway</b>
- <b>Amazon CloudWatch</b>
- <b>Amazon EC2</b>
- <b>Amazon S3</b>
- <b>Amazon VPC</b>


<h2>Project Workflow:</h2>


- **Establishing Prerequisites:**
  - Configured AWS account with Admin privileges
  - Generated a new key pair for secure access
- **Provisioning Infrastructure with CloudFormation:**
  - Developed YAML-based CloudFormation templates for VPC, Windows instance, and Linux instance
  - Launched the VPC stack with specific parameters
  - Launched the Windows and Linux instance stacks
- **Setting Up a File Gateway:**
  - Established connectivity with the on-premise Windows instance using RDP
  - Created an S3-backed file gateway
  - Configured and deployed an AWS File Gateway
- **Configuring and Mounting the NFS File Share:**
  - Created an NFS-based file share associated with the file gateway
  - Connected to the Linux instance via SSH from the Windows instance
  - Mounted the NFS file share on the Linux instance
- **Configuring Alarm Triggers with CloudWatch:**
  - Configured a CloudWatch alarm for data transfer thresholds
  - Set up email notifications using Amazon SNS
  - Tested the alarm by transferring data to the mounted NFS file share
- **Testing Your System:**
  - Successfully transferred data to the NFS file share
  - Validated the data transfer by inspecting files on the NFS mount
