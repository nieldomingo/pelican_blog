Title: A Thought on OO Inheritance
Date: 2015-08-10
Category: object-oriented, random_thoughts

# Introduction

This post is inspired by a situation in my work. There was this
class that was reused by a particular module. However, the expected
behaviour was quite different which caused some problems. So to fix
the problem, a new class was written that implemented the expected
behaviour. A comment that came up is, "the new class should inherit
from the old class, right?". This made me think. I asked this
question years ago in a similar case and we decided that it wasn't
a good idea simply because that keeping the dependency to the old
code would make it harder to deprecate the old code. This appeared
to be also true, so I suggested that we do the
same. This made me think. It seems to be a very good idea from the
perspective of the object-oriented (OO) paradigm to inherit from the
original class. But after some thought I realized that from an OO
perspective, the right way should be to create a parent class and
make both classes inherit from that parent class. But whether that
class hierarchy is really necessary, I don't think so. I felt that
the use-case is really incidental. So even if its debatable, I think
not having the dependency is right and not creating an additional
class hierarchy is right.

This incident spurred me to think about the OO paradigm and also to
be retrospective about my history with the OO paradigm.

# Little Use of Object-oriented Paradigm

From the very start, I wasn't really a big fan of the OO 
paradigm. Not because I have extensive experience with OO and
experience to prove that it isn't really a very good idea, I
attribute it two things. First, is that I have used Python as my
main language for so many years and Python is very flexible when it
comes to which paradigm you use. I notice that most of the time
except for the use of objects from libraries, I primarily use the
modular approach. Another reason is that years ago, I read Eric S.
Raymond's Art of Unix Programming. It was really very insightful and
one of the things that it discussed is the failure of the OO
paradigm. If I remember it correctly, it said that OO is good for
some application domains like UI applications, otherwise it isn't
really a very good idea. But eventhough I didn't really used OO that
much, I'd like to say that I have a good understanding of its
basics.  Every now and then when I had to write libraries, I used
OO paradigms when it was really appropriate.

# Switch to Ruby, Started to Appreciate the Object-oriented Paradigm

This changed two years ago when I started delving into Ruby. First
was when I had to learn Chef to be able to use AWS Opsworks. I had
to learn a little Ruby to be able create custom cookbooks. This
exposed me to a language that strongly supported the OO paradigm.
After having worked with Python for so many years, it was really
refreshing. It was like looking at things from a different angle. I
also for a time fell in love with the poetic style of writing code.
I eventually dove deeper into Ruby when I joined a company which was
primarily a Ruby shop. To fit-in, I decided to go all-in and learn
Ruby. I didn't just want to learn to write code in Ruby, I wanted
to learn its idioms and paradigms. I didn't want to write Ruby code
that looked like Python. So before joining the company, I set out to
read Eloquent Ruby and Practical Object-oriented Design in Ruby. It
was really very interesting. I remembered years ago when I tried to
pick-up Java and compared its approach to the OO paradigm, it 
felt that Ruby's approach to OO was more accessible. From then on, I
embraced OO when developing in Ruby. It was a different way of doing
things and it seems to be a very good idea.

# Layers of Abstraction

I was working with Ruby for a few months and was completely
embracing the OO paradigm. However, I really was noticing some
issues. I felt that working with the code-base wasn't really as
pleasant as figuring out how something works always entails going
through the implementation of a lot of classes. To be honest, I
felt that it goes against a principle that I have embraced when I
was still working with Python, use thin layers. One of my gripes
when working with the code-base is, "its not abstraction, its
layering". But at the end of the day, its a team decision and I
think maybe its just me.

# Clojure, Simple Made Easy

I encountered functional programming years ago before it became
really, really popular. I fell in-love with the idea that it
inspired me to read and watch the SICP lectures. However, at that
time, I was too invested in Python. Python wasn't even that
mainstream at that time. PHP was sort of the thing. But because
Python supports some functional paradigms, I sort of just decided
to stick with Python and adopt a functional paradigm whenever it
was appropriate.
