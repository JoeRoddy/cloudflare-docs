---
pcx_content_type: get-started
title: Calls vs regular SFUs
weight: 4
---

## Cloudflare Calls vs. Traditional SFUs

Cloudflare Calls represents a paradigm shift in building real-time applications by leveraging a distributed real-time data plane. It creates a seamless experience in real-time communication, transcending traditional geographical limitations and scalability concerns. Calls is designed for developers looking to integrate WebRTC funcintionalities in a server-client architecture without delving deep into the complexities of regional scaling or server management.

### The Limitations of Centralized SFUs

Selective Forwarding Units (SFUs) play a critical role in managing WebRTC connections by selectively forwarding media streams to participants in a video call. However, their centralized nature introduces inherent limitations:

- **Regional Dependency:** A centralized SFU requires a specific region for deployment, leading to latency issues for global users except for those in proximity to the selected region.

- **Scalability Concerns:** Scaling a centralized SFU to meet global demand can be challenging and inefficient, often requiring additional infrastructure and complexity.

### How is Cloudflare Calls different

Cloudflare Calls addresses these limitations by leveraging Cloudflare's global network infrastructure:

- **Global Distribution Without Regions:** Unlike traditional SFUs, Cloudflare Calls operates on a global scale without regional constraints. It utilizes Cloudflare's extensive network of over 250 locations worldwide to ensure low-latency video forwarding, making it fast and efficient for users globally.

- **Decentralized Architecture:** There are no dedicated servers for Calls. Every server within Cloudflare's network contributes to handling Calls, ensuring scalability and reliability. This approach mirrors the distributed nature of Cloudflare's products such as 1.1.1.1 DNS or Cloudflare's CDN.

## How Cloudflare Calls Works

### Establishing Peer Connections

To initiate a real-time communication session, an end user's client establishes a WebRTC PeerConnection to the nearest Cloudflare location. This connection benefits from anycast routing, optimizing for the lowest possible latency.

### Signaling and Media Stream Management

- **HTTPS API for Signaling:** Cloudflare Calls simplifies signaling with a straightforward HTTPS API. This API manages the initiation and coordination of media streams, enabling clients to push new MediaStreamTracks or request these tracks from the server.

- **Efficient Media Handling:** Unlike traditional approaches that require multiple connections for different media streams from different clients, Cloudflare Calls maintains a single PeerConnection per client. This streamlined process reduces complexity and improves performance by handling both the push and pull of media through a singular connection.

### Application-Level Management

Cloudflare Calls delegates the responsibility of state management and participant tracking to the application layer. Developers are empowered to design their logic for handling events such as participant joins or media stream updates, offering flexibility to create tailored experiences in applications.

## Getting Started with Cloudflare Calls

Integrating Cloudflare Calls into your application promises a straightforward and efficient process, removing the hurdles of regional scalability and server managementso you can focus on creating engaging real-time experiences for users worldwide.
