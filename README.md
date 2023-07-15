# pornhub

A bash script for downloading pornhub in json.

## Requirements

 - [hgrep](https://github.com/TUVIMEN/hgrep)
 - [jq](https://github.com/stedolan/jq)

## Installation

    install -m 755 pornhub /usr/bin

## Json format

Here's example of [pornstar](pornstar-example.json), [video](video-example.json), [model](model-example.json) and [playlist](playlist-example.json).

## Usage

    pornhub [OPTION] [DIR]

The script gets links from sitemap and downloads specified pages (4 in parallel). Files are named by sha256sum of their urls.

Download pornstars into DIR

    pornhub -p DIR

Download videos into current directory using 8 threads

    pornhub -t 8 -v

Download models into DIR

    pornhub -m DIR

Download playlists into DIR

    pornhub -P DIR

Get some help

    pornhub -h
