---
nav_order: 2
section_id: Containers
title: Why containers?
---

### Standardized, portable packaging for your applications.

A standard package of software—known as a container—bundles an application’s code together with the related configuration files and libraries, and with the dependencies required for the app to run. This allows developers and IT pros to deploy applications seamlessly across environments.

#### Why you should care about containers?

The problem of an application failing to run correctly when moved from one environment to another is as old as software development itself.Containers address this problem by providing a lightweight, immutable infrastructure for application packaging and deployment. An application or service, its dependencies, and its configuration are packaged together as a container image. The containerized application can be tested as a unit and deployed as a container image instance to the host operating system.

This way, containers enable developers and IT professionals to deploy applications across environments with little or no modification.

#### Container vs. virtual machine

Virtual machines (VMs) virtualize hardware to run multiple OS instances. Each VM has its own OS and access to virtualized hardware resources. VMs allow running different OSes on the same server, efficient resource use, and fast server provisioning, but can be large.

Containers virtualize the OS, making the app believe it has exclusive access to CPU, memory, and storage. They can run anywhere with consistent base images, are lightweight, start quickly, and offer efficient resource utilization. Containers share the host OS, eliminating the need to boot an OS or load libraries, reducing maintenance overhead. However, containers are constrained to the OS they're defined for, e.g., a Linux container can't run on Windows.

#### Benefits

- **Agility**: Containerizing applications reduces deployment efforts, streamlines development and testing, and enhances collaboration between development and operations teams. This leads to faster app delivery.
- **Portability**: Containers offer a standardized format for packaging applications, ensuring they run consistently across different environments, including various operating systems and cloud platforms. This eliminates issues like "It works on my machine" and provides portability from development to production.
- **Rapid scalability**: Containers are more lightweight than virtual machines (VMs) because they don't require separate operating system instances. This allows for supporting many more containers on the same infrastructure. Containers can be started and stopped quickly, enabling rapid scalability up or down as needed.