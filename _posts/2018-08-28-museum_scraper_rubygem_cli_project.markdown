---
layout: post
title:      "Museum Scraper: RubyGem CLI Project "
date:       2018-08-28 18:48:19 +0000
permalink:  museum_scraper_rubygem_cli_project
---


Starting the first big project for the Flatiron Curriculum was definitely a challenging moment. This was the first time I was required to cover all aspects of my code, including setting up files, creating a git hub repository, and figuring out exactly what I was going to be creating!

I knew that I wanted to scrape some sort of art related website. My first thought was to scrape the Metropolitan Museum of Art's website to get all of the works by a specific artist or for a specific time period. However, as soon as I started to map this out I was reminded about how vast and complex the Metropolitan Museum's collection is and realized that I needed to consider what were my current capabilities. In a similar subject area, I decided to scrape Condé Nast's Traveler's Best NYC Museums. My goals were to condense this lenthy web page into a simplified list and have the user select which museum they wanted to know more about.

For me the hardest part of starting this project was figuring out how exactly to get everything up and running so I could even begin coding. When we covered GitHub earlier in the curriculum I knew that i would have trouble with it, but luckily one of my fellow students had written a blog post details the basics of getting started in GitHub. Once I had the repository set up, I was able to map out the necessary files I would need and thing about the different classes I needed. 

To start I set up the three classes I would need: ```Scraper``` which retrieves the data from the CN Traveler's web page, ```Museum``` which stores and allows the program to access the information for each museum, and the ```CLI``` which sets up the interactive portion of the program, asking the user for input and allowing them to learn about NYC's top museums. 

I started with the ```Scraper``` class becuase it was the one I knew would take the longest to figure out. Setting up the scrape in the code and finding where the information was stored in the webpage was acually pretty straightforward, but when I built out my ```CLI``` a bit to test my scrape, it would only return an empty array. By digging around through some blogs I came across the ```HTTParty``` gem that was able to help me pull and inspect the information from the website. 

After I got my scraper off the ground, coding my ```Museum``` class was pretty straightforward. I knew I had to initialize my Museums with a hash of attributes: Name, Description, Museum URL, as well as save them in an array so they could be saved and accessed. After the page was scraped and the museums were put into an array, my ```create_from_array``` class method takes in array of hashes and iterates over them to create new individual museums.

I had the most fun going through my ```CLI``` class and designing the user interface. Trying to create a dynamic set of loops with user input and information output was challenging but very rewarding. Building something that has a tangible user output is very satisfying and I enjoy mapping out how the user will interact with my gem.  

Ultimately, I am pleased with the outcome of my project. I really tried to focus on clean coding and making sure each class had a singular responsibility. I also set myself up to be able to expand on my current code and go a level deeper. I wanted to make sure that I had a clear understanding of what I was doing and was able to perfect my current program, so I didn't go as deep as I would've liked, but in the future I would like to scrape each of the museums profile page, and provide more information about these museums, including their hours, address, etc. 


