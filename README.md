What is Geocode?
=================

Intro to Geocoding Session for Mozilla Festival 2015; no 40,000 word special issue needed.

![](http://i.imgur.com/RqhIgbV.png)

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

![daynight](http://i.imgur.com/gAHunJD.jpg)

- Translate from the world of human-recognizable addresses + names => coordinates (e.g. latitudes and longitudes)
- Convert an address to "referenced coordinates"

**Considerations**

- Anything you might want to compute about place uses coordinate data, which computers can easily understand, as opposed to these addresses
- Addresses aren't computable, and (for our purposes at least) aren't map-able

### What do geocoders do?

![](http://i.imgur.com/dp3M1ru.jpg)

**What's an address then?**

- Identication + References
- Used to identify a place and provide enough information to route to there (with local context or knowledge)

**What are coordinates?**

- Latitude + Longitude [WGS84]: 51.502817, 0.003117
- (or other coordinate systems)
    - Military Grid Reference System: 31UBT9185310007
    - Geohash: u10hbp
- Standard locator systems to find a place; assume you're using Latitude & Longitude as your units and WGS84 as your coordinate system

### How are geocoders done?

* [CartoDB Academy Account](https://cartodb.com/signup?plan=academy) - geocoding credits and free space
* [Pelias](https://mapzen.com/pelias) - open source geocoder by MapZen
* [CSV geocoder](https://github.com/veltman/csvgeocode) - a map project by Noah Veltman
* [GeoCodio](http://geocod.io/) - geocoding as a service

### Understand Your Needs:

 * Lists of data
   * Address Data - Address geocoder (google, Here, Nominatim, national geocoders) - Most tools are optimized for this
   * Cities, Towns, Neighborhoods - Places that aren't getting enclosed with walls and a roof - Coarse Geocoder (CartoDB Free, Twofishes, Nominatim, Mapzen, Google)
   * Businesses, public spaces, named places: Points of Interest - Yelp, Foursquare, Google, Facebook
   * Coordinates -> place names:
    * An address: Google, Here, Nominatim, geocodio - look at who has coverage
    * A business: Yelp, 4sq, Google, Facebook, weird proprietary data providers - only ones with the databases
    * Cities, Towns, Neighborhoods, states: Twofishes, Mapzen Search
 * Place names in text:
  * Looking for "That looks like a place"
  * Geoparsing: [CLIFF from MediaMeter](http://cliff.mediameter.org/)
 * Making An An Interactive Thing (app/Site):
  * Localizing users (region) - Autocomplete Geocoder with regions


### Let's play with geocoders!

- Adventures in reverse geocoding
- Experiements with re-geocoding a few datasets
- API Keys:
  - Mapzen Search: search-wmLsOxQ [temporary]

![](http://i.imgur.com/RqhIgbV.png)

