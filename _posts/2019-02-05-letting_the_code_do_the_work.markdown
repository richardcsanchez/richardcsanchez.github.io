---
layout: post
title:      "Letting the Code do the Work"
date:       2019-02-05 20:01:57 +0000
permalink:  letting_the_code_do_the_work
---


 
As I've learned more coding languages and styles, one of the things that I appreciate the most is the way that code is logical and direct. While there are many ways to go about solving problems and building programs, a method has a clear function and processes data in an expected fashion.

Moving into Rails, one of the things I struggled with was abstracting my code, and not expliciting stating all of the steps. A huge of appeal of Rails is that there is so much built in functionality within the framework. However, in order to effectively utilize these almost magic functions, I needed to be able to see and understand what was happening 'behind the scenes'.

I found it really helpful to work backwards with my code. I would code in a more verbose way that was more explicit and detailed, and then go back to abstract and simplify it. This not only helped me to understand what the mre abstract code was doing, but also allowed me to be more precise with my code. Having more precision was helpful in creating my nested routes, and specifying what each view was presenting to the user. It was useful in creating the ```before_action``` and ```helper_methods``` that simplified my controllers and shortened my methods. By abstracting my logic and shaving down my functions to be streamlined I was able to create a sleeker, more readable application. 

Setting up my third party login system through Omniauth Facebook was a challenge, and I ended up with a lot of unecessary code and logic in my controller. By abstracting the different elements of the process, and separating the request for information in the controlller and the actual processing of information in the model, I was able to clarify my separation of concerns and create a skinnier controller.
