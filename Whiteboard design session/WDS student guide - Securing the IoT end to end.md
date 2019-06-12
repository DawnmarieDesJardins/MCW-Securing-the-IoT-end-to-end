![](https://github.com/Microsoft/MCW-Template-Cloud-Workshop/raw/master/Media/ms-cloud-workshop.png "Microsoft Cloud Workshops")

<div class="MCWHeader1">
Securing the IoT end to end
</div>

<div class="MCWHeader2">
Whiteboard design session student guide
</div>

<div class="MCWHeader3">
June 2019
</div>


Information in this document, including URL and other Internet Web site references, is subject to change without notice. Unless otherwise noted, the example companies, organizations, products, domain names, e-mail addresses, logos, people, places, and events depicted herein are fictitious, and no association with any real company, organization, product, domain name, e-mail address, logo, person, place or event is intended or should be inferred. Complying with all applicable copyright laws is the responsibility of the user. Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.

Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document. Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.

The names of manufacturers, products, or URLs are provided for informational purposes only and Microsoft makes no representations and warranties, either expressed, implied, or statutory, regarding these manufacturers or the use of the products with any Microsoft technologies. The inclusion of a manufacturer or product does not imply endorsement of Microsoft of the manufacturer or product. Links may be provided to third party sites. Such sites are not under the control of Microsoft and Microsoft is not responsible for the contents of any linked site or any link contained in a linked site, or any changes or updates to such sites. Microsoft is not responsible for webcasting or any other form of transmission received from any linked site. Microsoft is providing these links to you only as a convenience, and the inclusion of any link does not imply endorsement of Microsoft of the site or the products contained therein.

© 2019 Microsoft Corporation. All rights reserved.

Microsoft and the trademarks listed at <https://www.microsoft.com/en-us/legal/intellectualproperty/Trademarks/Usage/General.aspx> are trademarks of the Microsoft group of companies. All other trademarks are property of their respective owners.

**Contents**

<!-- TOC -->

- [Securing the IoT end to end whiteboard design session student guide](#securing-the-iot-end-to-end-whiteboard-design-session-student-guide)
    - [Abstract and learning objectives](#abstract-and-learning-objectives)
    - [Step 1: Review the customer case study](#step-1-review-the-customer-case-study)
        - [Customer situation](#customer-situation)
        - [Customer needs](#customer-needs)
        - [Customer objections](#customer-objections)
        - [Infographic for common scenarios](#infographic-for-common-scenarios)
    - [Step 2: Design a proof of concept solution](#step-2-design-a-proof-of-concept-solution)
    - [Step 3: Present the solution](#step-3-present-the-solution)
    - [Wrap-up](#wrap-up)
    - [Additional references](#additional-references)

<!-- /TOC -->

# Securing the IoT end to end whiteboard design session student guide

## Abstract and learning objectives 

In this whiteboard design session, you will work with a group to design an end-to-end solution that leverages Microsoft Azure's IoT features, tools and resources to secure and monitor a set of IoT devices.

At the end of this session, you will be better able to design and recommend solutions that help organizations properly secure and monitor their IoT-based infrastructure.

## Step 1: Review the customer case study 

**Outcome**

Analyze your customer's needs.

Timeframe: 15 minutes

Directions: With all participants in the session, the facilitator/SME presents an overview of the customer case study along with technical tips.

1.  Meet your table participants and trainer.

2.  Read all of the directions for steps 1-3 in the student guide.

3.  As a table team, review the following customer case study.


### Customer situation

Contoso, Ltd. has major holdings in one of the world’s most important oil-producing regions. To overcome the challenges of monitoring and optimizing a vast number of widely dispersed field assets, Contoso, Ltd. is looking to streamline its operations with IoT solutions. They want to deploy IoT technologies to electronically collect data and use cloud based solutions to store and analyze it in order to gain new insights into well operations and future drilling possibilities. 

Their environments are very tough environments in which to work. The climate is hot, harsh, and unforgiving, and oil wells are often spaced many miles apart, so field technicians can spend much of their day just driving from one to another. Cellular and radio reception is spotty at best, so collecting data about well conditions and performance typically involves manually writing down information. The technician must then make the long trek to the central office at the end of the day to upload the data for analysis. With such remote situations, a key concern for Contoso is not only how they manage these remote devices, but more broadly how they secure the complete solution that encompasses the physical device, the software on the device, the services processing the data in the cloud and the network connecting it all. 

Contoso plans to tie in to existing sensors at the well head that monitor key system parameters like temperatures, pressures, and flow rates. They will deploy gateway devices route device data for processing, storage and analytics. Internal IT staff and engineers want to visualize the high-resolution data and deliver near real-time analyses. The company is placing a premium on flexibility and ease of use, with security as a fundamental. 

In addition, they would also like see the solution yield benefits to their workers in the field. “The field technicians and lease operators already have tools on their phones that they use every day to see what a well is doing,” explains Miles Strom. “Our goal is to connect these tools to live data from the IoT sensors. So, instead of seeing low-resolution volumes or flow rates, they’ll see what is happening in real time. This way they can respond immediately to problems that lead to downtime or maintenance issues.”

They have implemented a proof of concept solution for collecting and analyzing device telemetry using IoT Hub, but are interested in learning about any related services in Azure that would help them to secure such solutions. 

### Customer needs 

1.  Ensure that all IoT devices are properly registered and assigned a secure tamperproof identity.

2.  Ensure devices are operating within assigned policy standards and are not tampered with.

3.  Enable an alerting solution with little to no effort configuration that will notify and allow for remediation in the case of fault or malicious activity.

4.  Ensure all events are surfaced in one place for simplicity.

5.  Address the need to have auditing and monitoring across a wide range of device operating systems and processor architectures (Linux, x86, x64, etc).

6.  Automate the security agent provisioning rather than having to physically or remotely "touch" all the devices.

7.  Ensure only the most secure protocols are implemented and used during any transmissions

8.  Ensure that in the future it will be possible to have an enterprise-wide look at any vulnerabilities or malicious events, not just specifically focused the IoT infrastructure.

### Customer objections 

1.  Contoso, Ltd staff are worried it may be impossible to manage the many thousands of IoT devices they have deployed around the world with any one product.

2.  Can Azure handle all the different types of operating systems and processor architectures of their devices?

3.  Will they be able to monitor for specific events on some of their propriatary devices?

4.  Can Azure support non-TPM hardware devices?

5.  Will the communications from a device to Azure be secure enough?

6.  Can an Azure logging solution handle the massive amount of events and alerts that will need to be ingested?

7.  Is it possible to assign role-based permissions based on their security objectives and policies to the IoT resources such as the Hub, Edge and individual devices? 

8.  Is the solution capable of being flexible in the types of reporting and alerts that can be generated based on custom logging event data?

9.  Will we be able to limit the messages and network traffic to specific network IP addresses/subnets for our devices?

### Infographic for common scenarios

![Envisioned situation](../Media/envisioned-situation.png)

## Step 2: Design a proof of concept solution

**Outcome**

Design a solution and prepare to present the solution to the target customer audience in a 15-minute chalk-talk format.

Timeframe: 60 minutes

**Business needs**

Directions:  With all participants at your table, answer the following questions and list the answers on a flip chart:

1.  Who should you present this solution to? Who is your target customer audience? Who are the decision makers?

2.  What customer business needs do you need to address with your solution?

**Design**

Directions: With all participants at your table, respond to the following questions on a flip chart:

*High-level architecture*

Without getting into the details (the following sections will address the details), diagram your initial vision for handling the top-level requirements.

Briefly sketch-out and propose a high-level solution that meets the customer's business and technical needs and mitigates their objections. For this workshop, you may choose from the following technologies (you may not need all of them in the correct solution):

1.  IoT Hub and Provisioning Service

2.  Azure Networks and Network Security Groups

3.  Virtual Private Networks (Point to Point, Site to Site) and Express Route

4.  Azure Web Apps

5.  Azure Log Analytics

6.  Azure Security Center

7.  Azure Sentinel

8.  Azure Active Directory

*Azure Security*

Describe how you will utilize Azure security features to secure the various resources such as the following:

1.  How will you secure the IoT Hub?

2.  How will you secure the IoT Provisioning Service?

*Device Security*

Describe how you will secure the following:

1.  How will you secure the IoT Edge Devices?

2.  How will you secure the IoT Devices?

*Ensuring auditing and compliance*

Describe how you will use Azure features to ensure the following:

1.  How will you monitor and audit device access?

2.  How will you monitor and audit Azure resource changes?

3.  Create custom alerts and execute remediation and investigation activities on detection?

4.  What tools would you setup to surface audit and compliance reporting to IT Executives?

**Prepare**

Directions: With all participants at your table:

1.  Identify any customer needs that are not addressed with the proposed solution.

2.  Identify the benefits of your solution.

3.  Determine how you will respond to the customer's objections.

Prepare a 15-minute chalk-talk style presentation to the customer.

## Step 3: Present the solution

**Outcome**

Present a solution to the target customer audience in a 15-minute chalk-talk format.

Timeframe: 30 minutes

**Presentation**

Directions:

1.  Pair with another table.

2.  One table is the Microsoft team and the other table is the customer.

3.  The Microsoft team presents their proposed solution to the customer.

4.  The customer makes one of the objections from the list of objections.

5.  The Microsoft team responds to the objection.

6.  The customer team gives feedback to the Microsoft team.

7.  Tables switch roles and repeat Steps 2-6.

##  Wrap-up 

Timeframe: 15 minutes

Directions: Tables reconvene with the larger group to hear the facilitator/SME share the preferred solution for the case study.

##  Additional references

|    |            |
|----------|:-------------:|
| **Description** | **Links** |
| Azure IoT Hub   | https://docs.microsoft.com/en-us/azure/iot-hub/  |
| Azure IoT Edge   | https://docs.microsoft.com/en-us/azure/iot-edge/  |
| Azure IoT Device Provisioning Service   | https://docs.microsoft.com/en-us/azure/iot-dps/  |
| Azure IoT Edge Security Manager  |  https://docs.microsoft.com/en-us/azure/iot-edge/iot-edge-security-manager|
| Azure Security Center for IoT  | https://docs.microsoft.com/en-us/azure/asc-for-iot/overview  |
| Azure IoT SDK  | https://github.com/Azure/azure-iot-sdks  |
| Azure IoT Security Agent  | https://github.com/Azure/Azure-IoT-Security-Agent-C  |
| Azure Sentinel   | <https://docs.microsoft.com/en-us/azure/sentinel/>   |
| Azure Policy   | <https://azure.microsoft.com/en-us/services/azure-policy/>   |
| Compliance Commitments   |  <http://azure.microsoft.com/en-us/support/trust-center/services/>  |
| Azure Trust Center  | <http://azure.microsoft.com/en-us/support/trust-center/>     |