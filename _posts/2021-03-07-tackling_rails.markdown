---
layout: post
title:      "Tackling Rails"
date:       2021-03-07 22:22:35 +0000
permalink:  tackling_rails
---


While I really found my stride with the Sinatra project, for some reason Rails brought me right back to overthinking and self-doubt. But at the end of the day, anyone who's made it this far in the program is capable and I knew I could get through any problem that popped up... and it seemed like there were many!

For starters, I found myself overthinking the use of the join table. I also saw it as a passive participant in my app, rather than a tool to be used. 

I also got stuck on silly little things that turned into big lessons, such as nested route paths needing two arguments (if you give it just one, trust me, your routes will be all kinds of wonky).

One of my biggest challenges ended up being my nested form. My app is meant to be used as a way for hand lettering artists to track their projects and tools they've used. I struggled with getting my associations to form properly and to be able to create the parent and child at the same time (who doesn't love a good associations challenge??). At the end of the day this is where using the join table object (ProjectsTool in this case) came in handy as being an active part of this app. I created a nested form for a new ProjectsTool object, with a nested attribute for the Tool that would be associated with that new object (via its tool_id foreign key). 

Overall, this project was challenging, yet fun, and I feel like I learned the most throughout the process of creating this app versus the previous two projects. I honed in on my Rails Google search abilities and I'm proud of my problem-solving skills and ways in which I was able to adjust and make things work.

