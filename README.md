# PARA: Privacy Management and Control in Emerging IoT Ecosystems using Augmented Reality

## Privacy Management and Control in the IoT using AR

The ubiquity of smart devices, combined with a lack of information about data garnered by them, make privacy a significant challenge for adopting smart devices. Ensuring users can safeguard their privacy without compromising the devices' functionality requires effective yet intuitive ways to manage personal privacy preferences. Current solutions for privacy management are severely lacking as they are ineffective in making users aware of potential privacy risks or how to mitigate them and as they offer limited support for interaction. As our first contribution, we develop a novel AR privacy management interface (PARA) that uses AR visualization to contextualize data disclosure and improve user's perceptions of privacy threats. We present our system's overall design and a prototype that we have developed to support two important and popular classes of off-the-shelf consumer-grade devices:  smart speakers and smart cameras. Besides offering support for enhancing user's privacy perceptions, our interface supports privacy control on compatible devices through privacy-enhancing technologies. As our second contribution, we systematically study factors affecting privacy perceptions and privacy control for the two device classes through a user study with N=32 participants. Our results show that the contextualization and visualization of privacy disclosure offered by PARA strongly affect the participants' privacy perceptions. For privacy control, we demonstrate that our prototype improves the participant's capability to identify risks and provides an effective and easy-to-use mechanism for controlling privacy disclosure, in contrast to existing state-of-the-art privacy management interfaces. 



## The System



### The Privacy Filters
{% assign filter_default= "default" %}
{% include filters.html filter = filter_default %}


### Third parties data infering 

Emotion recognition has been actively studied from both images and audio. Patents such as Amazon [Business Insider, Alexa emotional intelligence] show the increasing interest of companies to gather more accurate information about users' whereabouts. There are several open toolkits (such as EmoPy and OpenSMILE) that can be used to accomplish this task easily. While we are not certain whether there exists a commercial device that integrates such toolkits into smart cameras or speakers, this capability exists and is easy to use, posing a real threat to the users. Furthermore, even if such a device would not be available at the moment, the patents mentioned above highlight how it is only a matter of time before they will become available, and thus our experiments cover a wide range of privacy threats, from well-known and easy to understand to complex and emerging that have not been actively studied.

