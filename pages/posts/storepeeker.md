---
title: "Project: Storepeeker"
date: 2023/09/15
description: A spy tool that helps sellers find top-selling Shopify stores and products.
tag: web, project
# author: You
---

import Image from 'next/image'
import Link from 'next/link'

*August - September 2023*


Storepeeker is a Shopify spy tool that helps sellers find top-selling stores and products. I built it in 6 weeks and got 60 business users before shutting it down due to a change in Shopify's endpoints.

[Go to project](https://storepeeker.com)

---

<Image
  src="/images/storepeeker.png"
  alt="Photo"
  width={1927}
  height={737}
  priority
  className="next-image"
/>

I wanted to build this because, after about 2 years helping Shopify sellers with their stores, I realized that the most common question I got was "What are the best Shopify stores to learn from?" This app answers that question.

First, I wrote a Node.js server to scrape data from Shopify stores, manage tracking lists, and generate sales reports. This took about 2 weeks.

I sent the reports over email to early users to get feedback.
<Image
  src="/images/email-example.png"
  alt="Photo"
  width={1436}
  height={1286}
  priority
  className="next-image"
/>

Some store owners shared thier actual sales figures with me so I could test the accuracy of the reports. I was able to get consistently within 10% of the actual sales numbers.

At this point, I felt like the concept was solid, so I built a web app to display the data and let users manage thier own tracking lists. I used with Next.js, Tailwind CSS, and a PostgreSQL db managed by Supabase. I ran most of the web scraping and data processing on a separate AWS EC2 instance using Flask/Python and Express/Javascript. One script had to be optimized so I rewrote it in Rust with the help of a friend. This all took about 4 weeks.

Features
- Track and get accurate estimates of any Shopify store's revenue
- Find the best selling products of any Shopify store
- Export any Shopify store's product list and other data
- See the most popular stores for a given niche

I launched on Twitter and got 100+ likes and 60 signups. I got a lot of great feedback and feature requests.

Then, tragedy struck. After hitting an undocumented Shopify endpoint at over 2,000 requests/minute for a few weeks, Shopify changed the endpoint to make it impossible for me to collect sales numbers. 

Not only did this break my app, it broke several other 'shopify spy' apps like dropship.io with millions of monthly users. I can't be sure that my app was the cause of the change, but it is possible. 

Since sales tracking was the flagship feature of the app, I decided to shut it down. At some point, I might rebuild it with a different approach to estimate sales numbers based on other factors.

I learned about the dangers of building on undocumented APIs. I also learned how to get a product to market quickly and get better feedback from real users. 

I shut down the servers so you won't be able to sign up but you can still check out the [landing page.](https://storepeeker.com)
