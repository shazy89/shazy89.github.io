---
layout: post
title:      "Power Of JS"
date:       2020-09-18 22:33:07 +0000
permalink:  power_of_js
---

Yes, it is incredibly expressive, powerful, limitless, popular, very easy to learn, there are over 30 000 NPM packages available. Moving forward from Rails was hard at the beginning but after four weeks now I can see myself as a JS developer. It was very hard to decide on my project this time and I ended up with FootballMasters.
  What do we need to create a sports single page web app?
   
  API ARCHITECTURE is:
	Countries , Leagues, Teams, Players Api
```
fetch(`${rapidApiBaseUrl}/v2/countries`
fetch(`${rapidApiBaseUrl}/v2/leagues/country/${countryName.country}/2020`
fetch(`${rapidApiBaseUrl}/v2/teams/league/${id}`
fetch(`${rapidApiBaseUrl}/v2/players/squad/${id}/2019
fetch(`${rapidApiBaseUrl}/v2/leagues/league/${lgId}`
fetch(`${rapidApiBaseUrl}/v2/teams/team/${teamId}`
```
Also user's can add players and create new Favorite Teams. Thanks to Rails api mode, we can create our backend in five minutes and  it is very powerful. It's fun when you try to delcare variables on rails using `const or let` or when you forget about `const and let ` and get errors while using JS.
 My models directory contains five classes.
 
  ```"Leagues class"
  "Teams class"
  "Players class"
  "FavoriteTeams class "
  "Materialize clas"```
	
  Services directory has `Api class` . Api class is for all `GET` requests and we need country names to to get leagues.
	After we get leagues we can render teams and from teams we render players. This project was also my teacher, it taught me so much and made belive that if you want, you can do everything.   
	

	
	
