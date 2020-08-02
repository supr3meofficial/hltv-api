# Code-breaking changes
### 'event_image_url' is now called 'event_logo' 

# Extra features
* New 'ranking_date' function: retrieves the HLTV Ranking date
* Retrievable event logo image urls: 'event_logo'
* Retrievable team logo images urls: 'team1_logo' and 'team2_logo'

# hltv-api
Provides an API for HLTV

## `top5teams`  

```python
>>> import main as hltv
>>> hltv.ranking_date()
'May 4th, 2020'
```

## `top5teams`  

```python
>>> import main as hltv
>>> hltv.top5teams()
['Astralis', 'fnatic', 'Natus Vincere', 'mousesports', 'Liquid']
```

## `top30teams`  

```python
>>> hltv.top30teams()
[{'name': 'Astralis',
  'rank': 1,
  'rank-points': 847,
  'team-id': 6665,
  'team-players': [{'name': "Andreas 'Xyp9x' Højsleth", 'player-id': 4954},
                   {'name': "Peter 'dupreeh' Rasmussen", 'player-id': 7398},
                   {'name': "Lukas 'gla1ve' Rossander", 'player-id': 7412},
                   {'name': "Nicolai 'device' Reedtz", 'player-id': 7592},
                   {'name': "Emil 'Magisk' Reif", 'player-id': 9032}]},
...]
```

## `top_players`  

```python
>>> hltv.top_players()
[{'country': b'France',
  'maps-played': b'600',
  'name': 'Mathieu Herbaut',
  'nickname': b'ZywOo',
  'rating': b'1.29'},
...]
```

## `get_players`  

```python
>>> hltv.get_players("6665")
['Xyp9x', 'dupreeh', 'gla1ve', 'device', 'Magisk']
```

## `get_team_info`  

```python
>>> hltv.get_team_info("6667")
{'current-lineup': [{'country': 'Denmark',
                     'maps-played': 918,
                     'name': 'Andreas Højsleth',
                     'nickname': 'Xyp9x'}, ...],
 'historical-players': [{'country': b'Denmark',
                         'maps-played': 90,
                         'name': 'René Borg',
                         'nickname': b'cajunb'}, ...]
 'stats': {b'K/D Ratio': b'1.13',
           b'Maps played': b'918',
           b'Rounds played': b'23911',
           b'Total deaths': b'75124',
           b'Total kills': b'84890',
           b'Wins / draws / losses': b'629 / 2 / 287'},
 'team-name': b'Astralis'}
```

## `get_matches`  

```python
>>> hltv.get_matches()
[{'date': b'2020-05-05 - Tuesday',
  'event': b'ESL One: Road to Rio - Europe',
  'event_image_url': 'https://static.hltv.org/images/eventLogos/5277.png',
  'team1': b'Dignitas',
  'team2': b'Astralis',
  'time': b'23:30'},
...]
```

## `get_results`

```python
>>> hltv.get_results()
[ {'date': '5/5/2020',
  'event': b'ESL One: Road to Rio - Europe',
  'event_image_url': 'https://static.hltv.org/images/eventLogos/5277.png',
  'team1': b'FaZe',
  'team1score': 2,
  'team2': b'GODSENT',
  'team2score': 0},
... ]
```

## `get_results_by_date`

```python
>>> hltv.get_results_by_date()
[{'date': '5/5/20',
  'event': 'ESL One: Road to Rio - Europe',
  'map': 'Overpass',
  'team1': 'FaZe',
  'team1score': 16,
  'team2': 'GODSENT',
  'team2score': 6},
... ]
```
