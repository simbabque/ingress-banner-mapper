# Bannergress Map Display

This project displays banners from [Bannergress](https://bannergress.com) on a map.

## Features

- Display multiple banners on a single map.
- Display all banners from a place, such as a city or a country, by pasting the place's "browse" URL.
- Suggested places: London, Lisbon, Porto, Hannover.

## Usage

1. Go to https://simbabque.github.io/ingress-banner-mapper/.
2. Paste your Bannergress links into the textarea. This can be an individual banner or a whole area.
3. Click the "Show banners" button to display the banners on the map.
4. Click the "Clear banners" button to remove all banners from the map.


## Presetting a banner or zoom to share with others

You can pass in the `banners` URL parameter to make the page prepoluate and load a specific banner or area. Here's an example:

https://simbabque.github.io/ingress-banner-mapper/?banners=https://bannergress.com/banner/francesinha-8c71

## Finding banners based on a place

You can also pass in the `place` URL parameter. We will try to use the Bannergress API to find the next best place and fetch all banners. The output may vary as these places are not sorted. For parts of London, there may be two or more results, and calling it multiple times may return different things each time.

file:///home/julien/code/private/banners/index.html?place=Ronnenberg

## Disclaimer

This project is not affiliated with Niantic, Inc., Ingress, or Bannergress.

## Issues

If you encounter any issues or have any feature requests, please [raise an issue on Github](https://github.com/simbabque/ingress-banner-mapper/issues).