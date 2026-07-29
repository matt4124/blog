---
layout: post
title: "Implementing MQTT for a Power Protection System"
header: false
---

## Overview

Developed a demonstration of a secure MQTT-based communication system for coordinating two relay and circuit breaker systems through a central network coordinator.

The project investigated how modern communication protocols could be integrated into power protection systems while maintaining secure and authenticated communication between network components.

## System Design

The system used MQTT as the communication protocol between the network coordinator and two protection systems. Secure communication was implemented using a certificate hierarchy and mutual TLS (mTLS), providing authentication and encryption between connected devices.

A Python-based graphical user interface (GUI) was developed to interact with and monitor the system.

The system was integrated with PSS®E, where a dynamic power system simulation was used to demonstrate the response of the protection system to electrical faults. This allowed the communication and protection workflow to be evaluated in the context of a simulated power network.

## Key Takeaways

This project provided experience at the intersection of power system protection, industrial communication, and cybersecurity. It demonstrated how secure communication infrastructure can be integrated with power system protection equipment and used to coordinate responses to network faults.