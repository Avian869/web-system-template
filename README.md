# Dota 2 match prediction system

## Description
- The system shows heroes, there stats, matchups, bought items, also allows users to make matchup suggestions. The system also allows you to build teams and get there odds of winning against one another.

## Entity definition
- Entity – Hero (
- id(number 1 - 129), 
- name(<50 symbols), 
- image(string), 
- icon(string), 
- matchup statistics(
- hero id(number 1 - 129),
- winrate(number 0 - 100))

## API definition
- System will use methods
- GET api/heroStats - gets all stats of all dota 2 heroes
- GET api/heroes/:id/matchups
- GET api/heroes/:id/matchups - gets recorded matchups for hero with given ID
    - 400 - {error: 'invalid hero_id' }
- POST /teams/:id - puts selected hero in team
    - 400 - {error: 'invalid hero_id' }
- DELETE /teams/:id - delete a given hero from team
    - 400 - {error: 'invalid hero_id' }

## UI definition
