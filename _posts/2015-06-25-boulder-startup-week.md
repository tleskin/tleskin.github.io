---
layout: post
title:  "Tickling funny bones at the Quick Left Humor Hackfest 2015"
date:   2015-06-25 05:45:00
categories: coding
---

Being a student at [Turing](http://www.turing.io/) can be a roller coaster of a time for seven months. You have practically no free time to do anything else, hence why I'm writing this blog post about a month and a half late. You experience ups and downs, times when you feel like the best programmer in the world and other times you're doubting yourself and thinking this probably isn't for me. In my experience though, all the hard work pays off and you eventually get to a break between the six week modules, known as an intermission week.

Although these weeks are somewhat breaks, the burner is turned down only slightly and you still have pre-work for the next module to complete. During the last intermission week, it was lucky enough to fall on the same week as Boulder Startup Week 2015. For a student who will now be graduating in about 7 weeks (including the intermission week), this couldn't have fallen on a better time. It was perfect to try to get involved in the local startup community as well as to do some networking.

There were numerous events during BSW, but the one that sticks out in my mind the most was the Humor Hackfest hosted by Quick Left, a software consultancy on Pearl Street in Boulder.

It was the first time I had ever participated in such an event so I was both excited and nervous. If you're unfamiliar with what a hackfest is, it's not an event where you're trying to do something like hack the government, like you hear in the news involving China and the U.S., but an event where you're given a limited amount of time to try to "hack" together some kind of working app. In the case of the Humor Hackfest at QL, you were given about three hours to build an app around the theme "humor" or as the event description said, "create products — tech or otherwise — that help people learn and practice how to be funnier, thus enriching their lives and the lives of people around them." The only real strict rules were that you couldn't have built it before the event and it had to "work", so you needed to be able to present a working app.

Before the hackfest, I had been excited for the event for weeks and even started recruiting a team before hand, which ended up being my friends and fellow Turing students Eric Dowty and Patrick Medaugh, but we had no idea what we were doing to build. One of the ideas vetoed was an app that lets you receive emails from your favorite celebrities, such as Taylor Swift, who surprisingly some people people at Turing are obsessed with. We settled on an app that we called Trolio that let you spam your friends with random MMS messages.

![Trolio](/assets/img/trolio.png)

The thought behind Trolio was that just about everyone gets random texts from time to time from someone they don't know. Eric came up with the idea, which a lot of people really enjoyed and thought was pretty funny, where you could go to our app, enter a message, which we provided the default 'wish you were here!', enter a URL to an image, again a random default one is provided, then you enter a phone number and your friend (or person you're trolling) will receive a text with all of that information from a random rural Colorado phone number.

During the event we did our best to code as quickly and efficiently as possible, mostly working in pairs (yes, we do lots of pair programming at Turing). As soon as Rachel Scott from QL yelled "go!" after everyone got pizza and beer for dinner, it was a mad dash to your work area. I just remember it being a whirlwind to get started and also feeling the pressure of only having three hours to build our app. The advantage to pairing was that we had who brains what could write code twice as fast, that was also much cleaner.

The three of us had just come out of Module 2 at Turing, so our Rails skills were just starting to really develop, but we felt comfortable enough to be able to create a new project and implement what we wanted. One of the most challenging parts was one of the most crucial pieces of our app, integrating the Twilio API, which allows your app to make and receive phone calls and send and receive text messages. We had never used an API before, we actually just got really deep into using third-party APIs in the past six weeks at Turing in Module 3, but it only took us less than an hour to get it all hooked up.

As the time went on, we had our app mostly finished in about an hour and a half. A lot of the time afterwards was spent trying to get some CSS styling and to add additional features, but the most challenging thing was that we wanted to have an app in production so that people could use and visit our app even afterwards. With electronic music blasting in the background and time running thin, we tried everything and eventually got our app pushed to Heroku at the last minute. I can't remember what the issue was that were having, but thanks to some help from other fellow Turing students, we got it sorted out.

In the end, we got to present our app and although we didn't win, people did seem to love it. I remember reading on Twitter how someone mentioned our app was their favorite out of all the presentations so far. It also seemed to be the most favorited and retweeted out of all the apps.

![Group](/assets/img/hackfest.png)

Even before attending the Humor Hackfest, I got some advice from a Turing graduate that I should try to participate in as many 'hack-a-thons' as possible since it looks good to employers and many look for new employees at these sort of events. While that's probably true, I think participating in such an event shows that you're able to come up with an idea and put together some sort of implementation quickly. For anyone studying software development, Turing students or not, I challenge you to participate in at least one as it will give you a great assessment of your skills and show that you can think on your feet under pressure and time constraints. Some advice that I'd give, which could apply to any project, not just for a hackfest, is to use some agile practices and work in iterations. There's no way you're going to build the next hot fully fleshed out app in just a few hours, but the chances are you can build something that can be expanded upon later.

Besides that, just have fun and happy hacking!
