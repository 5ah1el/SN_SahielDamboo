Technical Design: Personal Home Cloud

This document outlines the technical architecture, technology stack, implementation details, and design trade-offs for the Personal Home Cloud project.
1. High-Level Architecture

The system is designed with a layered security approach, prioritizing secure remote access and clear separation of services. The diagram below illustrates the network traffic flow and component interactions.
User Access Scenarios:

    Remote Admin/Family (Most Secure): User -> INTERNET -> WireGuard VPN Tunnel -> Home Router -> Home Cloud Server

    Remote Guest (Restricted): User -> INTERNET -> HTTPS -> Reverse Proxy -> Home Cloud Server (Guest Portal)

    Local User (On Home Wi-Fi): User -> LAN -> Home Cloud Server


