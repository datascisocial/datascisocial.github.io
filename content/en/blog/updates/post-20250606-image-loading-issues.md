---
title: "Image loading issues"
date: "2025-06-06T08:10:00+01:00"
description: "We had temporary image loading issues for around two days"
tags: [outage]
---

As [announced yesterday](https://datasci.social/@mszll/114624016346626261), we had some image loading issues in the last two days, where some images did not load, and images could not be added to posts. By now, the problem has resolved itself automatically - thank you for your understanding.

The reason for this outage was the migration to a more stable provider to avoid [full outages like the last one in April](https://community.datasci.social/blog/2025-04-20/10h-server-outage/): An additional cache for images was added that also stores the data in an efficient manner, but due to the large initial load some of its requests were timing out to the backend. To resolve this quicker, our server admins were increasing the timeouts, and were also manually pushing data into it so it had data before the initial request.