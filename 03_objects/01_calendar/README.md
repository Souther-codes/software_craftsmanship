# Objects

Variables in computer programs track data. We saw some of the kinds of data they
can track in chapter 1. In chapter 2, we saw how computers can use variables to
track calculations across a number of functions. Whether this is as internal
variables to remember an intermediate result, in arguments to take or pass data,
or in return statements to hand data back the the caller, variables are integral
to making programs work.

Sometimes, though, we want a bit more structure than what we can get just from
naming them differently. What we want as programs get complex is a way to bundle
several related variables together. In this way, we can treat them as a single
entity in our program. We can create them once, modify each part individually,
and keep the whole thing together when passing it to another function. This also
helps understanding - rather than talking about an area a width and a height
which we keep in our heads as being about one rug, we can instead talk about a
single rug, which has an area, a width, and a height. It may sound pedantic, but
in practice it really makes tracking complex pieces of data much easier!

These bundles of data are called **objects**. Each piece of data bundled into
an object is a **property** on an object. We can think of objects having
"shape" or "structure" based on what properties it has on it, and the types
of data that are stored in those properties. A property is, in many ways,
just a variable that is attached to a single object in our program. The
property has an **identifier** and stores a **value**. It's just that it can't
appear alone, and only is part of the object.

As we work with objects, these pieces of data with many facets, we often want to
talk about their "structure" or their "shape". For simple data, in the last two
chapters, we talked about the type of a value. It could be a number, a string,
or a boolean. For complex data, the type of the value is described by its shape
or structure. "Shape" and "structure" in this context describe the properties on
an object, and the types of values that go in each of those properties. Let's
consider a date for a moment.

Usually, we write a date in one single block - 2020/08/12. We might consider
using a string to hold the 10 characters. But when we think about the date
again, we often want to think about the parts of the date itself. What year is
it in? What month? Which day of the month is it? With only strings, we would be
required to do some sort of matching and conversion, like "for the month, take
the 6th and 7th characters, and convert them to a number." With the concept of
objects, we would instead store each of those pieces separately. Instead of
using a variable to store the single value `"2020/08/12"`, we can use an object
to store three properties - `year: 2020, month: 8, day: 12`.

The structure of this complex data object has three properties, year, month, and
day, each of which have type number. We can call this structure of three
properties with these names the **type** of the data object. We've now created a
new data type, beyond what the programming language originally provides. Instead
of working with a combersome single string, or needing to lug around three
variables with numbers, we can create a single Date object and it has all the
pieces we need to do calculations on a date as a whole.

A definition of a complex object like this is called an **interface**. It is the
public description of what the object is, the full description of its shape.

An object is a value, which means you can assign it to a variable. You can pass
it to a function as an argument. You can even assign an object into a property
of another object! Building out complex objects like this is how we'll later
begin building **data structures**. That's a couple chapters away - in the mean
time, just keep in mind objects being a bundle of related data, each piece of
which you can access from its properties. Let's get some practice looking at
dates, objects which store information about a moment in time.

[Python](./01_python.md)