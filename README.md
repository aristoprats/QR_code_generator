# Bulk QR Code Generator
Team members: Prats Mathur
## Table of Contents
* [Project Status](#project-status)
* [Project Purpose](#project-purpose)
* [Project Constraints](#project-constraints)
* [Technologies Used](#tech-used)
* [Cited Sources](#cited-sources)
* [Setup](#setup)

## Project Status
In development but deployed on pilot scale.

### To Do
* [X] Create a script that can convert any provided URL to a single QRCode
* [X] Modify script to take in multiple URLs and iterate over them to create unique QRCodes
* [ ] Fix up formatting on HTML side to attach assetname to QRCode in human readable format
* [ ] Beautify like....any of it

## Project Purpose
This project was created to generate a bulk amount of QR codes to make physical asset documentation easier to locate from an electronic database.

But don't plenty of web-services/pages exist that churn out QR codes for a nominal fee? Absolutely, in fact they probably run smoother and have far more polish than what this random college student can do.

However, I was given the specific constraint of our internal URLs shouldn't be leaving the local machine during this process for fear of being "hacked". (Let's take a moment and ignore the fact that if someone can hack a microsoft web server on URL alone we have much bigger problems).

Compounding this problem was a company wide IT policy which was...conservative... to say the least and wouldn't allow for running any local scripts or custom programs.

So that created a requirement for a quick script with the following specifications:

## Project Constraints
 
* Must convert a list of URLs into QR codes
* Conversion process must be clear to someone on site who's most advanced tools are excel and a browser
* URL data must not leave the local machine
* IT will block any apps/scripts run directly

## Technologies Used

### Java Script
    > This script actually runs as a pure JS implementation to ensure both ease of transfer between machines, convenient useage for technologically-lacking users and allowing an easy IT bypass without creating a large risk.

## Cited Sources

This script would not be as simple as it is without the following javascript modules:
### [XLSX] (https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.15.3/xlsx.full.min.js)
    > This is used to help parse out the input XLSX and extract the key-value pairs for each URL
### [JQuery] (https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js)
    > This is used to help attach the javascript into the HTML by directly handling the upload event
### [QRCodeJS] (https://cdn.rawgit.com/davidshimjs/qrcodejs/gh-pages/qrcode.min.js)
    > This is the main workhorse that converts a URL into QR Code objects

## Setup

None required! The single HTML file is all you need on any machine with a webbrowser.
Just download that one file, and have your excel data tabulated with the same headings as seen in the sample excel documents.