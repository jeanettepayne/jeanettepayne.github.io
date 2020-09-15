---
layout: post
title:      "My CLI Build Experience"
date:       2020-09-15 22:52:37 +0000
permalink:  my_cli_build_experience
---

I'm not going to lie - this was intimidating for me. It's clearly one thing to complete tasks and labs, read lessons and watch lectures, but another thing entirely to create a working program from scratch.

The hardest part of this project for me was just getting it off the ground. I know it will take time and repitition to get the structure setup down, but I'm already much more comfortable with the process after being pushed out of the nest and forced to fly on my own. 

From there, it was time to really hone in on my app, its structure, and how to make it function. 

I'm an overthinker, and this was no exception. 

I decided to pull from an API, another opportunity to learn from trial by fire, as I'd never worked with an API before. The one I used is laid out pretty nicely, which was great to work with, and is essentially a massive hash of makeup products. Hundreds and hundreds of makeup products.

Originally the plan was to give the user a list of makeup categories (blush, eyeshadow, etc.) that they could choose from, then that the user could sort that category by brand, price categories (that I would be creating), or rating. I ended up way overthinking that process and creating excess classes that were completely unnecessary (classes for brand, price, and rating), then reeling myself back in. 

I also realized that a lot of products don't actually have a rating listed, which would cause issues in regards to pulling by top rated products. I didn't feel that would give the user the true best products and the best options overall.

I decided to pivot and just allow the user to choose a product category, then get the list of those products (product name, brand, and price). From there they have the option to get the full description for any product in that list that they may be interested in.

I think this pivot allowed me to really hone in on the process and coding rather than trying to clean up a messy pass-around that I was overthinking.

One interesting issue I ran into that I had fun figuring out the solution for was that when I went to create the method to put out a list of specific products in a given makeup category, I originally used each.with_index, then interpolated the "puts" method to put out the index and product information. This gave me the product's index within the larger list of every makeup product. I ended up ditching the index and using a counter as I iterated over MakeupSelector::Makeup.all to pull the products matching the selected category. Yay! Now I have a nicely numbered list.

I thought that fixed all my problems, and the program seemed to be running well, but I noticed that my method to select the specific product for which to grab the description was, again, pulling from the larger selection of all products, so the number entered was pulling the index number rather than the list number. I realized I needed to create a new array of only products pulled for that specific list, so I created an instance variable set equal to an empty array, then pushed each product in the selected category into that array. I then used that array's index to allow the user to select the product they're interested in, giving them the correct product description. 

Overall, while frustrating at times, I'm extremely proud of myself and the CLI app I created. It feels great to have built a functional program from the ground up, and it was a great learning experience.
