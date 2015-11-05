What is Geocode?
=================

Intro to Geocoding Session for Mozilla Festival 2015; no 40,000 word special issue needed.

## Faciliators:
* [Stuart Lynn](https://github.com/stuartlynn)
* [Aurelia Moser](https://github.com/auremoser)
* [David Riordan](https://github.com/riordan)


- why are geocoders necessary
 - Translate from the world of human-recognizable addresses + names => coordinates (e.g. latitudes and longitudes)
 - Anything you might want to compute about place uses coordinate data, which comptuers can easily understand, as opposed to these addresses.
 - Addresses aren't computable, and (for our purposes at least) aren't mapable
 - Well... What's an address then?
  - Identication + References
  - Used to identify a place and provide enough information to route to there (with local context or knowledge)
   - e.g.  6 Penrose Way, Greenwich Peninsula, London SE10 0EW, United Kingdom
   - [Addresses be crazy](https://www.mjt.me.uk/posts/falsehoods-programmers-believe-about-addresses/)
  - Convert an address to "referenced coordinates"
   - What are coordinates?
    - Latitude + Longitude
- how are geocoders done
- what do geocoders do

    - pelias perhaps?
    - veltman's CSV geocoder project

- reverse geocoding
- demo time: experiements with re-geocoding a few datasets
