# JS-paramExtractor

Thanks to Danyz89.

Tool for extract parameters from text and create a objects array 

paramExtractor uses a text o char for split a general text
var textSplit='';

uses a array of name and regular expresion pair

var regexList=[];

also can convert text like 352,632,734,135 to array [352,632,734,135] if fieldToSplit include the field name 

var fieldToSplit='';

for example

for extract a list with some param from pokemon essential db(pokemonEssential.txt) property from Maruno17 https://github.com/Maruno17/pokemon-essentials/blob/master/PBS/pokemon.txt

we use:
var textSplit='#-----';
var fieldToSplit='baseStats types';
var regexList=[['name', /^Name\s?=\s?(\w+)/mi],
	['types', /^Types\s?=\s?((\w+,?)+)/mi],
	['baseStats', /^BaseStats\s?=\s?((\d+,?)+)/mi],
	['description', /^Pokedex\s?=\s?([\wéáíóúèàìòùº\s\d\.\'\,\-\—\(\)\!\"]+)\r\n/mi]];
 
this is the result with this params for pokemonEssential.txt

(899) [1: {…}, 2: {…}, 3: {…}, 4: {…}, 5: {…}, 6: {…}, 7: {…}, 8: {…}, 9: {…}, 10: {…}, 11: {…}, 12: {…}, 13: {…}, 14: {…}, 15: {…}, 16: {…}, 17: {…}, 18: {…}, 19: {…}, 20: {…}, 21: {…}, 22: {…}, 23: {…}, 24: {…}, 25: {…}, 26: {…}, 27: {…}, 28: {…}, 29: {…}, 30: {…}, 31: {…}, 32: {…}, 33: {…}, 34: {…}, 35: {…}, 36: {…}, 37: {…}, 38: {…}, 39: {…}, 40: {…}, 41: {…}, 42: {…}, 43: {…}, 44: {…}, 45: {…}, 46: {…}, 47: {…}, 48: {…}, 49: {…}, 50: {…}, 51: {…}, 52: {…}, 53: {…}, 54: {…}, 55: {…}, 56: {…}, 57: {…}, 58: {…}, 59: {…}, 60: {…}, 61: {…}, 62: {…}, 63: {…}, 64: {…}, 65: {…}, 66: {…}, 67: {…}, 68: {…}, 69: {…}, 70: {…}, 71: {…}, 72: {…}, 73: {…}, 74: {…}, 75: {…}, 76: {…}, 77: {…}, 78: {…}, 79: {…}, 80: {…}, 81: {…}, 82: {…}, 83: {…}, 84: {…}, 85: {…}, 86: {…}, 87: {…}, 88: {…}, 89: {…}, 90: {…}, 91: {…}, 92: {…}, 93: {…}, 94: {…}, 95: {…}, 96: {…}, 97: {…}, 98: {…}, 99: {…}, 100: {…}, …]

[1 … 100]
1: {name: 'Bulbasaur', types: Array(2), baseStats: Array(6), description: "Bulbasaur can be seen napping in bright sunlight. … sun's rays, the seed grows progressively larger."}

2: {name: 'Ivysaur', types: Array(2), baseStats: Array(6), description: "To support its bulb, Ivysaur's legs grow sturdy. I…ght, the bud will soon bloom into a large flower."}

3: {name: 'Venusaur', types: Array(2), baseStats: Array(6), description: "Venusaur's flower is said to take on vivid colors …he flower's aroma soothes the emotions of people."}

4: {name: 'Charmander', types: Array(1), baseStats: Array(6), description: 'The flame that burns at the tip of its tail is an …armander is happy, and blazes when it is enraged.'}

5: {name: 'Charmeleon', types: Array(1), baseStats: Array(6), description: 'Without pity, its sharp claws destroy foes. If it …ame on its tail flares with a bluish white color.'}

6: {name: 'Charizard', types: Array(2), baseStats: Array(6), description: 'A Charizard flies about in search of strong oppone…erial. However, it will never torch a weaker foe.'}

7: {name: 'Squirtle', types: Array(1), baseStats: Array(6), description: 'Its shell is not just for protection. Its rounded … water, enabling Squirtle to swim at high speeds.'}

8: {name: 'Wartortle', types: Array(1), baseStats: Array(6), description: "Its large tail is covered with rich, thick fur tha…e evidence of this Pokémon's toughness in battle."}

9: {name: 'Blastoise', types: Array(1), baseStats: Array(6), description: 'The waterspouts that protrude from its shell are h…y nail tin cans from a distance of over 160 feet.'}

10: {name: 'Caterpie', types: Array(1), baseStats: Array(6), description: 'Its voracious appetite compels it to devour leaves…eleases a terribly strong odor from its antennae.'}

11: {name: 'Metapod', types: Array(1), baseStats: Array(6), description: 'Its shell is as hard as an iron slab. A Metapod do… its soft innards for evolution inside the shell.'}

12: {name: 'Butterfree', types: Array(2), baseStats: Array(6), description: 'It has a superior ability to search for delicious … honey from flowers blooming over six miles away.'}

13: {name: 'Weedle', types: Array(2), baseStats: Array(6), description: 'A Weedle has an extremely acute sense of smell. It…es by sniffing with its big red proboscis (nose).'}

14: {name: 'Kakuna', types: Array(2), baseStats: Array(6), description: 'It remains virtually immobile while it clings to a…. This is evident from how hot its shell becomes.'}

15: {name: 'Beedrill', types: Array(2), baseStats: Array(6), description: 'A Beedrill is extremely territorial. For safety re…ts nest. If angered, they will attack in a swarm.'}
