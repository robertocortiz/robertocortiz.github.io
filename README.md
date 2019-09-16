# Jarvis Home Automation

## Instructions Provided

A JavaScript application simulating house automation: pressing a button on a control panel would visually turn on a light, change the temperature or close the curtains. Some constraints:

* the application must use jQuery.
* the components must have HTTP based "server" interaction (use a static file for simplicity, data persistence is not required). For example, the heating component retrieves the current temperature from the server and also sends the desired one back to the server.
* the solution has to be extensible and documented, so that we can develop our own components that react to events.

The application will be executed on a plain HTTP server with no possibility to run code server side and is being viewed in 2 major browsers of your choice.

## Demo

The Demo is available [here](https://robertocortiz.github.io)

## Download source code

The source code can be downloaded from [here](https://github.com/robertocortiz/robertocortiz.github.io/archive/master.zip)

## Description of Project

This project was inspired by Mary Shaw's [Just Another Automated Home](https://github.com/marybeshaw/Just-Another-Automated-Home), Thomas Knochbloch's [Smart House](https://github.com/ThomasKnobloch/smart-house) and of course a lot of references within [Google's MDL docs](https://getmdl.io/started/), [W3Schools](https://www.w3schools.com/js/default.asp), [CodePen](https://codepen.io/), [jQuery Docs](https://api.jquery.com/on/)

The project implements the MVC pattern in order to be flexible and extensible, I've used the core functionalities from the above projects and updated aesthetics and javascript functions that I needed to achieve desired state.

## Floor Plan SVG

A picture of a house floor plan is being used to show the different states of the rooms.

The SVG format is great to be able to show and hide every part of the house plan.

Each `<g>` tag represents a room (identified by the room name) which gathers all the room objects (light, curtains and temperature display).

I had to break down the object and loop through the elements to be able to click on each room and bring up each corresponding menu

Then had to ensure all rooms were visible if Menu was selected

## Mock Server

The server-side is replaced by a static file (mock-server/house.json) that is used on read-only for the initial state of the application, which has all items turned off.

It contains a JSON object organized as follows:

```json
{
    roomName1:{
        propertyA: stateA1,
        propertyB: stateB1,
        propertyC: stateC1
    },
    roomName2:{
        propertyA: stateA2,
        propertyB: stateB2,
        propertyC: stateC2
    },
    ...
}
```

## Third-party libraries utilized

* jQuery: JavaScript library used to simplify the client-side scripting of HTML.
* Material Design Lite (MDL): Icons and CSS templates that helps to build fast, modern mobile-ready web apps.

Both libraries are retrieved from external CDNs hosted by Google

## Setup

This application can be hosted on a plain HTTP server. There is no server-side code needed.

I tested the application on Google Chrome, Mozilla Firefox and Safari for MacOS.