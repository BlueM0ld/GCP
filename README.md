# GCP
Collection of notes for GCP. Specifically for the google cloud associate exam

**What are the main differences between Compute Engine, Kubernetes Engine, App Engine and Cloud Functions?**

**Compute Engine** 
- Iaas
- Gives users the most amount of control; allows the creation of **VMs**, attachment of **storage** to make use of other GCP services
- GCP uses a KVM hypervisor
- Compute engine provides 2 ways for launching VMs; Pre- configured and Custom approach

*Pre-configured, uses templates to set up their **VM***

     1. Standard VM : Equal computional power and mermory
     2. High memory VM : Memory intensive tasks that require access to non-disk storage quickly
     3. High-CPU VM : Intensive computational workload
     4. Shared-core VM : VMs share a physical core, cost-effective for small applications that run low demanding resources
     5. Accelerator optimized machine types : High performance computing and machine learning
     
*There are 3 storage options for the VM instances*

     1. Persistent Disk : block-oriented systems. Build data persistence when VMs start, stop, or terminate
     2. FileStore : Managed storage option provides network storage
     3. Local SSD : Attached to VM instance server physically. High throughput, low latency, data persists until the instance stops
     4. Cloud Storage : Object based 
 
**Kubernetes Engine**

- Caas

**App Engine**

- Paas

**Cloud Functions**

*What is a VM*
- VM stands for Virtual Machine
- They emulate physical servers. Providing CPU, storage, RAM etc
- They run within a hypervisor

*What is a hypervisor*
- Is the emulator that creates and run virtual machines 
- Can be software, hardware or firmware
- A computer that where a hypervisor runs a 1 virtual machine or more is called the host machine and each VM that it runs is called a guest machine that are isolated from eachother

*What is KVM*
- KVM stands for kernel virtual machine and provides virtualization on Linux systems

*Why does GCP use the KVM hypervisor -- possible reasons*
- open source
- Cross Platform compatibilty
- High performance

