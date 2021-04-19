---
title: "HeartCare"
excerpt: "A real-time heart rate monitoring system"
header:
  overlay_image: /assets/images/heartcare-fullres.png
  overlay_filter: 0.5
  teaser: /assets/images/heartcare.png
collection: portfolio
layout: single
toc: true
read_time: true
share: true
search: true
date: 2017-07-31
---
{% comment %}
T18:38:52+00:00
tags: 
  - sample post
  - readability
  - test
{% endcomment %}
Created and designed by Kishore Ravisankar, Muhammad Irthifa Khan and Anuroop Reddy Adala.

HeartCare is a system that gives a user real-time ECG readings. The app is connected to a Genuino 101 circuit which consists of an ECG sensor and a GPS module, via a MQTT server. The Genuino 101 uses a ESP8266 module to transmit the ECG values and the patient’s location to a server. The app obtains the values from the server and displays a real time graph for the patient and doctor to monitor the heart rate.

This was submitted as one of the entries for Intel Hacks 2017.

## HeartCare in Action
{% include video id="EQ5KGW4X5Ko" provider="youtube" %}

## Inspiration
One of the team member's grandparent had undergone a bypass surgery. Post surgery, he had to be placed under constant monitoring because of the delicate situation. Since it was close to impossible to have any individual under a constant monitor and since not everyone can afford a nurse or a doctor, we realised that there was no mobile solution in the market that was effective enough to monitor the health situation of an individual. That's when we came up with the idea.

## What it does
HeartCare is an system that gives any user real-time ECG readings. An Android app is connected to a circuit which consists of an ECG sensor and a GPS module, which is interfaced with the Genuino 101. The Genuino 101 uses the ESP8266 WiFi module to transmit the ECG values and the patient’s location to a server. The app obtains the values from the server and displays a real time graph for the patient and doctor to monitor the heart rate. The ECG sensor is what sets apart the HeartCare system from other similar products in the market, because the ECG signal is accurate.

## How we built it
We used an AD8232, a GPS module, Arduino 101, ESP8266, Android studio to develop the app, a web console for uploading data to server (cloudmqtt.com)

## Know more
Visit [this link](https://devpost.com/software/heartcare-qfj0rs) at Devpost to know more about the hack.

## Check it out
The code can be viewed [here](https://github.com/falcon97/HeartCare).
