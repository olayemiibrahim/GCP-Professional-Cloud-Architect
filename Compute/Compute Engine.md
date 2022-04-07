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

## Machine Type

A **machine type** is a set of virtualized hardware resources that include your system memory size, virtual CPU (vCPU) count, and persistent disk limits for your VM instances.

**General Purpose Machine Types**

-   Best price-to-performance ratio for most workloads
-   Four families: E2, N2, N2D, and N1
    -   E2:
        -   Day-to-day computing at a low cost.
        -   Typically for serving web applications, small to medium sized databases, microservices, virtual desktops, and dev enviroments
    -   N2, N2D, N1:
        -   Offer a balanced price-to-performance ratio.
        -   Typically used for web applications, backend applications, medium-sized to large databases, caching, and media/streaming

**Memory Optimized Machine Types**
