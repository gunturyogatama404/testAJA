# Linux SDK Integration Guide

- [Linux SDK Integration Guide](#linux-sdk-integration-guide)
  - [General](#general)
  - [Prerequisites](#prerequisites)
  - [Step 1:  Select the program corresponding to the CPU architecture.](#step-1--select-the-program-corresponding-to-the-cpu-architecture)
  - [Step 2: Assign read, write and execute permissions to the owner, group and other users of the program.](#step-2-assign-read-write-and-execute-permissions-to-the-owner-group-and-other-users-of-the-program)
  - [Step 3:  Start the program using the appkey.](#step-3--start-the-program-using-the-appkey)
  - [Step 4:  Verify if integration is successful.](#step-4--verify-if-integration-is-successful)


## General
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This guide is for developers who want to monetize Linux applications with Packet SDK.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Integrating the Packet SDK into an application is the first step toward earning revenue. Once you've integrated the SDK, you will start seeing devices data and revenue in [Packet SDK Dashboard](https://dashboard.packetsdk.com) in 24 hours.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This document will walk you through the steps needed to be taken in order to properly integrate Packet SDK into your application.


## Prerequisites
- Create an app in [Packet SDK Dashboard](https://dashboard.packetsdk.com) and obtain the corresponding **app_key**. 'app_key' is an important way to track your earnings, please ensure it is set correctly in the subsequent integration steps.
- Download the Packet SDK Linux integration package `packet_sdk_linux-1.0.*.zip` and unzip it.
Once you unzip the package, you can see the following contents:
packet_sdk_linux-1.0.*.zip
&nbsp;&nbsp;&nbsp;&nbsp;├───x86_64(amd64) &nbsp;&nbsp;ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), static-pie linked, stripped
&nbsp;&nbsp;&nbsp;&nbsp;├───Intel 80386 &nbsp;&nbsp;ELF 32-bit LSB pie executable, Intel 80386, version 1 (SYSV), static-pie linked, stripped
&nbsp;&nbsp;&nbsp;&nbsp;├───aarch64 &nbsp;&nbsp;ELF 64-bit LSB pie executable, ARM aarch64, version 1 (SYSV), static-pie linked, stripped
&nbsp;&nbsp;&nbsp;&nbsp;├───armv5l &nbsp;&nbsp;ELF 32-bit LSB pie executable, ARM, EABI5 version 1 (SYSV), static-pie linked, stripped
&nbsp;&nbsp;&nbsp;&nbsp;├───armv6 &nbsp;&nbsp;ELF 32-bit LSB pie executable, ARM, EABI5 version 1 (SYSV), static-pie linked, stripped
&nbsp;&nbsp;&nbsp;&nbsp;└───armv7l &nbsp;&nbsp;ELF 32-bit LSB pie executable, ARM, EABI5 version 1 (SYSV), static-pie linked, stripped



## Step 1:  Select the program corresponding to the CPU architecture.
- You can use the `uname -a` command to view the CPU architecture of Linux devices.
- You can use the `file packet_sdk` command to view the architecture of the PacketSDK executable program.

<blockquote style="font-size: 16px; padding: 0 8px; border-left: 5px solid #0969DA;">  
    <p style="margin-bottom: 0;"><strong style="color: #0969DA;">Note</strong></p>  
    <ul style="margin-top: 0;">
        <li>If you need Linux PacketSDK with other CPU architectures, please contact our customer service personnel.</li>  
    </ul>  
</blockquote>

## Step 2: Granting read, write, and execute permissions to programs.
  ```
  chmod 777 packet_sdk
  ```

## Step 3:  Start the program using the appkey.
  ```
  ./packet_sdk -appKey=YOURAPPKEY
  ```
<blockquote style="font-size: 16px; padding: 0 8px; border-left: 5px solid #0969DA;">  
    <p style="margin-bottom: 0;"><strong style="color: #0969DA;">Note</strong></p>  
    <ul style="margin-top: 0;">
        <li>Packet SDK Linux executable program don't have the function of auto start and keep alive, you need to set it yourself.</li>  
    </ul>  
</blockquote>

## Step 4:  Verify if integration is successful.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;When you receive "This device has been successfully certified" in the console, it indicates that you have successfully started the Linux Packet SDK.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;You will start seeing devices data and revenue in [Packet SDK Dashboard](https://dashboard.packetsdk.com) in 24 hours.

