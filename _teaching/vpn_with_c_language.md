---
title: "VPN with C Language"
collection: teaching
type: "C, Ubuntu, Network, VPN"
permalink: /project/vpn_with_c_language
date: 2018-1-1
---

A command line based VPN application.

[Link to GitHub](https://github.com/ZzzGin/VPN-in-C)

- Virtual network kernel with [TUN/TAP](https://en.wikipedia.org/wiki/TUN/TAP)
  - Creating virtual network device using TUN/TAP
  - Routing data stream to the virtual NIC card by modifying routing table
  - Re-packeting data and then send to VPN server

- Encrypted tunnel using SSL based on PKI
  - Data between clients and server are encrypted by SSL tunnel 
  - Clients can verify the server

- Client login mechanism
  - Clients need to login to continue to use the VPN application
  - User names and passwords are store in a encrypted file
  - Server can verify the Clients

- Multiple clients supported
  - A mother process is listening to connection requests
  - Using fork() to create a new process for a new connected clients
  - Clients can terminate or reconnect the connection by commands

