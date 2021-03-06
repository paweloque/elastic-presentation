## elasticsearch Presentation by Iterativ/Pawel Kowalski

## Demo:

Data: http://data.iterativ.ch:9200

Explorer: http://data.iterativ.ch/

# Git Repositories:

This here: https://github.com/iterativ/elastic-presentation

Explorer: https://github.com/iterativ/elastic-dataexplorer


## Installation and Development

# Install

```
brew install openssl
env LDFLAGS="-L$(brew --prefix openssl)/lib" CFLAGS="-I$(brew --prefix openssl)/include" pip install cryptography
pip install -r req.txt
```

# Elasticsearch data server:
http://data.iterativ.ch

# Access Server
ssh data

## Index data into elasticsearch

```
cd elastic
python index_bulk.py -e data.iterativ.ch:9200 -f ../data/musicbrainz.json -m albums.json -i albums -t album -c 100
```

## Manipulate json data

```
jq '.[1]' musicbrainz.json > musicbrainz_1.json
```