# Network Security Lab Project - Chandana

## Project Overview

This project is a comprehensive network security lab simulation created using GNS3 (Graphical Network Simulator 3). The lab is designed for educational purposes to demonstrate network security concepts, firewall configurations, and network segmentation.

## Author
**Chandan Mariyada**

## Project Structure

```
Chandana/
├── Chandana.gns3                           # Main GNS3 project file
├── document network security.pdf           # Project documentation
├── step 2 document network security.pdf   # Additional documentation
├── project-files/                         # GNS3 project assets
│   ├── images/                            # VM disk images
│   ├── virtualbox/                        # VirtualBox VM files
│   │   ├── 0b80d915-7a54-46c4-a3ce-3c800208683b/  # Windows LAN VM
│   │   ├── 0eed372f-ac78-4513-a9d8-817d0cc6efd9/  # pfSense Firewall VM
│   │   ├── 19f3530b-e356-4349-aac4-3c920af8bdd8/  # Ubuntu DMZ VM
│   │   └── f9dcb7f5-f3e5-4277-9503-a7d40e0140af/  # Kali Linux VM
│   └── vmware/                            # VMware specific files
└── README.md                              # This file
```

## Network Topology

The lab consists of the following network components:

### Virtual Machines
1. **pfSense Firewall/Router** (`pfsense1.2`)
   - Main firewall and router for the network
   - 3 network adapters
   - 5852 MB RAM
   - Acts as the central security gateway

2. **Windows LAN Client** (`windows010`)
   - Windows 10 machine in LAN segment
   - 1 network adapter
   - 6039 MB RAM
   - Represents typical corporate workstation

3. **Ubuntu DMZ Server** (`Ubuntu24.1`)
   - Ubuntu 24.x server in DMZ segment
   - 1 network adapter
   - 4096 MB RAM
   - Hosts public services

4. **Kali Linux** (`kali-linux-2025.3`)
   - Security testing and penetration testing platform
   - 1 network adapter
   - 2048 MB RAM
   - Used for security assessments

### Network Infrastructure
- **vSwitch**: OpenVSwitch-based virtual switch
- **Internet Cloud**: Simulated internet connection
- **Multiple Network Segments**: LAN, DMZ, and WAN configurations

### Network Connections
- **WAN**: Connection to Internet through pfSense
- **LAN**: Internal network with Windows and Kali machines
- **DMZ**: Demilitarized zone with Ubuntu server
- **Management**: Administrative access to network devices

## Prerequisites

### Software Requirements
- **GNS3** (version 2.2.55 or later)
- **VirtualBox** (for running VMs)
- **Docker** (for network appliances)

### Hardware Requirements
- **RAM**: Minimum 16 GB (recommended 32 GB)
- **Storage**: At least 50 GB free space
- **CPU**: Multi-core processor with virtualization support
- **Network**: Internet connection for downloading images

## Setup Instructions

### 1. Install Required Software
```bash
# Install GNS3
# Download from: https://www.gns3.com/software/download

# Install VirtualBox
# Download from: https://www.virtualbox.org/

# Install Docker (for Linux-based appliances)
# Download from: https://www.docker.com/
```

### 2. Import the Project
1. Open GNS3
2. File → Open Project
3. Navigate to and select `Chandana.gns3`
4. Wait for all components to load

### 3. Configure VM Images
Ensure you have the following VM images:
- pfSense 2.8.0 or later
- Ubuntu Server 24.x
- Windows 10/11
- Kali Linux 2025.3

### 4. Start the Lab
1. Right-click on each VM and select "Start"
2. Allow VMs to fully boot before proceeding
3. Configure network interfaces as needed

## Lab Exercises

This network security lab supports various learning objectives:

### 1. Firewall Configuration
- Configure pfSense firewall rules
- Set up NAT and port forwarding
- Implement traffic filtering policies

### 2. Network Segmentation
- Understand LAN, DMZ, and WAN concepts
- Configure VLANs and subnets
- Implement security zones

### 3. Security Testing
- Use Kali Linux for penetration testing
- Perform vulnerability assessments
- Test firewall effectiveness

### 4. Network Monitoring
- Monitor network traffic
- Analyze security logs
- Implement intrusion detection

## Default Configurations

### Network Addressing (Typical)
- **WAN**: DHCP from Internet cloud
- **LAN**: 192.168.1.0/24
- **DMZ**: 192.168.2.0/24

### Default Credentials
- **pfSense**: admin/pfsense
- **Ubuntu**: ubuntu/ubuntu (may vary)
- **Windows**: Administrator/[custom password]
- **Kali**: kali/kali

## Troubleshooting

### Common Issues
1. **VMs won't start**: Check VirtualBox installation and VM paths
2. **Network connectivity issues**: Verify switch connections and IP configurations
3. **Performance problems**: Allocate sufficient RAM and CPU resources
4. **Missing images**: Download required VM images and place in correct directories

### Performance Optimization
- Close unnecessary applications
- Allocate adequate system resources
- Use SSD storage for better VM performance
- Disable unnecessary VM services

## Learning Objectives

Upon completion of this lab, students should understand:
- Network security fundamentals
- Firewall configuration and management
- Network segmentation strategies
- Penetration testing methodologies
- Security monitoring and incident response

## Documentation

Additional documentation is available in:
- `document network security.pdf` - Main project documentation
- `step 2 document network security.pdf` - Detailed implementation steps

## Support and Contributions

For questions or issues related to this project:
1. Check the troubleshooting section
2. Review the provided documentation
3. Consult GNS3 community forums
4. Contact the project author

## License

This project is created for educational purposes. Please ensure compliance with software licensing requirements for all VM images and software used.

## Version History

- **v1.0** - Initial network topology setup
- **Current** - Revision 9 with optimized configurations

---


**Note**: This lab environment is designed for educational and testing purposes only. Do not use in production environments without proper security review and hardening.
