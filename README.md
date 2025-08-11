# Wireshark Network Traffic Analysis Project

This repository contains the deliverables for a hands-on network analysis task. The goal was to capture live network traffic from a Linux VM and analyze the behavior of fundamental internet protocols using Wireshark.

## Project Objective

To develop practical, hands-on skills in packet capture and analysis, moving from theoretical knowledge of protocols to direct observation of their real-world implementation.

## Deliverables

*   **`packet_captures/capturing_packets.pcapng`**: The raw packet capture file containing all traffic from the analysis session. This can be opened with Wireshark.
*   **`Network_Analysis_Report.pdf`**: A detailed report (created from the template above) documenting the methodology, specific findings, and conclusions drawn from the packet data.

## How the Capture Was Performed

The traffic was generated on an Ubuntu Linux VM with the following actions:

1.  **Pinging `google.com`**: To generate ICMP traffic.
2.  **Visiting `https://github.com`**: To generate DNS, TCP, and HTTPS/TLS traffic.
3.  **Using `dig cnn.com`**: To isolate a specific DNS query.

## Key Protocols Identified and Analyzed

My analysis of the `.pcapng` file focused on the interplay between these protocols:

*   **DNS**: Observed standard A record queries over UDP port 53. For example, my machine (`[Your VM's IP]`) queried `[Your DNS Server IP]` to resolve `[e.g., github.com]`.
*   **ICMP**: Isolated a clear sequence of 10 echo requests and replies, confirming connectivity with `[e.g., Google's IP address]`.
*   **TCP**: Watched multiple three-way handshakes establish connections for web browsing. A key example was the connection to `[e.g., GitHub's IP]` on port 443.
*   **TLS/HTTPS**: Analyzed the TLS handshake (Client Hello, Server Hello) that secured the session with GitHub, rendering the subsequent "Application Data" unreadable.

## Outcome and Skills Gained

This project was instrumental in developing my network analysis skills. I am now proficient in:
*   Configuring Wireshark on Linux.
*   Capturing and saving live network traffic.
*   Applying display filters to isolate specific conversations.
*   Analyzing protocol handshakes (TCP, TLS) and request/response pairs (DNS, ICMP).
