# DEV161 - Develop Applications from Start to Finish Through LCNC and SAP AppGyver

[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/teched2021-DEV161)](https://api.reuse.software/info/github.com/SAP-samples/teched2021-DEV161)
[![Not Maintained](https://img.shields.io/badge/Maintenance%20Level-Not%20Maintained-yellow.svg)](https://gist.github.com/cheerfulstoic/d107229326a01ff0f333a1d3476e068d)


## Description

This repository contains the material for the SAP TechEd 2021 session DEV161 - Develop Applications from Start to Finish Through LCNC and SAP AppGyver and is provided as-is.
We will create an application with the new Low-Code perspective of the SAP Business Application Studio and additionally add a digital touchpoint as a mobile application using SAP AppGyver.

## Overview

This session introduces attendees to the new SAP Business Application Studio perspective for Low-Code development. Also we will cover the basic app development using SAP AppGyver.

## The use case

The use case we cover in this sesssion is that we implement a solution for a new start-up which enables customers to book superheroes for their birthday parties, team meetings or for support in your fight against the local neighbourhood villian.
For this we need to provide a way to store our business data: available heroes to rent, customers and bookings. At the same time, we have different users we need to care about: the backoffice users, who maintain the list of heroes we have under contract as well as to get insights into the orders. On the other side , we have the customers who should use our mobile-first approach and should be enabled to browse our catalog of heroes as well as place orders.

## Requirements

Local requirement is to preferably use the Google Chrome browser to access the SAP Business Application Studio and SAP AppGyver. You will get dedicated users for login to the development environment during the course.
Other than a modern browser, there is no local installation needed.
Please use the incognito mode of your browser as we will distribute SAP Universal ID login credentials for you to use during the session and they might conflict with existing logins of your SAP ID user you have already in use.

Note: After TechEd 2021, users can use the content in this repo on their productive SAP BTP environment.

## Exercises

The exercises are divided into two parts. In part one we use the new Low-Code perspecitive in the Buesiness Application Studio to create an API service including persistence on SAP BTP. This includes already some applications for the backoffice users using Fiori Elements. In part two, we will create a mobile app for the consumer of our service.

## PART 1

- [Getting Started - Preparation Part 1](exercises/ex0/README.md)
- [Exercise 1 - Create a back-end application with Low-Code perspective in SAP Business Application Studio ](exercises/ex1/README.md)
- [Exercise 2 - Create an API (Service](exercises/ex2/README.md)
- [Exercise 3 - Add some sample data](exercises/ex3/README.md)
- [Exercise 4 - Add Your First App](exercises/ex4/README.md)
- [Exercise 5 - Preparation for Mobile App and Deployment](exercises/ex5/README.md)

## PART 2

- [Getting Started - Prepartion Part 2](exercises/exPrep/README.md)
- [Exercise A - Create a new AppGyver Project](exercises/exA/README.md)
- [Exercise B - Create a Data Source](exercises/exB/README.md)
- [Exercise C - Create the Pages/UX](exercises/exC/README.md)

Start the exercises [here](exercises/ex0/README.md).

**IMPORTANT**

## Appendix

Technologies and tools used in this course:

- SAP BTP, cloud foundry environment
- SAP Business Application Studio
- SAP AppGyver
- SAP Launchpad service (HTML5 Repository)
- SAP Workflow Management
- SAP HANA
- CLoud Application Programming Model (CAP)
- SAP UI5 and Fiori Elements

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed.

## License

Copyright (c) 2021 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
