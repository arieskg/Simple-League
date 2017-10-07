## Simple League
##### The goal of this project is to make a very simplistic MOBA with similar rules to league

#### General Assumptions
 - About the game
     - The game takes place on a single map, so map should be top-node class
     - Map is made up of units, passable or impassable
     - **Summoners** must be able to traverse to the other side of the map
 - Game Objects
     - Destroyable structures - state: impassable until destroyed
     - Indestroyable structures - state: impassable
     - Moving Objects
         - Minions
         - Summoners
 - Simple League
     - Since most object attributes are environment related, **Summoners** will be aggregated into Team


#### Design Blueprint
 - The Map
     - Unless specified, all units are impassable
     - D Structures are impassable until destroyed
 - D Structure Generators
     - Turret
     - Inhibitor
     - Nexus
 - Minion Generators
     - Melee
     - Range
     - Cannon
 - Global Clock

#### Research
 - Current Summoner's Rift
     - min: {x:0, y:0}
     - max: {x:14820, y: 14880}
         - minimap - min:{x:-120, y:-120} , max:{x:14870, y:14980}
 - LOL API - https://developer.riotgames.com/api-methods/#lol-static-data-v3
 - Data Dragon - http://ddragon.leagueoflegends.com/tool/


#### Plan Part 1
 - downscale Summoner's map by 10x to x length 1482, y length 1488,
 - 
     - The length from top left to bottom right is the length of hypotenuse
     - The divider will mirror all behaviors in symmetry
