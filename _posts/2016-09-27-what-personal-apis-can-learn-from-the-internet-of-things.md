---
published: true
title: What Personal APIs can learn from the Internet of Things
---

![IMG_20160428_204324698-01-500x418.jpeg]({{site.baseurl}}/media/IMG_20160428_204324698-01-500x418.jpeg)
Many IoT devices exist in an occasionally connected state. For both battery and bandwidth conservation, most IoT devices are only intermittently connected. They sleep between data collection points, only connecting to cloud resources to transmit data for status. This presents a challenge in communication, placing the burden of interrupted communication on the consuming service.

A pattern has emerged in IoT that uses a cloud resource for an IoT device. The cloud resource acts as a highly available proxy for the device itself, usually containing a record of last device state, data history, and allowing messages or data to be queued to the device. An occasionally connected temperature sensor can now make its temperature information highly available without maintaining a constant connection.

This concept is present in [Picos][pico], and also shows up in more limited form on the [AWS IoT][awsiot] platform in the form of a [Device Shadow][ds]. The pattern of pairing a cloud representation to a physical IoT device applies directly to Personal APIs.

## My Agent

Establishing a cloud representation of individual people brings all the benefits demonstrated in the IoT world. **My personal API is a highly available representation of me**, allowing communication with me in spite of my partially connected state. 

Our connectivity as humans is limited by gaps in cellular coverage, but more significantly by our need to not be glued to our digital devices.

Personal APIs can serve to answer questions about us without directly interfacing with us. If I’ve granted permission, you should be able to ask about my food preferences and allergies, request a phone call, or send me a message. You can do all these things no matter my physical location, cellular connection status, or my preferences for interruption.

Since the beginning of the Internet, we humans, the 'users' of the Internet, have been granted online presence only through the graces of established 'always on' businesses. With the exception of those who arranged their own domain, DNS, and hosting, most humans are represented online only by companies who sell access to us for a profit. Our presence on the Internet is shaped by their financial desires. 

## We Can Do This

If we want to be first class citizens in an API world, we need to find a way to establish an online presence on our own terms, and under our own control. The challenges of creating an API to represent us individually (including all the requirements for high availability) are difficult but not insurmountable. The reward for such effort is an Internet of peers, connected by choice.

[ds]: http://docs.aws.amazon.com/iot/latest/developerguide/iot-thing-shadows.html
[pico]: https://picolabs.atlassian.net/wiki/display/docs/Persistent+Compute+Objects
[awsiot]: https://aws.amazon.com/iot/
