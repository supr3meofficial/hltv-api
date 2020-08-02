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
'July 27th, 2020'
```

## `top5teams`  

```python
>>> import main as hltv
>>> hltv.top5teams()
['BIG', 'Vitality', 'Evil Geniuses', 'Natus Vincere', 'G2']
```

## `top30teams`  

```python
>>> hltv.top30teams()
[{'name': 'BIG',
  'rank': 1,
  'rank-points': 869,
  'team-id': 7532,
  'team-players': [{'name': "Johannes 'tabseN' Wodarz", 'player-id': 5794},
                   {'name': "Tizian 'tiziaN' Feldbusch", 'player-id': 5796},
                   {'name': "Florian 'syrsoN' Rische", 'player-id': 7266},
                   {'name': "Ismailcan 'XANTARES' Dörtkardeş",
                    'player-id': 7938},
                   {'name': "Nils 'k1to' Gruhne", 'player-id': 12781}]},
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
['dupreeh', 'device', 'es3tag', 'Magisk', 'Bubzkji']
```

## `get_team_info`  

```python
>>> hltv.get_team_info("6667")
{'current-lineup': [{'country': 'Denmark',
                     'maps-played': 939,
                     'name': 'Peter Rasmussen',
                     'nickname': 'dupreeh'},
                    {'country': 'Denmark',
                     'maps-played': 919,
                     'name': 'Nicolai Reedtz',
                     'nickname': 'device'},
                    {'country': 'Denmark',
                     'maps-played': 0,
                     'name': 'Patrick Hansen',
                     'nickname': 'es3tag'},
                    {'country': 'Denmark',
                     'maps-played': 492,
                     'name': 'Emil Reif',
                     'nickname': 'Magisk'},
                    {'country': 'Denmark',
                     'maps-played': 0,
                     'name': 'Lucas Andersen',
                     'nickname': 'Bubzkji'}],
 'historical-players': [{'country': b'Denmark',
                         'maps-played': 90,
                         'name': 'René Borg',
                         'nickname': b'cajunb'}, ...
 'stats': {b'K/D Ratio': b'1.13',
           b'Maps played': b'944',
           b'Rounds played': b'24605',
           b'Total deaths': b'77289',
           b'Total kills': b'87244',
           b'Wins / draws / losses': b'645 / 2 / 297'},
 'team-name': b'Astralis'}
```

## `get_matches`  

```python
>>> hltv.get_matches()
[{'date': '2020-08-03',
  'event': b'Nine to Five 2',
  'event_logo': 'https://static.hltv.org/images/eventLogos/5431.png',
  'team1': b'Gambit Youngsters',
  'team1_logo': 'https://static.hltv.org/images/team/logo/9976',
  'team2': b'ALTERNATE aTTaX',
  'team2_logo': 'https://static.hltv.org/images/team/logo/4501',
  'time': '12:00'},
...]
```

## `get_results`

```python
>>> hltv.get_results()
[{'date': b'Results for July 26th 2020',
  'event': b'Eden Arena Malta Vibes Cup 4',
  'event_logo': 'https://static.hltv.org/images/eventLogos/5434.png',
  'team1': b'LDLC',
  'team1score': 2,
  'team2': b'CR4ZY',
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
