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
     
*Custom configuration, can specify parameters*

     1. Operating system
     2. Size of persistent storage
     3. Adding GPUs for intensive operations such as machine learning
     4. Making the VM preemptible
     
     
*There are 3 storage options for the VM instances*

     1. Persistent Disk : block-oriented systems. Build data persistence when VMs start, stop, or terminate
     2. FileStore : Managed storage option provides network storage
     3. Local SSD : Attached to VM instance server physically. High throughput, low latency, data persists until the instance stops
     4. Cloud Storage : Object based 
 
**Kubernetes Engine**

- Caas
- Run containerized applications on a cluster of servers
- Containers are comparable to VMs in regards to computing processes and resources 
- No need for hypervisor as the *Host Operating System* maintains isolation using a container manager
- Easy to add/remove resources from a Kubernetes cluster using a GUI or CLI
- Monitors health, automatically repairs problems amd autoscales applications on load

**App Engine**

- Paas
- No need to concern with configuration, create applications in any popular language
- deploy to a serverless environment (Serverless product)
- There are 2 available environments. Standard and flexible.

*Standard Configuration*

     1. When applications need to deal with rapid scaling
     2. Source code is writing in **specific version** of supporting programming languages
     3. Need to run at a low cost/free
     4. Experiences sudden/extreme spikes in traffic
     5. No need for software that would have to be installed along with the application code.
     
*Flexible Configuration*

     1. Source code is writing in version of supporting programming languages
     2. Runs in a docker container
     3. Depends on frameworks that include native code
     4. Access resources/services that reside in the Compute Engine Network
     5. Need for software that would have to be installed along with the application code.
     6. work with background processes and write to local disk.
         
         
**Cloud Functions**

- Light weight computing option good for event-driven processing
- Runs code in response to events 
- Code run in cloud functions need to be short running 
- ** This service is not suited for long running code**
- Call other services APIs and other GCP Services
- Serverless product
- No configurations required, this service autoscales on load.



*What is the differnce between a VM and a Container*
- Containers virtualze an OS so that multiple workloads run on 1 OS instance
- VM virtualize the hardware to run multiple OS instances
- Containers are ligher and more portable that VMs 

*What is a VM*
- VM stands for Virtual Machine
- They emulate physical servers. Providing CPU, storage, RAM etc
- They run within a hypervisor

*What is a hypervisor*
- Is the emulator that creates and run virtual machines 
- Can be software, hardware or firmware
- Sits between the virtual machine and the hardware
- A computer that where a hypervisor runs a 1 virtual machine or more is called the host machine and each VM that it runs is called a guest machine that are isolated from eachother

*What is KVM*
- KVM stands for kernel virtual machine and provides virtualization on Linux systems

*Why does GCP use the KVM hypervisor -- possible reasons*
- open source
- Cross Platform compatibilty
- High performance

