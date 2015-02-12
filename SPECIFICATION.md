# Thug Pigeon Specification

Here are described the specification of all features and components of the Thug Pigeon project.

## Summary
- [Features](#features)
- [Daemon](#daemon)
- [Mailer Service](#mailer)
- [Web Service](#webservice)
- [Database](#database)
- [API](#api)
- [SDK's](#sdk)

##<a name="features"></a>Features
- Campaign management
- Send process totally independent and controlled
- Scheduled campaigns
- Delivery report
- Bounce Collector with black list support (mod_bounce)
- Outgoing IP Balancing based in ISP (mod_balance)
- OAuth security (mod_auth)
- Cluster ready (mod_cluster)
- And more...

##<a name="daemon"></a>Daemon

The Thug Pigeon daemon is a background service that will run on server listening for commands to be executed, like start a send process, clear the queue or anything that need to be executed in the background runtime of Thug Pigeon service. That's no defined in what language it will be written, but for now, I'm thinking in something like C ANSI, C++ or Python, but this doesn't care for now.

##<a name="mailer"></a>Mailer Service

The Mailer Service is the CLI application that will be responsible to send the emails of an campaign, it will get the queue of campaign, build the request and send the email itself.

##<a name="webservice"></a>Web Service

The Web Service will be the interface that you'll provide to your applications to communicate and control the Thug Pigeon service, it will be written firstly in PHP, after in NodeJS and possibly in other languages.

##<a name="database"></a>Database

The Thug Pigeon will use MySQL as the main database that will store the most of all things of the Thug Pigeon service. It will use too MongoDB for the mail queue, the statistics about the sent emails and the black list created by the bounce collector. I'm thinking too in use Redis or Memcached to improve the Thug Pigeon performance, but this can be discussed later.

##<a name="api"></a>API

The API will be the last step of the project ROADMAP that consists in a powerful API with CLI support to be integrated with other server side applications, something to think yet.

##<a name="sdk"></a>SDK's

We're looking to provide SDK's for some languages to facilitate the integration of their systems.
