What is Geocode?
=================

Intro to Geocoding Session for Mozilla Festival 2015; no 40,000 word special issue needed.

## Faciliators:
* [Stuart Lynn](https://github.com/stuartlynn)
* [Aurelia Moser](https://github.com/auremoser)
* [David Riordan](https://github.com/riordan)


## Outline:

### You are [here](http://www.ravensbourne.ac.uk/).

![ravensbourne](http://i.imgur.com/GnCgVH7.jpg)

If you were asked where you were, you might say Mozfest or Ravensbourne:

> 6 Penrose Way, Greenwich Peninsula, London SE10 0EW, United Kingdom

But if I wanted to describe the location as a point on a map, I might describe the same location using latitude and longitude:

> 51° 30' 6.25" N, 0° 0' 19.94" E

It reads as "51 degrees, 30 minutes and 06.25 seconds, 0 degrees, 0 minutes and 19.94 seconds"

We describe locations with a [spatiotemporal notation](https://en.wikipedia.org/wiki/Longitude_(book)), it's also somewhat obscure. So let's describe the same place using longitude and longitude but using decimal degrees instead of minutes and seconds. There are a number of conversion tools available online to do this:

> 51.501736, 0.005539

In general [addresses be crazy](https://www.mjt.me.uk/posts/falsehoods-programmers-believe-about-addresses/), a geocoder can sort out some of the incongruencies between human and machine-readable location information.

### Why are geocoders necessary?

- Translate from the world of human-recognizable addresses + names => coordinates (e.g. latitudes and longitudes)
- Convert an address to "referenced coordinates"

**Considerations**

- Anything you might want to compute about place uses coordinate data, which computers can easily understand, as opposed to these addresses
- Addresses aren't computable, and (for our purposes at least) aren't map-able

### What do geocoders do?

**What's an address then?**

	- Identication + References
	- Used to identify a place and provide enough information to route to there (with local context or knowledge)

**What are coordinates?**

	- Latitude + Longitude

### How are geocoders done?

* [CartoDB Academy Account](https://cartodb.com/signup?plan=academy) - geocoding credits and free space
* [Pelias](https://mapzen.com/pelias) - open source geocoder by MapZen
* [CSV geocoder](https://github.com/veltman/csvgeocode) - a map project by Noah Veltman
* [GeoCodio](http://geocod.io/) - geocoding as a service

### Let's play with geocoders!

- Adventures in reverse geocoding
- Experiements with re-geocoding a few datasets
