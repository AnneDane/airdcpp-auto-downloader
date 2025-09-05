# airdcpp-auto-downloader [![GitHub Actions][build-badge]][build] [![npm package][npm-badge]][npm] [![npm downloads][npm-dl-badge]][npm] [![codecov][coverage-badge]][coverage]

Extension to add search terms that will be searched in intervals and downloaded when found.

## ⚠️ TTH Auto-Search Enhancement (xAI-Grok Modified Version)

**This fork includes TTH (Tiger Tree Hash) auto-search functionality developed by xAI-Grok.**

### New TTH Features:
* **Automatic TTH Detection**: 39-character base32 TTH values are automatically detected
* **Exact TTH Searches**: Uses AirDC++ API's TTH search capability for precise file matching
* **Mixed Search Lists**: Combine TTH and text patterns in the same search configuration
* **Backward Compatibility**: All existing text-based search features remain unchanged

## Supported NodeJS versions
Though older NodeJS versions may work, only the versions in LTS or Maintenance status are supported.

As of right now these are **18.x (LTS), 16.x (LTS), 14.x (LTS)**.

See NodeJS documentation for up to date information: https://github.com/nodejs/release#release-schedule


## Known issues
Changing the search interval requires stopping and starting the extension

## Features

* Configure search interval in minutes
* Provide multiple search terms as a list, one search term per line
* **NEW**: Automatic TTH (Tiger Tree Hash) detection and searching
* Options for:
  * minimum size
  * file type
  * file extensions
  * download directory
  * exclude keywords
  * exclude users (when a user is sole source for item)<sup>1</sup>
  * priority
  * require exact match
  * allow queueing all items from search result
  * remove search term when found
  * handle dupes

### TTH Usage Examples:
```
NXLFNHV2HQHTR6GPXVBB6R3NOJPOROCRZ3MVF7Y
Some movie name
YUQAQOGX6MPO7WT4VKUARKUOVZZD2ZKMWE3G33A
Another search term
```
The extension automatically detects 39-character TTH values and performs exact TTH searches.

---

  <sup>1</sup> For now list of excluded users don't have to include all special character prefixes or suffixes as we don't do exact matching.<br />Though it means if a user has a very generic nick like 'some' it would also match a user named 'someone'.<br />
  So be sure to add the users as unique as possible. Feel free to open an issue or let me know what you think of this.

## Screenshot

![Settings Screenshot](doc/settings-screenshot.png?raw=true "None")


## Resources

- [Bug tracker](https://github.com/peps1/airdcpp-auto-downloader/issues)
- [Changelog](https://github.com/peps1/airdcpp-auto-downloader/blob/master/CHANGELOG.md)

- [AirDC++ Web API reference](https://airdcpp.docs.apiary.io/)

[build-badge]: https://github.com/peps1/airdcpp-auto-downloader/workflows/build/badge.svg
[build]: https://github.com/peps1/airdcpp-auto-downloader/actions

[npm-badge]: https://img.shields.io/npm/v/airdcpp-auto-downloader.svg?style=flat-square
[npm]: https://www.npmjs.org/package/airdcpp-auto-downloader
[npm-dl-badge]: https://img.shields.io/npm/dt/airdcpp-auto-downloader?label=npm%20downloads&style=flat-square

[coverage-badge]: https://codecov.io/gh/peps1/airdcpp-auto-downloader/branch/master/graph/badge.svg
[coverage]: https://codecov.io/gh/peps1/airdcpp-auto-downloader
