---
title: "Crop Field Protection and Animal Intrusion Detection System"
excerpt: "An IoT system to prevent crop damage by animals"
header:
  overlay_image: /assets/images/crop-field.jpg
  overlay_filter: 0.5
  teaser: /assets/images/crop-field.jpg
  caption: "Photo credit: [**Henry Be**](https://unsplash.com/@henry_be)"
collection: portfolio
layout: single
toc: true
read_time: true
share: true
search: true
date: 2018-03-31
---
{% comment %}
T18:38:52+00:00
tags: 
  - sample post
  - readability
  - test
{% endcomment %}

## Introduction
The agricultural sector forms an integral part of every country’s economy. Its contribution towards gross domestic product of any country is undoubtedly significant. Agriculture meets the food requirements of people and produces several raw materials for industries. But due to animal interference in agricultural lands, crops get damaged, thereby causing a huge loss for farmers. To avoid these financial losses, it is very important to protect agricultural fields or farms from animals. Field surveys showed that on an average, 36% of the crop were damaged by wild animals. The incidents of damage were very high in crop fields adjacent to forest areas; this resulted into direct conflict between people and wild animals like boars. Hence arises the need for a reliable system to prevent crop damage.

## What it does
This system implements effective fencing methods by making use of sensors which consume low power. In case an animal enters the field, the sensors in the vicinity of the animal get triggered, alerting the farmer about the intrusion via a simple and interactive mobile application. At the same time, an unmanned aerial vehicle reaches the vicinity of the animal, and captures images of the intrusion. Image processing and machine learning techniques are used to recognize the animal which intrudes the field. Countermeasures are automatically deployed to a minimal extent to drive the animal out from the field.

## How it was built
* PIR sensors, paired with a network of XBee modules and ATtiny85 microcontrollers.
* A drone with the Ardupilot flight controller, with a Raspberry Pi + Camera setup and an ultrasound sensor.
* A TensorFlow script on Raspberry Pi using a pre-trained Inception image model, and a script making use of Google Cloud Vision API.
* An Android app connected to the Raspberry Pi a MQTT server, which monitors drone stats.
