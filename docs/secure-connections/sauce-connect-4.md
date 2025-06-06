---
id: sauce-connect-4
title: Sauce Connect Proxy 4
sidebar_label: Overview
---

:::caution Important Notice: Sauce Connect 4 is reaching end-of-life status.
Starting Jan 31, 2026, servers will no longer support Sauce Connect version 4 traffic. To avoid interruptions, upgrade to [Sauce Connect 5](/secure-connections/sauce-connect-5/migrating) at your earliest convenience.
:::

If your company has firewall rules that limit your ability to run tests on Sauce Labs, you can use our Sauce Connect Proxy feature to connect to Sauce Labs in the cloud without exposing your company's IT infrastructure to security risks.

Sauce Connect is a proxy server that opens a secure connection between a Sauce Labs virtual machine, emulator, simulator or real device running your browser or native app tests, and an app or website you want to test that is on your local machine or behind a corporate firewall.

## Getting Started

Prior to getting started, you'll need to validate that your local machine meets our system requirements and confirm that your firewall rules allow for outbound traffic.

From there, install the Sauce Connect Proxy client on your local network. Should you encounter issues when starting or using the client, we recommend consulting your network administrator. They may need to update firewall rules or help configure Sauce Connect Proxy to use a network proxy.

Sauce Connect Proxy must be physically installed on the same _network_ as the app or website you're testing, but does not need to be on the same local machine. For this reason, when setting up Sauce Connect Proxy, be mindful of how it will interact with your network architecture.

### Setup and Configuration

We offer several different setup types, from the [Basic Sauce Connect Proxy Setup](/secure-connections/sauce-connect-4/setup-configuration/basic-setup) to the [High Availability Sauce Connect Proxy Setup](/secure-connections/sauce-connect-4/setup-configuration/high-availability).

As you’re configuring the setup type that’s right for you, it's important to understand how the program will interact with your network architecture components, such as proxies, firewalls, and geographically distributed data centers.

## Why We Recommend Sauce Connect Proxy over Allowlisting IP Addresses

Testing your internal systems with Sauce Labs requires that our service is able to establish a secure connection.

Rather than allowlisting our external IP addresses, we strongly recommend using our Sauce Connect Proxy tool, which will provide the following benefits:

### Configurability

Sauce Connect Proxy provides many tools designed to improve the testing experience, from selective traffic routing to bandwidth restriction.

Each Sauce Connect Proxy instance can be assigned different network proxies, run on different hosts, allocated to different users and allowed access to different systems under test. This allows infrastructure teams great control and flexibility over system access.

Allowlisting provides no controls over which systems can be accessed by which users; anyone with the correct URL can access any service.

### Portability

Sauce Connect Proxy can be used in any part of your corporate infrastructure, with relatively minimal setup. It allows you to test systems in different environments, different locations, and different physical hosts. With a flexible Sauce Connect setup, a developer can run tests on their local machine, their staging service, their build server, and anywhere else required.

Allowlisting, in comparison, requires different routes and URLs for each environment under test. This places a maintenance burden on the networking team and leads to configuration problems for testers.

### Reliability and Ease of Maintenance

Once you're up and running with Sauce Connect Proxy, no maintenance is required; you'll only need to update to the new versions of our software, upon release.

Sauce Connect Proxy can be set up for multiple corporate users and multiple systems under test, at the same time.

With Sauce Connect Proxy, our support team can provide greater assistance debugging connectivity and reliability problems, thanks to improved logging and network tracking. Additionally, Sauce Connect Proxy's underlying network tools improve reliability over bad network connections.

### Security

Sauce Labs operates from a wide range of IP addresses, which you could allocate to any test environment at any time. By allowlisting these IP addresses, any Sauce Labs customer could conceivably send requests to your system under test, and your network infrastructure would allow it. Additionally, allowlisting does not provide tools for time-based access controls or easy disconnection.

By using Sauce Connect Proxy instead of allowlisting, your network will be secure. At the end of every Sauce Connect Proxy session, upon terminating the client, the connection between our service and your infrastructure is severed, allowing you fine-grained access control.

For more information about Sauce Connect Proxy&trade; and its security, see [this white paper](https://saucelabs.com/resources/white-papers/sauce-connect-proxy-security-overview).

## More Information

- [Sauce Connect Proxy 5 Overview](/secure-connections/sauce-connect-5/)
- [Sauce Connect Proxy Quickstart](/secure-connections/sauce-connect-4/quickstart/)
- [Sauce Connect Proxy Basic Setup and Configuration](/secure-connections/sauce-connect-4/setup-configuration/basic-setup/)
- [Sauce Connect Proxy CLI Reference](/dev/cli/sauce-connect-proxy)
