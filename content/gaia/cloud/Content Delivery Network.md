---
title: "Content Delivery Network"
---

Content delivery networks (CDN) serve a specific region by storing copies of an original video closer to the consuming devices which reduces network congestion and improve the transmission times. So it acts as a local store (cache) for digital content.
The content on a CDN is only updated from the origin server if there is new content.

This approach is beneficial for video [Streaming](streaming/Streaming.md) because it enables the user to access a local version of a video and provides a better viewing experience and reduces latency.
Reducing the latency results in less waiting for the video to start and less buffering.

An additional benefit of CDNs is that they significantly reduce the total data traffic across the internet.

## Energy Consumption

Within the [Conventional Approach](energy/approaches/Conventional%20Approach.md), the energy consumption of data centres is estimated with an energy intensity per viewing hour of $1.3 Wh/hour$.

The equation for energy consumption related to data centres is as follows:
$$ED_{C}= ID_{C}\times D$$
Where $ED_C$ denotes the data centres energy consumption, $ID_C$denotes the energy intensity of data centres and $D$ denotes the duration of video streaming.