---
layout: post
title:      "Ruby Red Sinatra"
date:       2020-07-19 13:56:51 +0000
permalink:  ruby_red_sinatra
---


Yeah, I did it! I built my first website Ruby Red. Users can create accounts, log in and log out.
Ruy Red is the very beginning of the website, users have an opportunity of creating Cars (used and new) and Real Estate posts. Ruby Red is the connection between a seller and buyer and is totaly free :D 
 
Corneal .. Magic :D Maybe it's not magic but it is really helpful..
   `corneal new APP-NAME    # Creates a new Sinatra application` and Sinatra skeleton is ready.. 
	 Ok, Ruby Red is created and I'm looking at a white page and have no idea where to start.
	 It is not like the lessons we were working on. We have to build everything from the scratch.
Before I started my project I took notes about my route and this was wery helpful.
   
	`get "/"  do
	   erb :welcome
	end
	
	post "/" do 
	   erb :welcome
	end `
  
Look at this code, it looks very simple to me now after I spent many hours of practice and debuging my mistakes.
But I can say that I love `errors` my errors were my teachers in this project.
The worst was when I forgot to add ForeginKey to my `CreateCreateHouseposts` table.
After my first attempt to generate **house post** I found out that I have too add ForeginKey. 
Ok, that's easy, lets add it.
 
 `class ForeginKey < ActiveRecord::Migration
  def change
    add_column :create_houseposts, :usere_id, :integer
  end
end
` 
This :user **e**_id this is because of **e** letter I had to spend about my 3 hrs trying to figure where the problme is.
 I wasnt expecting the error ` add_column :create_houseposts, :usere_id, :integer` here because I just migrated that and  everything was fine. But, I have learned my lesson.. If something is wrong check your last step and make sure everything is ok with that before digging deeper and get lost like I did.
