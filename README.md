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

If you want to add multiple banners, use url-encoded newlines (`%0A`) or spaces (`%20`) as the delimiter and pass them all into the same `banners` parameter: 

https://simbabque.github.io/ingress-banner-mapper/?banners=https://bannergress.com/banner/london-xm-research-7b96%0Ahttps://bannergress.com/banner/rotherhide-ingressfs-august-2024-5245%0Ahttps://bannergress.com/banner/gen-x-in-canada-water-8dfa

## Finding banners based on a place

You can also pass in the `place` URL parameter. We will try to use the Bannergress API to find the next best place and fetch all banners. The output may vary as these places are not sorted. For parts of London, there may be two or more results, and calling it multiple times may return different things each time.

https://simbabque.github.io/ingress-banner-mapper?place=Ronnenberg

## Sharing visible banners

You can use the '🔗' button on the map to copy a sharable URL of the current set of banners to the clipboard. This will include
everything on the map, but not where your map is scrolled to. It does not take the content of the text box at the bottom of the
screen into account. It is intended to be used to store or share a curated list of banners.

## Exporting banners as Drawtools JSON

You can use the 'DT' button on the map to export all visible banners as a JSON file compatible with Drawtools. This creates a downloadable file containing all banner routes as polylines with their coordinates and colors. The exported file will be automatically named with the current location and timestamp, for example: `banners_London_2025-09-03-14-30-15.json`.

You can then use this to import the routes into IITC with Drawtools. It is useful for planning new routes while avoiding existing ones.

## Hiding the navigation panel

You can use the '☰' (hamburger menu) button in the top-right corner of the map to show or hide the navigation panel. This is useful when you want to:

- Get a full-screen view of the map for presentations or screenshots
- Maximize map space when viewing many banners
- Quickly switch between navigation and map-only views

You can also hide the navigation panel permanently by appending the `bare=1` URL parameter. This is useful if you want to present a fixed view of a specific set of banners, such as providing a link for the banners in the area of a First Saturday event:

https://simbabque.github.io/ingress-banner-mapper/?banners=https://bannergress.com/banner/london-xm-research-7b96%0Ahttps://bannergress.com/banner/rotherhide-ingressfs-august-2024-5245%0Ahttps://bannergress.com/banner/gen-x-in-canada-water-8dfa&bare=1

## Disclaimer

This project is not affiliated with Niantic Spatial, Inc., Ingress, or Bannergress.

## Issues

If you encounter any issues or have any feature requests, please [raise an issue on Github](https://github.com/simbabque/ingress-banner-mapper/issues).