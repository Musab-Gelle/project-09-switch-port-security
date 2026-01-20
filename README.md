# project-09-switch-port-security
This project demonstrates Layer 2 access-layer security using Cisco Port Security to prevent unauthorized devices from connecting to the network.  Port security is commonly used in enterprise environments to protect against rogue devices and accidental desk moves.  

# Network Context
- Built on top of an existing enterprise network (VLANs + DHCP)
- Security implemented only at the **switch level**
- Routers and DHCP services remain unchanged


# Port Security Configuration
The following security policies were applied:
- Access ports only
- Maximum of **1 MAC address per port**
- **Sticky MAC learning**
- **Shutdown** mode on violation



# Violation Test
- Original PC disconnected
- Unauthorized PC connected to secured port
- Port entered **secure-shutdown** state
- Network access blocked successfully


# Recovery Procedure
```text
interface fa0/x
 shutdown
 no shutdown
