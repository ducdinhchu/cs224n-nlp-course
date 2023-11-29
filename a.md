Welcome back in this chapter, we are going to create a world
map with our most popular end stations plotted just to recap
on the data.
This data is taken from Citi bike nyc dot com city bikes
provides bicycles in New York City, and the data
we're looking at is from the month of February 2018.
This data shows us where the city bikers, right when do the
right with stations are most popular and so on.
We have different measures and dimensions.
Different measures like end station ID, the end station
and start station, geo location, data and so on.
And we have dimensions like Berthier, the names of stations
and user type and so on.
Making maps and charts and tableau is very simple.
A lot of the data type that tableau detects automatically
actually tells the software what kind of plots can
potentially be created with that kind of data.
And you can see this Show me menu in the right side.
So if you hover over any of these, uh, different kind
of plots at the bottom, it will show you what kind
of dimensions and how many dimension measures are required
to create this kind of a plot.
So if I use latitude and then use longitude on this canvas,
then we will be able to create a world map.
We're not going to use this preset right now, so I'll just
click on, show me to hide this menu and all we are trying
to do here is a look at the end station, longitude
and latitude and basically drag and drop them
onto this canvas to create a World Bank.
All right, so let me start by dragging and dropping
this latitude, you can put it on either rows or columns.
I'm gonna put it on Rose and then launch it.
You're on columns.
Great. So when we use these two measures as our column
and row, respectively, we automatically get a word map.
We don't have to select anything.
We just get this automatically and you can drop any data
at multiple places in a canvas, and it will try to plot
the data in the most meaningful way.
So now the big get a world map.
The problem right now we have is that it's showing us only
one location on the map this dark right here.
This location is the average of all the latitude, values
and average of all the longitude values instead
of the average values.
What we are looking at is to actually plot all the end
stations separately.
So if you click on the little drop down icon right here,
where it is average and station latitude and instead
of measure select dimension, we will get all these different
end stations plotted.
We can do the same thing for our columns, which has longitude.
Great. Now, if you want to change the size of these dots, you
can do that by going to marks click on size and just dragging
and changing the size with this slider.
Now, most of the end stations are right here, and there's
one up here.
This might be an anomaly.
It doesn't really seem right.
But what we are looking to do is we are looking to filter
to find most popular end stations.
In order to do that, you have a filter section
above the marks section, and we can use this to create
different kind of filters to select different kind of, uh,
measures that we might want.
So what we are looking for is to find the most popular
and stations.
In order to do that, we're going to look at this
automatically generated field, which counts the number
of records.
So if I drag and drop this on filters, it will ask us, how do
you want to filter on number of records?
So we are looking at this sum total of these values from our
records.
So we're looking at at least stations which are at least
5000 records.
Let's say so.
The maximum value here is 9060.
So we're looking at stations which have at least 5000 number
of records take okay.
And this will figure out a lot of these stations which are
not very popular and what were left dead.
Here are a few of these stations, but only the ones which are
popular.
Let's zoom out of this map a little bit, David.
Go. So now we have the most popular and stations on this plot.
We're going to do the same thing for our start stations and
will also create other kind of plots in the following
chapters.
See, you guys think.
