# PARA: Privacy Management and Control in Emerging IoT Ecosystems using Augmented Reality

## Privacy Management and Control in the IoT using AR

The ubiquity of smart devices, combined with a lack of information about data garnered by them, make privacy a significant challenge for adopting smart devices. Ensuring users can safeguard their privacy without compromising the devices' functionality requires effective yet intuitive ways to manage personal privacy preferences. Current solutions for privacy management are severely lacking as they are ineffective in making users aware of potential privacy risks or how to mitigate them and as they offer limited support for interaction. As our first contribution, we develop a novel AR privacy management interface (PARA) that uses AR visualization to contextualize data disclosure and improve user's perceptions of privacy threats. We present our system's overall design and a prototype that we have developed to support two important and popular classes of off-the-shelf consumer-grade devices:  smart speakers and smart cameras. Besides offering support for enhancing user's privacy perceptions, our interface supports privacy control on compatible devices through privacy-enhancing technologies. As our second contribution, we systematically study factors affecting privacy perceptions and privacy control for the two device classes through a user study with N=32 participants. Our results show that the contextualization and visualization of privacy disclosure offered by PARA strongly affect the participants' privacy perceptions. For privacy control, we demonstrate that our prototype improves the participant's capability to identify risks and provides an effective and easy-to-use mechanism for controlling privacy disclosure, in contrast to existing state-of-the-art privacy management interfaces. 

Therefore, we explore the effects on privacy and compare PARA with the widely used approaches on smart devices. In brief, PARA offers an AR interface that enables users to explore and configure the disclosed data in real-time. PARA also contains a software component named privacy filters that obfuscates the sensor data before the permission of data disclosure. 

PARA consists of three components: smart devices, privacy filters, and a user application. 
First, the smart device transmits the collected privacy-protected data, supported by two components: (i) *privacy manager* that applies the current privacy filter configuration to the \textit{collected data}, and (ii) *databases* storing users' privacy preferences as well as privacy filter statistics (e.g., activation and deactivation time with a device). Second, the **privacy filter (PF)** obfuscates the user's personal information such as face, eye, age, gender, and emotion, using data manipulations such as deepfake approaches (narula2020preserving-10.1145/3382507.3418833, shirai2019privacy,li2019anonymousnet). We select these filters following previous works (zhang2021did, apthorpe2018discovering-10.1145/3214262) that highlight the risks of video analytics (e.g., emotion recognition (yin2020speaker))(zhang2021did) and users concerns in ubiquitous environments regarding the types of collected data (apthorpe2018discovering-10.1145/3214262). Moreover, these filters are easier for the participants to understand our prototype.



## The System

Augmented Reality (AR) facilitates natural interaction between users and smart devices (mayer2014magic, becker2020connecting,park2019iot, mayer2014magic, lee-survey, Shatilov2021EmergingEN), and has great potential to improve user privacy (kumar2021-mm,krings2020development,park2019iot). Previous works demonstrate that exposing the physical locations of smart device in the user's vicinity (bermejo2021_seeing,song2020m,apthorpe2018discovering-10.1145/3214262,naeini2017privacy) could enhance user privacy. PARA builds on top of previous findings (bermejo2021_seeing) but goes one step further, contextualizing the privacy capability once such threats from nearby smart devices appear. 

In general, users feel comfortable with smart devices when the shared data is conditioned on informed consent (apthorpe2018discovering-10.1145/3214262). AR can serve as a privacy-consent interface for user-device interaction (bermejo2021_seeing). Once the user's device appears in the camera FOV, PARA alleviates the cumbersome and often overwhelming list of data sharing permission (park2019iot). 



### The Privacy Filters

As shown in the Figure below, when the user enables any of the privacy filters (e.g., gender) to the smart camera, the system replaces the authentic face by a 'generated' one, which contains a randomly assigned gender, different emotion (narula2020preserving-10.1145/3382507.341883), and similar age to the original (shirai2019privacy). 

Although there are numerous alternatives to implementing the filters, such as physical filters (champion2019smart), and middleware (davies2016privacy), we pick embedded filters that reside directly on the devices (song2018situ). Rather than constantly moving a tremendous amount of data to the cloud or edge devices, we perform the inference tasks in the smart device. This approach also reduces privacy threats that might appear during the data transmission or in the cloud (song2018situ). 

Finally, user application displays user data being collected by nearby smart devices and the currently enabled privacy filters. 
The application detects nearby smart devices using object detection and Bluetooth. Smart devices images are registered in our database. Users via AR can interact with smart devices to alter the privacy filters' status, i.e. enabled/disabled data collection, and inspect how the *privacy filters* affects the collected data in real-time. In scenarios when devices are installed in the same room and the field of view of the camera, the interface will only visualize the location of these devices (motivated by Song *et al.* (song2020m)). The users can select by touching on the screen the device to configure the device and show more related information such as privacy filters and collected data.

{% assign filter_default= "default" %}
{% assign caption_default= "" %}
{% include filters.html filter = filter_default caption = caption_default %}


### Third parties data infering 

Emotion recognition has been actively studied from both images and audio. Patents such as Amazon [Business Insider, Alexa emotional intelligence] show the increasing interest of companies to gather more accurate information about users' whereabouts. There are several open toolkits (such as EmoPy and OpenSMILE) that can be used to accomplish this task easily. While we are not certain whether there exists a commercial device that integrates such toolkits into smart cameras or speakers, this capability exists and is easy to use, posing a real threat to the users. Furthermore, even if such a device would not be available at the moment, the patents mentioned above highlight how it is only a matter of time before they will become available, and thus our experiments cover a wide range of privacy threats, from well-known and easy to understand to complex and emerging that have not been actively studied.


## Source

- Proceedings of the 2021 International Conference on Multimodal Interaction (ICMI '21). *DOI: 10.1145/3462244.3479885*

### Authors
- Carlos Bermejo Fernandez <cbf@cse.ust.hk>
- Lik Hang Lee <likhang.lee@kaist.ac.kr>
- Petteri Nurmi <petteri.nurmi@helsinki.fi>
- Pan Hui <panhui@cse.ust.hk>



