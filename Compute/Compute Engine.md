# Google Cloud Compute Engine

Secure and customizable compute service that lets you create and run virtual machines on Google’s infrastructure.

[Official Documentation](https://cloud.google.com/compute)

Compute Engine is GCP's **IaaS** solution that enables users to launch virtual machines on demand.

## Virtual Machine Instances

An **instance** is a virtual machine hosted on Google's infrastructure.

When you create an instance you assign the following things:

-   Instance Name
-   Labels (Optional)
-   Region
-   Zone
-   Machine Configuration
-   Network

### Machine Type

A **machine type** is a set of virtualized hardware resources that include your system memory size, virtual CPU (vCPU) count, and persistent disk limits for your VM instances.

**General Purpose Machine Types**

-   Best **price-to-performance ratio** for most workloads
-   Four families: E2, N2, N2D, and N1
    -   E2:
        -   Day-to-day computing at a low cost.
        -   Typically for serving web applications, small to medium sized databases, microservices, virtual desktops, and dev enviroments
    -   N2, N2D, N1:
        -   Offer a balanced price-to-performance ratio.
        -   Typically used for web applications, backend applications, medium-sized to large databases, caching, and media/streaming

**Memory Optimized Machine Types**

-   Optimized for **memory**-intensive workloads, and offer more memory per core than other machine types **(up to 12TB of RAM)**.
-   Two families: M1 and M2
    -   M1 and M2:
        -   Optimized for **ultra-high-memory** workloads.
        -   For large in-memory databases such as SAP HANA, Redis, or in-memory analytics.

**Compute Optimized Machine Types**

-   Optimized for **compute-intensive** workloads, and offer more performance per core than other machine types.
-   Offer Intel Scalable processors and up to **3.8HGz** of sustained all core turbo.
-   One family: C2
    -   C2:
        -   Used for high-performance computing, gaming, and single-threaded applications that are CPU intensive.

**Shared-core Machine Types**

-   Optimized for **cost**, and share a physical core.
-   Used for running very small, non-resource intensive applications
-   Two families: N1 and E2
    -   N1:
        -   f1-micro and g1-small
        -   One vCPU available for short periods of bursting
    -   E2:
        -   e2-micro, e2-small, and e2-medium
        -   Two vCPUs available for short periods of bursting

**GPUs**

-   GPUs can also be added if workload is graphically intensive.
-   GCP offers NVIDIA Tesla GPUs

**Preemptible VMs or Spot VMs**

-   Fighly affordable compute instances suitable for batch jobs and fault-tolerant workloads.
-   Best used for batch workloads
-   Priced anywhere between a 60%-91% discount from a regular VM
-   May stop preemptible instances at any time due to system events.
-   Compute Engine WILL shut the VM down once it reaches 24 hours, however this timer can be reset by starting and stopping the VM
-   ^ is not the case for Spot VMs
-   No SLA

**Shielded VMs**

-   Security feature designed to offer a verifiable integrity of your VM to ensure VM's are not compromised by bootkits and rootkits
-   Designed for highly sensitive workloads and organizations with strict compliance requirements
-   Leverges Secure boot with virtual Trusted Platform model vTPM and integrity monitoring

**Confidential VMs**

-   Ensures that your data and applications stay private and encrypted even while in use.

**Sole-Tenant Nodes**

-   Allows physical hardware isolation for organizations that want to completely mitigate any risk of hackers exploiting the hardware to access other VM's on the server

### Images

**Public Images**

-   Provided or maintained by Google, the open source community, or third-party vendors
-   Various OS options such as RHEL, Debian Windows Server, CentOS, etc.,
-   Typically maintained through their life cycle

**Custom Images**

-   Boot disk images created by you/your organization, that you're responsible for maintaining, hardening, and controlling access to
