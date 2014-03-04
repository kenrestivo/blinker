# blinker

Blinking binary counter LEDs as a tool for teaching the concept of place value in math to kids.

## Usage

The [live version is here](http://restivo.org/blinker).

It's best to run the app in a group, on a large screen, and have them all shout out counting as they go along. But the goal is for it to work on mobile too.

## Building

1. Download react-0.9.0.js and dump it into the cache/ directory. I frequently have flaky internet so I wanted it local instead of on CDN.

2. Use lein cljsbuild to build the javascript, and load the page.

3. index-dev.html is the development page, index-rel.html is the release page.
   You can make an alias to them if you like.

## Why???

About 5 years ago, when my daughter was in 2nd grade, I was aiding in the school's computer lab. My daughter's teacher was lamenting the difficulty of getting the kids to internalize the concept of place value in math. The kids had already become so adept at decimal, that the rhythms of counting by ten were deeply ingrained; they didn't get the concept of place value because numbers just did what they did, and that was the natural order of things. Do fish know what water is?

To try to break them out of that, I solderless-breadboard'ed up a little binary counter out of an Atmel ATTiny12 part and some LEDs, brought it in, showed it to the kids, and challenged them to try to count along with it. As they did, something pretty amazing happened. The rhythm of the counting was "all wrong", and the kids started to viscerally feel it. Instead of shifting at tens, it was shifting at powers of two. They were holding on at "niiiiineeee..." waiting for the ten, but the lights were making the big shifts at eight and sixteen instead-- ten was a non-event. Several of the kids attained enlightenment at that moment (and a few of the grownups too). I promised the teacher that I'd either build or write one for her to use in future classes.

Rather than build a hardware counter unit, since kids today are all about apps, and so that other teachers could use it too, and so that it could use bigger "lights" so a whole class could see, I figured it'd be best to have a webapp to do the counter. The project sat on the shelf for years. When I started playing with Clojurescript I decided I wanted to do use that, but couldn't find the time or energy to work on it. Finally, while trying to teach myself OM and React, and searching around for examples, I located a [binary clock](https://github.com/fredyr/binclock) in OM and started experimenting with it. It was similar enough to what I wanted that there really was no longer any excuse. After a few experiments and false starts I gutted the tutorial and started this instead.

## License

Copyright © 2014 ken restivo <ken@restivo.org>

Based in part on the [binary clock app](https://github.com/fredyr/binclock) tutorial.

Distributed under the Eclipse Public License either version 1.0 or (at your option) any later version.
