# Dota 2 match prediction system

## Description
- The system shows heroes, there stats, matchups, bought items, also allows users to make matchup suggestions. The system also allows you to build teams and get there odds of winning against one another.

## Entity definition
- Entity – Hero (
- id(number), 
- name(<50 symbols), 
- image, 
- icon, 
- matchup statistics(
- hero id(number),
- winrate(number))

## API definition
- System will use methods
- GET api/heroStats - gets all stats of all dota 2 heroes
- GET api/heroes/:id/matchups
- GET api/heroes/hero_id/matchups - gets recorded matchups for hero with given ID
    - 400 - {error: 'invalid hero_id' }
- POSt /teams/hero_id - puts selected hero in team
    - 400 - {error: 'invalid hero_id' }
- DELETE /teams/hero_id - delete a given hero from team
    - 400 - {error: 'invalid hero_id' }

## UI definition
