---
layout: page
title: Full Stack Application
description: An assignment to develop a prototype full stack web application for a client to keep track of their business operation
img: assets/img/1.-Initial-setup-with-ui-added.png
importance: 4
category: Learning
tags: .NET C# Cloud Database WebApp
github: https://github.com/NonIntelligent/full-stack-app
---

## The project

An optional university assignment that I chose to pursue to learn about developing web-apps using ASP.NET, as well as its deployment using Microsoft Azure. The task was to develop a prototype application to record the operational history of a company. Such as repair operations and equipment used.

## Implementation

I chose to use the Blazor framework as it’s good for building single-page applications. It also allows for C# code to be used alongside HTML and can replace JavaScript for development.

Microsoft Azure was used to deploy the application, the SQL database, and provide a secure connection between the client and server. Using the inbuilt functions of ASP.NET, secure user login details can be generated and stored as hashes on the database.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/log-in.jpg" title="Log in page" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

I added drop-down menus, input boxes and confirmation buttons for users to enter information about the operation to the database. These inputs create C# objects to contain the data and make it easier to send to the database.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/repairs.jpg" title="Data entry menu" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Challenges

As it’s my first attempt at developing a web-app, I spent a lot of time researching and learning about what functions I’m calling and what systems I need to implement. I followed the guides on Micorsoft’s own page to develop a web-app using ASP.NET and Blazor.

I also faced difficulty with the layout of components with HTML as they stacked horizontally. I’ve now learnt about differences between margin and padding as well as the HTML and CSS structure.

## For the future

I would setup the html elements with proper placements and good layout structure, or use a web builder to do the work for me.
Having the option to switch between a local connection and an online version would be very helpful for testing input data and functionality.

With the knowledge I’ve gained from this project, I can confidently develop web-apps and gain further understanding of the coding style and architecture.
