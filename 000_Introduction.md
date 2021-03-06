
# Introduction

Implementing a containerized environment is changing a lot not only how deployments are done but it also has a huge impact on a system and networking level and how hardware and network resources are being used.

This document is helping you to secure your containerized environment and keep it secure.


## Application Security?

There are often misunderstandings of what the security impacts - negative or positive - are supposed to be when using Docker.

Docker as any other containerization technology doesn't solve application security problems. It doesn't help doing input validation and it doesn't provide protecting against SQL injection. For application security risks OWASP provides a lot of other useful documents, starting from the OWASP Top 10 over the [https://www.owasp.org/index.php/OWASP_Proactive_Controls OWASP Proactive Controls] to the [https://www.owasp.org/index.php/Category:OWASP_Application_Security_Verification_Standard_Project OWASP Application Security Verification standard] -- just to name a few.

Container Security is mostly about system and network security and a secure architectural design.

This indicates that it is best _before_ you start using containerization, you should plan your environment in a secure manner. Some points are just difficult or costly to change later when you started already rolling out your containerization in production.

## Shift in Paradigm: new vectors

Looking at it from the perspective of the classical world, especially in system and network areas containerization  means big changes to your environment. Those changes are opening up new potential attack surfaces. Special care has to be taken so that no network and system security problems arise.

Apart from these technical areas there are two non-technical points:

* Docker with its 5 years is a relatively new technology. Subtracting the time for maturing and adoption the time span is even shorter. Every new technology needs time until the knowledge of the technology and their best practices becomes common knowledge.
* While container solutions might offer benefits for the developer, the technology is not simple from the security perspective. Not being simple is what makes security more difficult, a.k.a. the _KISS principle_ -- keep it simple and stupid.

This is what this document is trying to help you with: It provides you with the knowledge to avoid common pitfalls in the system and network area and it tries to get a handle on the complexity.

## Document Structure

In order to achieve this, this document first does an analysis of the threats caused by the technology. This is the basis for the ten points to follow.


