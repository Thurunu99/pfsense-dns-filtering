# Network Security: DNS-Based Content Filtering using pfSense

## Project Overview
This project focuses on implementing network-level content filtering to enhance security and control web traffic. By utilizing **pfSense** as a firewall and DNS resolver, we effectively block unauthorized access to specific websites across the local network.

## Network Architecture & Setup
The project infrastructure was carefully segmented to ensure secure traffic management:
- **WAN Interface:** Configured to handle upstream traffic and Internet connectivity.
- **LAN Interface:** Established for the internal local network where client machines (SliTaz Linux) are hosted.
- **OPT/Third Interface:** Utilized for network segmentation, enhancing security and traffic isolation.

## Implementation Steps
1. **Infrastructure Configuration:** Defined WAN, LAN, and additional interfaces to ensure proper routing and security.
2. **DNS Resolver Configuration:** Accessed the pfSense web interface to configure the DNS Resolver service.
3. **Implementing Host Overrides:** Created DNS Host Overrides for target domains (e.g., facebook.com), pointing them to `0.0.0.0` to block access.
4. **Verification & Testing:**
   - Validated the block using the `nslookup` command.
   - Confirmed the blocking behavior via web browser error responses (Connection Refused).

## Documentation
You can find the detailed project report here: [Project Report](pfsense.pdf)

## Results
- **Configuration:** Successful interface setup and DNS Host Override implementation.
- **Verification:** `nslookup` confirms `0.0.0.0` resolution.
- **Security:** Effective browser-level restriction of prohibited domains.

---
*Project developed as an academic implementation for network security management.*
