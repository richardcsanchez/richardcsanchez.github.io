---
layout: post
title:      "No Coder is an Island"
date:       2018-08-14 22:05:29 +0000
permalink:  no_coder_is_an_island
---


One of the attractive aspects of coding is that I always imagined it to be a mostly solitary experience and that it would require me to independent, self-starting, and resourceful. 

Spoiler Alert: it does require those things. However, it's much more fun and interesting when you're working with a team.

I was not expecting to find such value in Pair Programming exercises and I've come to really see the value in them. Having to explain code, and extapolate on my logic, to another person has been a strong tool for checking my knowledge and building my confidence. 

Over the course of doing the labs and code-alongs in the Learn.co Curriculum, there has been a lot of overlap and repeated motifs through the different labs. It is very easy to copy and paste previous code and adapt it to the current lesson or lab to get at least some of the tests passing. I think this is a perfectly valid way of building code and as Avi often says in his lectures, programmers are a bit lazy like that! But the experience of having to go back and explain those choices in a pair programming session has been extremely effective in making sure I am still retaining the concepts and logic in the reused code. In other words, I know this code works because it has worked in a previous program, *but can I explain why it's working now or how I changed it?* 

Another added benefit of pair programming is being able to see another person's logic and approach to the same problem or bit of code. So far, I haven't been that adventurous in my coding; I tend to overcode at times so I've been focusing on keeping my coding simpler and sticking to exactly what the tests are guiding me to do. In a pair programming session reviewing the OO-Triangle Lab, my pair suggested constructing a completely separate method for testing for the validity of the triangle, outside of the asked for method determining the Triangle's Type. By separating the methods, it was that much clearer when to raise a custom error and my logic was that much clearer.

I've included a clip of the resulting code below.

> ```
def valid_triangle?
  (@a+@b > @c) && (@b+@c > @a) && (@a+@c > @b) && @a>0 && @b>0 && @c>0
	#This covers the various requirements that every triangle *must* have in order to be valid: each sides must be greater than 0 and the sum of any two sides must be greater than the third side.
  end

  def kind
    if self.valid_triangle? != true
      raise TriangleError
			#The rest of the code covered the various configurations that would lead to a triangle being classified as an   Equilateral, Scalene, or Isoceles Triangle.
		end
	end
```

In spite of my expectations, I've gotten a lot out of Pair Programming. But there are some times when no one is available or I'm just not in the mood to chat/interact with other people. Taking inspiration from Andrew Hunt and David Thomas's The Pragmatic Programmer, I've adoped my own version of Rubber Duck Debugging. I hopped on the cryptocurrency trend and purchased a Cryptokitty, a sort of online Beanie Baby that have different generations with the earliest generations going up in price. I find myself debugging with the Cryptokitty and confiding my progamming woes to it when I'm trying to work through a particularly challenging bit of code. 

![](https://www.cryptokitties.co/kitty/854796)



