What is Geocode?
=================

Intro to Geocoding Session for Mozilla Festival 2015; no 40,000 word special issue needed.

## Faciliators:
* [Stuart Lynn](https://github.com/stuartlynn)
* [Aurelia Moser](https://github.com/auremoser)
* [David Riordan](https://github.com/riordan)


* why are geocoders necessary
 * Translate from the world of human*recognizable addresses + names => coordinates (e.g. latitudes and longitudes)
 * Anything you might want to compute about place uses coordinate data, which computers can easily understand, as opposed to these addresses.
 * Addresses aren't computable, and (for our purposes at least) aren't mapable
 * Well... What's an address then?
  * Identification + References
  * Used to identify a place and provide enough information to route to there (with local context or knowledge)
   * e.g.  6 Penrose Way, Greenwich Peninsula, London SE10 0EW, United Kingdom
   * [Addresses be crazy](https://www.mjt.me.uk/posts/falsehoods*programmers*believe*about*addresses/)
  * Convert an address to "referenced coordinates"
   * What are coordinates?
    * Latitude + Longitude
     * [coords of Ravensbourne]
  * And now you can math! Computers are good at Maths.
   * Easy to put on a map - knows how to align your place and your data to the underlying pictures
   * easy* to compute distance
    * maths on a sphere!
   * Integrate with other spatial data:
    * find places nearby, bring in weather data, find satellite imagery for that place

* what do geocoders do
 * geocoders are the {mythical boatman on the river styx for GIS}, taking us from the realm of how we talk about places, full of addresses and names and categories, and transport them into the realm of coordinates, of latitudes and longitudes and geospatial geometries. And they'll transport coordinates into the realm of names and addresses. It's not without cost. It's not always a safe trip, and sometimes data and  meaning are lost, but its a worthwhile one.
 * For our purposes we'll talk about 2 kinds of geocoding and one kind of search:
  * Forward Geocoding: Turning addresses into coordinates (putting a pin on a map) or a box around a place name (like the boundary of a country or city)
   * Address -> lat/lon
  * Reverse Geocoding: Turning coordinates into places by finding the place name or address that best represents the place
   * lat/lon -> address, place name, place hierarchy
   * Sensor data, phone data, address / area validation
 * Both of these are really useful for work in science, journalism, etc.


* [DEMO TIME WITH CSV GEOCODER]
 * [Florida Restaurant Inspections]


    * veltman's CSV geocoder project

* Understand Your Needs:
 * Lists of data
   * Address Data - Address geocoder (google, Here, Nominatim, national geocoders) - Most tools are optimized for this
   * Cities, Towns, Neighborhoods - Places that aren't getting enclosed with walls and a roof - Coarse Geocoder (CartoDB Free, Twofishes, Nominatim, Mapzen, Google)
   * Businesses, public spaces, named places: Points of Interest - Yelp, Foursquare, Google, Facebook
   * Coordinates -> place names:
    * An address: Google, Here, Nominatim, geocodio - look at who has coverage
    * A business: Yelp, 4sq, Google, Facebook, weird proprietary data providers - only ones with the databases
    * Cities, Towns, Neighborhoods, states: Twofishes, [etc.]
 * Place names in text:
  * Looking for "That looks like a place"
   * e.g. {quote}
  * Geoparsing: [CLIFF from MediaMeter](http://cliff.mediameter.org/)

 * Making An An Interactive Thing (app/Site):
  * Localizing users (region) - Autocomplete Geocoder with regions -


* reverse geocoding
* demo time: experiments with re*geocoding a few datasets
