### REVIEW SOCIAL COMMUNICATION FOR CALLCENTER
```
Author: Kevin.nguyen.eng
Author Email:kevin.nguyen.eng@gmail.com
```
## Table of contents
- [CISCO FINESSE](#CISCO-FINESSE)
    - [Cisco Finesse APIs](#Cisco-Finesse-APIs)
	- [Cisco Finesse Desktop APIs](#Cisco-Finesse-Desktop-APIs)
	- [Cisco Finesse Configuration APIs](#Cisco-Finesse-Configuration-APIs)
	- [Cisco Finesse Serviceability APIs](#Cisco-Finesse-Serviceability-APIs)
	- [Cisco Finesse Notifications](#Cisco-Finesse-Notifications)
	- [Open Resource Reference](#Open-Resource-Reference)
- [SOCIAL MINNER](#SOCIAL-MINNER)
	- [Authentication](#Authentication)
	- [Chat Feed](#Chat-Feed)
	- [Conversation (Twitter)](#Conversation-(Twitter))
	- [Twitter Reply](#Twitter-Reply)
	- [Email](#Email)
	- [Email Reply](#Email-Reply)
	- [Facebook Reply](#Facebook-Reply)
	- [Push Feed](#Push-Feed)
	- [XMPP BOSH Eventing](#XMPP-BOSH-Eventing)
	- [Custom reply Templates](#Custom-reply-Templates)
	- [XMPP BOSH Eventing](#XMPP-BOSH-Eventing)
	- [XMPP BOSH Eventing](#XMPP-BOSH-Eventing)
- [SOCIAL CONNECTOR](#SOCIAL-CONNECTOR)
	- [uccx chat connector for facebook](#uccx-chat-connector)
- [UCCX](#UCCX)

	
## Content

### CISCO FINESSE

GET requests are synchronous. That is, the response body of a successful GET request contains all requested
contents, which you can view in Poster or RESTClient. No event is published by XMPP and no event is
received in Pidgin.

PUT and POST requests are asynchronous. A successful response is an HTTP return code of 200 or 202. The
response body does not contain the updated object information.

If a PUT , POST , or DELETE request is on a User or Dialog object, the update is published by XMPP as a
real-time event to Pidgin. If a PUT , POST , or DELETE request is on a configuration object (for example, a
ReasonCode object), XMPP does not publish a real-time update. Y ou must perform a GET request to get an
updated copy of the object.

Failed GET, PUT , POST , and DELETE requests are synchronous. If a request fails, Poster or RESTClient
display the error . No event is published by XMPP to Pidgin.
The following sections provide instructions and examples for using the APIs with Poster and Pidgin.
	
* .[An Overview of XMPP](https://xmpp.org/about/technology-overview.html)
* .[Pidgin](http://pidgin.im/)
* .[Poster](https://www.wiztools.org/)

#### Cisco Finesse APIs
Sign In to Finesse

		• Finesse server FQDN: finesse1.xyz.com
		• Agent name: John Smith
		• Agent ID: 1234
		• Agent password: 1001
		• Agent extension: 1001
```
METHOD: PUT
URI: http://finesse1.xyz.com/finesse/api/User/1234
Header:
	Content-Type: application/XML
Body:
	<User>
	<state>LOGIN</state>
	<extension>1001</extension>
	</User>
```		
Change Agent State

Agents and supervisors use the Cisco Finesse Desktop APIs to communicate between the Finesse desktop
and Finesse server, and Unified Contact Center Enterprise (Unified CCE) or Unified Contact Center Express
(Unified CCX) to send and receive information about the following

		• Agents and agent states
		• Calls and call states
		• Teams
		• Queues
		• Client logs

#### Cisco Finesse Desktop APIs
Administrators use the Cisco Finesse configuration APIs to configure the following:

		• System, cluster, and database settings
		• Finesse desktop and call variable layout
		• Reason codes and wrap-up reasons
		• Phonebooks and contacts
		• T eam resources
		• Workflows and workflow actions

Finesse configuration APIs require administrator credentials (the application user ID and password) to be
passed in the basic authorization header .

#### Cisco Finesse Configuration APIs
#### Cisco Finesse Serviceability APIs
#### Cisco Finesse Notifications
The Cisco Finesse Web Service sends notifications to clients that subscribe to that class of resource.
For example, a client that is subscribed to User notifications receives a notification when an agent signs in or
out of the Finesse desktop, information about an agent changes, or an agent's state changes.

Note:
```
The preceding example illustrates some cases where notifications are sent. It is not intended to be an
exhaustive list.
```
Note:
```
Notification payloads are XML-encoded. If these payloads contain any special XML characters, you must
ensure that the client decodes this information correctly before processing it further .
```

#### Open Resource Reference
* .[Sample Gadgets and code for use with Finesse](https://github.com/CiscoDevNet/finesse-sample-code)
* .[Sample code for the Cisco DevNet Coding Skills Learning Labs](https://github.com/CiscoDevNet/coding-skills-sample-code)
* .[This repository holds code samples for DevNet Express DNA Track](https://github.com/CiscoDevNet/devnet-express-code-samples)
* .[Chatbot samples for Webex Teams built with Botkit ](https://github.com/CiscoDevNet/botkit-webex-samples)
* .[Code Samples to go along with the Learning Labs intro-standard-device-interfaces-learning-labs](https://github.com/CiscoDevNet/intro-standard-device-interfaces-code-samples)
* .[DEPRECATED: Cisco Jabber Bot SDK and sample code](https://github.com/CiscoDevNet/cisco-jabber-bot-sdk)
* .[Sample code for use with Unified Contact Center Express](https://github.com/CiscoDevNet/uccx-sample-code)
* .[Sample code using Cisco SocialMiner APIs](https://github.com/CiscoDevNet/socialminer-sample-code)
* .[Bot Connector allows you to connect your bot to multiple messaging channels.](https://github.com/RecastAI/bot-connector)
* .[Python 2.6+/3.1+ XMPP Library ](https://github.com/fritzy/SleekXMPP)
* .[XMPP for JavaScript ](https://github.com/xmppjs/xmpp.js)
* .[Modern XMPP in the browser, with a JSON API](https://github.com/legastero/stanza.io)
* .[Simple UCCX Dashboard Example](https://github.com/Holoskevych/SimpleUCCXDashboardExample)
* .[https://github.com/umnagendra/socialminer-pop-chat](https://github.com/umnagendra/socialminer-pop-chat)
### SOCIAL-MINNER
* .[Cisco Social Miner](https://developer.cisco.com/site/socialminer/overview)
* .[Cisco UCX](https://developer.cisco.com/site/contact-center-express/)
* .[Facebook Messenger Platform](https://developers.facebook.com/docs/messenger-platform)
* .[ngrok](https://ngrok.com/)
* .[botly](https://github.com/miki2826/botly)

![home](https://user-images.githubusercontent.com/990210/31310748-540c99d8-abbb-11e7-848d-67e6f03a2234.png)
* .[Illustrates a proactive customer pop-up chat using Cisco SocialMiner RESTful APIs](https://github.com/umnagendra/socialminer-pop-chat)
* .[SocialMiner example1](https://github.com/kingsBSD/SocialMiner)
* .[SocialMiner example2](https://github.com/dakk/socialminer)
* .[SocialMiner example3](https://github.com/umnagendra/melania)
### SOCIAL-CONNECTOR

### UCCX
* .[Simple UCCX Dashboard Example](https://github.com/Holoskevych/SimpleUCCXDashboardExample)
#### uccx-chat-connector
With this connector customers can be routed to a Cisco contact center from Facebook Messenger! The UCCX Chat Connector is a simple NodeJS web application. It will need to be publicly accessible along with access to the Cisco Social Miner server.
```
https://github.com/bdm1981/uccx-chat-connector 
```