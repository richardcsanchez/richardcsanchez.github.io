---
layout: post
title:      "Building a Database "
date:       2018-11-17 15:44:53 -0500
permalink:  building_a_database
---


One of things that sparked my interest in coding was when I was trying to find archival databases for my current job, at an art gallery. All of the databases that I found met some, or most, of my needs, but none had all of the flexibility and organizational modes that I needed. When I moved on from the Ruby section of the curriculim into SQL and databases I was excited to begin this new section. immediately I could see how the functionality could be helpful in peristing data, and how it could connect with Ruby's data manipulation to possibly build an archival application.

I knew I wanted to create a more simplistic version of art website database that I could eventually build upon. My intial hurdles were really understanding the associations and tables that I would need to not only capture the information, but also be able to sort it, and catagorize it. The application would need to be accessed by a User, in this case the "Collector," and store works of art with their relevant information, (Title, Artist, Year, Genre, Medium). Through these artworks, I wanted to be able to connect the Artist and Genre, and allow the Collector to view their artworks sorted by Artwork, Genre, and Artist. 

Another goal of mine was to focus on the privacy of the user, and ensure that each Collector's collection was visible only to them. Associating the Artwork as "belonging to" the Collector was an obvious choice and solved this issue. However, I also wanted the Artists and Genre's associated with the user to remain private and unique to the user. If one Collector has a Picasso (good for them!), another Collector shouldn't be able to see that Artist was part of the database. Similarly, if one Collector had a drawings, and another Collector had photographs, then it would be relevent to show one Collector the option to organize by Photographs or vice versa.

I thought this project was a very interesting way to connect my interests and experience in both the art field and coding and I genuinely enjoyed solving the challenges that I faced. To expand on this project in the future, I would like to create more dynamic connections between classes and store more information about the Artwork. In tandem with this, I would like to be able to sort and organize the Artwork in more ways, so the user could better narrow down their searches. My gallery currently has almost a thousand works, so ideally you could narrow them down by what show they were purchased, or what year they were made or purchased, or which materials were used in creating these works. Additionally, more information could be stored about each artist, such as their exhibition history with the gallery, contact information, and their associated genres, movements, and materials. 
