1- Wbat js EBS?

- Amazon Elastic Block Storage allows you to create storage volumes and attach them to Amazon EC2 Instances. Once attached, you can create a file system on top of these volumes, run a database, or use them in any other way you would use a block device. Amazon EBS volumes are placed in a specific Availability Zone, where they are automatically replicated to protect you from the failure of a single component.

2- EBS Volume Types

- SSD
    - General Purpose SSD (GP2)
        - General purpose, balances both price and performance.
        - Ratio of 3 IOPS per GB with up to 10.000 IOPS and the ability to burst uop to 3000 IOPS for extended periods of time for volumes at 3334 GiB and above.
    - Provisioned IOPS SSD (IO1)
        - Designed for I/O intensive applications such as large relational or NoSQL databases.
        - Use if you need more than 10.000 IOPS.
        - Can provision up to 20.000 IOPS per volumen.

- Magnetic
    - Thorughput Optimized HDD (ST1)
        - Big data
        - Data warehouses
        - Log processing
        - Cannot be a boot volume
    - Cold HDD (SC1)
        - Lowest Cost Storage for Infrequently accessed workloads
        - File Server
        - Cannot be a boot volume
    - Magnetic (Standard)
        - Lowerst cost per gigabyte of all EBS volume types that is bootable. Magnetic volumes are ideal for workloads where data is accessed infrequently, and applications where the lowest storage cost is important

- EBS vs. Instacne Store

- Instance Store Volumes are sometimes called Ephemeral Storage.
- Instance store volumes cannot be stopped. If the underlying host fails, you will lose your data.
- EBS backed instances can be stopped. You will not lose the data on this instance if it is stopped.
- You can reboot both, you will not lose your data.
- By default, both ROOT volumes will be deleted on termination. However, with EDS volumes, you can tell AWS to keep the root device volume.

- Encryption

- Create s Snapshot of the unencrypted root device volume
- Create a copy of the Snapshot and select the encrypt option
- Create an AMI from the encrypted Snapshot
- Use that AMI to launch new encrypted instances

