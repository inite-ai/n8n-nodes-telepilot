# n8n-nodes-telepilot

[![npm version](https://badge.fury.io/js/n8n-nodes-telepilot.svg)](https://badge.fury.io/js/n8n-nodes-telepilot)

## Overview

`n8n-nodes-telepilot is a module for the n8n automation engine that provides the ability to configure your personal Telegram assistant. 
It works alongside your main client, allowing you to interact with Telegram servers and see all the messages you can see, 
while also enabling your assistant to react to those messages.

With `n8n-nodes-telepilot`, you can enhance your Telegram user experience by automating various actions and responses. 
Your personal Telegram Co-Pilot acts as real-time assistant, providing additional functionalities and making your Telegram usage more efficient.

At TelePilot, we prioritize your privacy. We do not have access to your Telegram messages because you have full control over your personal instance of TelePilot, 
which runs on your self-hosted n8n instance. The choice of hosting environment is entirely up to you. 

Whether you prefer the convenience of cloud hosting or the control of running it on your own machine, TelePilot allows you to make that decision. 

Probably the fastest way to get everything up and running would be using Railway n8n template:

 - [Railway](https://railway.app/new/template/zo8wVU)

If you are technically inclined, you can even launch it on your homelab or Raspberry Pi. 
For a hassle-free experience, take one of these templates for self-hosting:

 - [n8n on Cloudron](https://www.cloudron.io/store/io.n8n.cloudronapp.html)
 - [YunoHost](https://yunohost.org/en/app_n8n) / [YunoHost n8n app on github](https://github.com/YunoHost-Apps/n8n_ynh)

## Features

- Interact with other users
- Respond to private messages: Co-Pilot can respond to private messages from other users, allowing for automated answers
- Interact with channels and groups:
	- Download messages
	- Topic Notification: Stay updated on specific topics of interest by receiving notifications when they are being discussed in Telegram. 
    Configure your personal Telegram assistant to monitor and alert you whenever a particular topic is mentioned.
	- Keyword Notification: Never miss important messages by setting up keyword notifications.
    Define specific words or phrases that you are interested in, and your Telegram assistant will notify you whenever those keywords are posted in any message. 
    Stay informed and engaged with the conversations that matter to you.
	- Moderating groups
  - Schedule message posting: you can schedule messages using your Telegram Co-Pilot
- Get more API events: Telepilot can receive API events that normal bots don't know about, such as when a message gets deleted through the client.


## Installation

### Install as n8n community node

To use this package in your n8n project, follow these steps:

1. Go to Settings -> Community modules of your self-hosted n8n instance
2. Select "Install Community node"
3. Specify the name `n8n-nodes-telepilot`, click checkbox that you understand the risks and click "Install"

### Manual installation

To get started install the package in your n8n root directory:

`npm install n8n-nodes-telepilot`

For Docker-based deployments, add the following line before the font installation command in your [n8n Dockerfile](https://github.com/n8n-io/n8n/blob/master/docker/images/n8n/Dockerfile):

`RUN cd /usr/local/lib/node_modules/n8n && npm install n8n-nodes-telepilot`

## TelePilot setup

### Connect TelePilot with your Telegram Account
![Connect Telepilot with your Telegram Account](https://telepilot.co/assets/images/telegram-api-1.png)
- Log in to your Telegram core: https://my.telegram.org with your phone number that you wish to use TelePilot with
- Go to [API development tools](https://my.telegram.org/apps) and fill out the form:
  - App title: `telepilot`
  - Short name: `telepilot`
- Receive basic addresses as well as the `api_id` and `api_hash` parameters required for user authorization.

### Create Credentials in your n8n
![Configure TelePilot Credentials](https://telepilot.co/assets/images/credentials-1.png)
To initiate connection with Telegram servers, you need to provide the following credentials:
- `license_key`: you can use free license, if you need real one drop us an email at `contact@telepilot.co`
- `api_id`: copy-paste it from https://my.telegram.org/apps page
- `api_hash`: copy-paste it from https://my.telegram.org/apps page
- `phone_number`: phone number used when registering the Telegram account.

Click on "Save" and make sure that you see "Connection tested successfully" message. 

### Import workflows

You can import predefined workflows that we have created for you, check out [this page](https://telepilot.co/workflows)

### Integrate with various APIs and Services

## Usage
This package provides various nodes and actions that allow you to interact with Telegram servers and enhance the Telegram user experience. 
Please refer to the n8n Documentation for detailed information on each node and its usage.
May you have any questions, reach out to us: contact@telepilot.co

## License
This project is licensed under the CC BY-NC-ND license, see LICENSE.md file.
