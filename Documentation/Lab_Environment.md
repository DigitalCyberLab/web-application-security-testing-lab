# Lab Environment

## Environment Overview

The Web Application Security Testing Lab uses a dedicated Ubuntu Server virtual machine hosted in Oracle VirtualBox.

OWASP Juice Shop is deployed using Docker and accessed from the Mac host through an SSH tunnel.

## Virtual Machine Configuration

| Component | Configuration |
|---|---|
| Virtualization | Oracle VirtualBox |
| Operating System | Ubuntu Server 26.04.1 LTS |
| VM Name | WebSecurity-Lab |
| Memory | 2 GB |
| CPU | 1 Core |
| Virtual Disk | 25 GB |
| Network Adapter | NAT |

## Application Deployment

OWASP Juice Shop is deployed as a Docker container using the official image:

`bkimminich/juice-shop`

The application runs on port 3000 inside the Ubuntu virtual machine.

## Access Configuration

The application is accessed locally from the Mac host through SSH local port forwarding.

Browser address:

`http://127.0.0.1:3000`

The SSH tunnel forwards traffic from the Mac to the Ubuntu virtual machine.

## Security Considerations

- The lab uses an intentionally vulnerable application for educational testing.
- The application is hosted in a dedicated VirtualBox virtual machine.
- Access is restricted to the local Mac through SSH port forwarding.
- Testing is limited to the authorized lab environment.
