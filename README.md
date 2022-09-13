# cloud-formation-volumes
* Creating and attaching custom EBS volumes to an EC2 instance.
* The resource VolumeMount creates a 10GB gp2 EBS volume.
*  This resource is referenced under Volumes and is mounted to /dev/sdf.

# Params

* Device - The mount point on the instance
* VolumeId - The id of the volume resource
* Size - The size of the volume, in GiBs
* VolumeType: The volume type, General Purpose SSD: gp2 | gp3


Resources        | AWS Docs
-------------    | -------------
EC2              | https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html
volumes          | https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html
VolumeAttachment | https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volumeattachment.html

# Design Template

Basic Mount Template
<img width="880" alt="Screenshot 2022-09-12 at 17 42 59" src="https://user-images.githubusercontent.com/67050571/189697631-b1adb0e7-ff34-4b3e-87ac-8721176e9dee.png">

Mount template with SSH

<img width="412" alt="Screenshot 2022-09-13 at 09 03 33" src="https://user-images.githubusercontent.com/67050571/189833021-d531fcba-05bf-4a24-ae02-ed5a5b897af1.png">
