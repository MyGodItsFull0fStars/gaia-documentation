
---
title: "Adaptive Streaming"
---

## Overview

Adaptive [Streaming](content/gaia/streaming/Streaming.md) is a method for improving streaming over HTTP networks.

Adaptive streaming starts at the [Encoding](content/gaia/streaming/Encoding.md) stage.
For adaptive streaming to work, different video files with different bitrates are created.

After the encoding process, the video is segmented into smaller chunks that are each a few seconds in length. 
Most streaming setups then send a series of sequences to the client, rather than an entire video file at once.
This process is important in order to be able to play a video content without having to wait for the entire video to be finished.
Segments are important for adaptive streaming because after the end of a video segment, an adjustment process is triggered, that is triggered if the connection is not able to download the video fast enough without buffering, and switches to smaller file segments.

## Example

A simple example of on-demand adaptive streaming is shown in 

> [!example] Example of On-Demand Adaptive Streaming
> 
> The multimedia content consists of video and audio components.
> The video component is encoded in three different [bitrates](content/gaia/streaming/Bitrate.md) and also contains I-frames in low frame rate in the *trick mode*.
> The corresponding audio content is available in two languages, english and french.
> Each of them are encoded in two qualities.
> >[!info] On-Demand Adaptive Streaming
> > ![example-on-demand-adaptive-streaming](content/gaia/figures/example-on-demand-adaptive-streaming.png)
> 
> In this example, a device first requests the content seqments in the highest quality of the bitstream and English audio at 128K AAC (1).
> After streaming the first segment and monitoring the effective network bandwidth, the device calculates that the actual available bandwidth is lower than the required 5Mbits/sec.
> Therefore, the next segments are requested as the next lower quality, *shown in transition 1->2*.
> 
> While streaming the next segment, the monitoring analysis has shown that the network bandwidth has further decreased to a value lower than 2Mbits/sec. In order to maintain the continuous playback, the steam switches the video content down to 500Kbits/sec and 48Kbits/sec audio, *shown in transition 2->3*.
> It streams the content in this quality until the network bandwidth improves ot be able to support a higher quality.
> 
> Next, in transition 4->5 it is shown that the user is pausing and rewinding the content. 
> The audio gets muted in the process (shown as the dashed line). 
> At some time step the user starts to play the content again, this time with French audio. Then the device starts streaming the content with the highest video and audio quality again.

## Benefits

Video content is an ever-growing channel and thus, ensuring the quality of video playback is an important and demanding task.

Adaptive streaming offers many benefits that are able to improve the video quality, such as:

* **Access to Content:** Viewers with slower connections or devices would not be able to watch some videos without the use of adaptive streaming.
* **User Experience:** With the use of adaptive streaming, the need for buffering videos decreases and users encounter fewer loading delays.
* **Less Interruptions:** Streaming on mobile devices has gained a lot of popularity in the recent years, and therefore, optimising for mobile streaming has become crucial. While physically moving the device, bitrates can vary widely on a mobile device. Therefore, adaptive streaming can be used to minimize the disruptions for mobile users by continuously adjusting to changing conditions.