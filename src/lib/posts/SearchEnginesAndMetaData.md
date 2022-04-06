---
date: '2022-4-4'
title: 'Search Engines & Metadata'
excerpt: Praising the greatest MtG search engine and how it can be applied to more topics.
categories:
  - 'Programming'
  - 'Metadata'
  - 'Magic The Gathering'
# updated: 
---

# Admiring The Complexity Of MtG

Although I don't get to play it often, I'm a huge fan of the trading card game Magic the Gathering.  From a game design standpoint, I think it's one of (if not the) most well designed complex systems that is out there.  The game appeals to many different kinds of people including competitive tournament players, draft players, artwork fans, rare card collectors, people who enjoy finding unique strategies, and those who play the 4 player game Commander where each deck contains 100 unique cards.  Additionally there are many different formats that the game creators have to balance around.  Some formats include all the cards in the 25+ year history, cards that only exist in the previous few editions, and cards that you have to pull randomly from booster packs.  For each card, the designers have to decide what type it is, how many of each type there are in a set, what the mana cost will be, what mechanics it will have, and what color the card will be based on the previous decisions.  Color, for those who are not familiar with the game, is a very important factor for the designers to get right since each one (and combination of multiple) have their own philosophy and goals that they have to consider.  MtG color theory in itself is very complex to the point where TV Tropes wrote a [43 thousand word article](https://tvtropes.org/pmwiki/pmwiki.php/Analysis/MagicTheGathering) explaining the motivations behind each color, and the explanations they give are very basic and could be expanded on!  

Each card in the game have a lot of details involved with them.  For every card, they all have to have the following information: 
- Name
- Type(s)
- Color(s)
- Mana Cost(s)
- Rarity
- Card text
- Flavor text
- Set/Edition
- Number in set
- Reprint status
- Power (if a creature)
- Toughness (if a creature)
- Loyalty Points (if a planeswalker)
- Artwork
- Artist attribute

At the time of writing there are over 23 thousand unique cards out there.  This does not include cards that have been reprinted in later sets, special promotional cards, or cards that have alternative artwork associated with them.  At this point in the game's history, it should be a nightmare to find a particular card out of the literal tens of thousands out there, but it's shockingly easy thanks to a very clever search engine.

# Enter Scryfall

[Scryfall](https://scryfall.com/) is an online search engine dedicated to Magic the Gathering cards.  The site allows you to search for cards based on any number of factors, sort in many different ways including second hand market prices, and filter those results all from one search box.  Searching for all creature cards that have a converted mana cost of less than 3, with power higher than 5, and is legal in the modern format (but isn't a green card) is as easy as typing this string into the search bar: 

```
t:creature cmc<3 pow>5 f:modern -c:green
```

`t` for type, `cmc` for converted mana cost, and the minus in front of `c` indicates we don't want it's match to show in the results.  The search commands are short, intuitive, and allow for a high level of control!  This search engine has made the daunting task of searching tens of thousands of cards into tens of letters.  

# Metadata Is Beautiful

Notice how the parameters we are searching on match the information about each card listed in the first section above?  This is because the search engine is working on this information, or it's metadata.  For those unaware, metadata refers to data about data, or the data that further describes something.  Metadata for a book would include it's author, the year it was written, the country it was written in, it's language, it's page length, and so on.  By allowing the user to narrow their search down based on this metadata, Scryfall achieves this level of granularity that it makes me wonder why more search engines don't allow this?  

# Other Metadata Search Engines Are Usually Bad

There are sites that have many options in their "advanced search" section, but the approach most take is usually very cumbersomely handled with a large amount of GUI controls and doesn't give you nearly as much control.  A prime example of this would be the [Internet Movie Database](https://www.imdb.com/search/title/).  In order to search based on movie metadata, you need to click many links to find the advanced search section then use it's check boxes and drop downs to get what you want.  If you are looking for a movie that isn't a western, you need to select the checkbox of every other genre.  User rating is stored in a drop down, so you have to scroll through a list of 100 different options to use a scale of 1-10.  Not only do you need to perform more actions than typing a few letters into a search bar, but you don't even get to fine tune that search!  

# The Potential To Find Exactly What You Are Looking For

Imagine if online storefronts had a search engine similar to Scryfall.  If you wanted to find a video game made for the PC that is an RPG set in space that doesn't contain nudity and is made by a smaller sized company, a potential search might look like this:

```
platform:PC genre:RPG setting:space -content:nudity studio-size:indie
```

Now compare that to the current experience.  Go to [Steam's store page](https://store.steampowered.com/) and see how long it takes you to get those kind of results.  Since I directed you to steam, which only sells PC games, the first part of the search is already completed.  For those of you actually doing this experiment, you'll find out quickly how difficult this is.  I find this to be the sad reality we live in, especially considering how many terabytes of data is stored by these companies.  With a better search engine, we have the potential to find the hidden gemstone needle in the rough haystack.

# With Great Search Engines Come Great Metadata Responsibility

Another reason I chose to highlight Steam in that previous example is that their current tagging system is broken.  Publishers have the incentive to tag their games with anything and everything that might apply in order to get more eyes on it.  This produces garbage results when searching by tags (a lame form of metadata) since publishers are putting in garbage values.  When you think of the top selling stealth games, what comes to mind?  Do you think of the Hitman, Metal Gear Solid, or Assassin's Creed games?  If you did, you would be incorrect according to Steam.  Instead you should be thinking of Dead by Daylight, Five Nights at Freddy's, and the first person shooter Metro since that is what comes up in [their top 5 results](https://store.steampowered.com/tags/en/Stealth/#p=0&tab=TopSellers).  I believe if we had better search engines that worked on metadata, we would quickly find out just how bad our current data stores are.  

# Not All Hope Is Lost

Scryfall exists, so this model does work when data is maintained.  Additionally, the data we are concerned about is metadata, data about data!  Data that points to other data!  There is no reason we can't have the ultimate Steam search engine today by creating our own search engine for PC games, then linking to the Steam store page of the particular game when the user has made a selection.  Alternative front ends to popular websites already exist for various reasons, be it a cleaner UI or for privacy concerns.  The technology is already out there, so this isn't an impossible request!  

# Possible FOSS Project? 

This could also be a community effort and open source project.  This would be something that I would love to start up myself in the future, but with my current knowledge of databases being limited I would have to study and learn more before getting this project up and running.  If any reader out there is interested in working on this project with me in the future, please reach out to me using the links in my contact section.  