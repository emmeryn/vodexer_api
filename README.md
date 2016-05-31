# Vodexer API
The API backend of Vodexer.

# Vodexer
Vodexer is a video indexing website aimed to index, categorise and tag Videos-on-Demand (VODs). Initially aimed towards e-sports such as Dota 2, Counter-Strike: Global Offensive, and League of Legends, it could potentially be useful for VODs of sporting events such as soccer or basketball. It is not primarily intended to host videos - rather, it makes use of existing videos already uploaded to YouTube, Twitch, or Hitbox, and tags timespans in the video with relevant information. For example, if a player achieved a double kill, the time period where it happens can be tagged with information such as the player's name, the type of kill (double kill in this case), the players killed, the characters they were playing as at that point, skills used, etc. This will make searching later on much easier, such as when you are looking for a particular player's triple kills with a certain skill, for example.

# Planned Features
* Adding videos to database
  * Initial seed with known tournaments, etc.
  * Manually indexing videos via web form.
  * Automatically indexing videos from certain YouTube/Twitch/Hitbox accounts.
* Categorisation of videos
  * Type: e.g. Video game, Sports, Political events
  * Name: e.g. Dota 2, English Premier League, Presidential Elections of the USA
  * Event: e.g. The International 2015, Tottenham Hotspurs vs Leicester City, Election Rally 2015
* Tagging of videos
  * Key-value pair?  e.g. ```{ player_name: iceiceice, no_of_kills: 2, skills_used: tidehunter_ravage, targets_hit: 4, damage_dealt: 3579 }```
  * Need to think more deeply about how key-value tagging will work. How do we design it extensible enough? 
  * To e.g. add descriptions to the tags, such as the damage done by the skills. Another table for tag descriptions...? 
  * What about if tags only belong to a certain game (lower priority)? Do we validate upon uploading a video?
* Search by category and tags
* Upvote/downvote (or equivalent) system to determine the relevancy of tags.
* Support for multiple video hosts
  * YouTube
  * Twitch
  * Hitbox
* API for tagging videos
  * e.g. provide video link and sets of timestamps + tags in JSON format.
  * Intended to allow games to provide direct tagging of captured video.
* Monetizing to keep the site alive?
  * Ads...? 
  * Miracle investor :P