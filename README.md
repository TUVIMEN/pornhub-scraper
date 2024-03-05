# pornhub-scraper

A bash script for scraping pornhub in json.

## Requirements

 - [hgrep](https://github.com/TUVIMEN/hgrep)
 - [jq](https://github.com/stedolan/jq)

## Installation

    install -m 755 pornhub-scraper /usr/bin

## Json format

Here's example of [pornstar](pornstar-example.json), [video](video-example.json), [model](model-example.json), [playlist](playlist-example.json) and [user](user-example.json).

## Usage

    pornhub-scraper [OPTION] [DIR]

The script gets links from sitemap and downloads specified pages (4 in parallel). Files are named by sha256sum of their urls.

It's recommended that you use -S option to save time.

Download pornstars into DIR

    pornhub-scraper -p DIR

Download videos into current directory using 8 threads

    pornhub-scraper -t 8 -v

Download models into current directory

    pornhub-scraper -m

Download playlists into DIR

    pornhub-scraper -P DIR

Download users from urls in FILE

    pornhub-scraper -u FILE

Get some help

    pornhub-scraper -h
