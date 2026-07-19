# Network Security: DNS-Based Content Filtering using pfSense

## Project Overview
This project focuses on implementing network-level content filtering to enhance security and control web traffic. By utilizing **pfSense** as a firewall and DNS resolver, we can effectively block unauthorized access to specific websites across the local network. 

This solution is designed to prevent users from accessing restricted domains by nullifying DNS resolution at the firewall level.

## Tools and Technologies
- **Firewall/Gateway:** pfSense
- **Client OS:** SliTaz Linux
- **Network Protocol:** DNS (Domain Name System)
- **Methodology:** Host Overrides & DNS Null-routing

## Implementation Steps
The project was executed through the following stages:

1. **Environment Setup:** Configured a local network with a pfSense gateway and a SliTaz Linux client.
2. **DNS Resolver Configuration:** Accessed the pfSense web interface to configure the DNS Resolver service.
3. **Implementing Host Overrides:** Created DNS Host Overrides for target domains (e.g., facebook.com), pointing them to `0.0.0.0`. This ensures that any request to these domains is blocked at the DNS level.
4. **Verification & Testing:** 
   - Validated the block using the `nslookup` command from the client machine.
   - Confirmed the blocking behavior via web browser error responses (Connection Refused).

## Documentation
You can find the detailed project report here: [Project Report](pfsense.pdf)

## Results
Below are the key milestones captured during the implementation:

- **Configuration:** pfSense DNS Resolver settings.
- **Verification:** `nslookup` test confirming `0.0.0.0` resolution.
- **Client Response:** Browser successfully displaying a 'Connection Refused' error.

---
*Project developed as an academic implementation for network security management.*
