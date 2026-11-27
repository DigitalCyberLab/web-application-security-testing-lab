# Lab Environment

## 1. Environment Overview

The Web Application Security Testing Lab uses a dedicated Ubuntu Server virtual machine hosted in Oracle VirtualBox.

OWASP Juice Shop is deployed inside the virtual machine using Docker. The application is accessed from the Mac host through an SSH local port forwarding tunnel.

OWASP ZAP runs on the Mac host and is used to perform web application security testing against the locally hosted Juice Shop application.

## 2. Virtual Machine Configuration

| Component | Configuration |
|---|---|
| Virtualization | Oracle VirtualBox |
| Operating System | Ubuntu Server 26.04.1 LTS |
| VM Name | WebSecurity-Lab |
| Hostname | websecurity |
| Memory | 2 GB |
| CPU | 1 Core |
| Virtual Disk | 25 GB |
| Network Adapter | NAT |

## 3. Application Deployment

OWASP Juice Shop is deployed as a Docker container using the following Docker image:

`bkimminich/juice-shop`

The container runs the application on port 3000 inside the Ubuntu virtual machine.

Docker is configured to restart the container automatically unless it is manually stopped.

## 4. Access Configuration

The application is accessed locally from the Mac host through SSH local port forwarding.

Browser address:

`http://127.0.0.1:3000`

The SSH tunnel forwards traffic from the Mac host's local port 3000 to port 3000 inside the Ubuntu virtual machine.

The SSH tunnel must remain active while accessing and testing the application.

## 5. Security Testing Configuration

OWASP ZAP is installed and operated on the Mac host.

The testing environment includes:

- OWASP Juice Shop as the target web application.
- OWASP ZAP as the web application security testing tool.
- Firefox for accessing the application through ZAP.
- Local proxy configuration using port 8080.
- Passive scanning while browsing the application.
- Active scanning against the authorized local Juice Shop target.

The assessment scope is restricted to:

`http://127.0.0.1:3000`

## 6. Tools and Technologies

| Tool / Technology | Purpose |
|---|---|
| Ubuntu Server | Lab operating system |
| Oracle VirtualBox | Virtual machine hosting |
| Docker | Application deployment |
| OWASP Juice Shop | Intentionally vulnerable web application |
| OWASP ZAP | Web application security testing |
| Firefox | Browser-based application testing |
| SSH | Secure remote access and port forwarding |
| GitHub | Project documentation and evidence storage |

## 7. Security Considerations

- The lab uses an intentionally vulnerable application for educational testing.
- The application is hosted inside a dedicated VirtualBox virtual machine.
- Access is provided through SSH local port forwarding.
- OWASP ZAP testing is restricted to the authorized local Juice Shop application.
- Active scanning is performed only against the intentionally vulnerable lab application.
- No unrelated external websites or systems are included in the assessment.
- Screenshots and documentation should be reviewed to ensure they do not expose sensitive information.

## 8. Conclusion

The lab environment provides an isolated and controlled setup for performing web application security testing.

The combination of Ubuntu Server, Docker, OWASP Juice Shop, and OWASP ZAP provides a practical environment for identifying, analyzing, and documenting common web application security weaknesses.
