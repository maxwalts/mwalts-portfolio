---
title: "Project: Area Liquor Printer"
date: 2023/06/01
description: A vertical SaaS for liquor stores in Michigan
tag: mobile, project
author: Max
---

import Image from 'next/image'
import Link from 'next/link'

*June - August 2023*

Liquor printer is a mobile app for the Area platform, which lets Liquor stores make orders, manage inventory, and update prices in their store using an associated label printer.

[Download the App](https://apps.apple.com/us/app/area-liquor-printer/id6460588987)

---

<Image
  src="/images/lp-preview.png"
  alt="Liquor printer preview"
  width={1927}
  height={737}
  priority
  className="next-image"
/>

This project was bootstrapped by an entrepreneur from Michgian, [Jake Lewin](https://www.linkedin.com/in/jake-lewin). The idea was validated by extensive customer interviews performed by the CEO and an operations hire in Ann Arbor. I was brought on to launch the mobile app and get us to our first paying users.

Features
- Scan a barcode on a bottle to pull up information on the product and send a tag to be printed
- Scan the QR code on a price tag to reorder an item


## Account management web app
My first challenge was to integrate Stripe and add account management for users. This was done by spinning up an EC2 to host a web app built with Vite, styled with TailwindCSS.

<Image
  src="/images/lp-homepage.png"
  alt="Liquor printer homepage"
  width={3024}
  height={1888}
  priority
  className="next-image"
/>

## Stripe API integration
more info to come

## Mobile app
The mobile app was build with React Native. The decision was made to not use Expo because we had to write a native module to enable communication between the app and our printer. The native module had to be written twice: once in Objective-C for iOS and once in Java for Android. 

I was surprised by how much of a challenge it was to get the app listed on the App store and Google Play store. There were many small changes requested my Google and Apple, like adding a privacy policy to our landing page. This by itself isn't an issue, but we were totally at the mercy of the 3-5 day cycle time of the app store reviewers.

<Image
  src="/images/lp-mobile-ss.png"
  alt="Liquor printer mobile app screenshots"
  width={892}
  height={894}
  className="next-image"
/>

more info to come 
