---
layout: post
title:  "What is printer nightmare"
tags:
    - netsec
    - summary
sources:
    - https://twitter.com/gentilkiwi/status/1415520478693888004
    - https://twitter.com/gentilkiwi/status/1416429891592011781
    - https://twitter.com/gentilkiwi
---

# Printer nightmare
Printer nightmare started as [CVE-2021-34527](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-34527) as a Remote Code Execution and Privilege Escalation vulnerability with a CVSS score of 8.8. The RCE vulnerability was fixed in security updates after July 6, 2021.

While these security updates fixed the RCE part of the vulnerability additional research has shown that the Privilege Escalation vulnerability has not been fixed for local users.

{% twitter https://twitter.com/gentilkiwi/status/1415520478693888004 %}

## Mitigation's
Currently the only mitigation is to restrict point and print to approved server as documented [here](https://admx.help/?Category=Windows_10_2016&Policy=Microsoft.Policies.Printing::PackagePointAndPrintServerList) and [here](https://docs.microsoft.com/nl-nl/troubleshoot/windows-server/printing/use-group-policy-to-control-ad-printer).

Additionally create additional firewall rules to prevent outbound RPC, CIFS and SMB traffic on either your edge routers or while working from home on the endpoint.

{% twitter https://twitter.com/gentilkiwi/status/1416429891592011781 %}

## Proof-of-Concept
Benjamin Delpy (@gentilkiwi) made a very simple user-to-system printer as shown in this tweet:

{% twitter https://twitter.com/gentilkiwi/status/1420069224106577927 %}

