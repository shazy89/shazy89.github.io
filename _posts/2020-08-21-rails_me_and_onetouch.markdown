---
layout: post
title:      "Rails me and oneTouch"
date:       2020-08-21 12:48:44 +0000
permalink:  rails_me_and_onetouch
---

oneTouch is a POS(point of sale) system and is cloud based also is very easy to use, everything is only one click away!

   To be able to use the program users must create a new account or can log in with their GitHub acc. 
   There must be an admin user. Admin users can manage the app. They can create, edit, and delete products. They can also add tables, edit the tables (table numbers) and delete the tables.

   Employee users, after signing up, have access to the main menu.
On the top left side is User Profile button, users can edit and update their information.
In the middle of the main menu, right under the company logo, are the tables.
 **“TABLE10” “TABLE11”**  
 
  Employee users have access to tables and inside the tables are the products. Users can select PRODUCT button for the full list of products. They can add or delete products and even edit the quantity. 
	
When we build a new house foundation it is the most important part of having a sturdy house and the foundation of app are the models and relationships between them.

```
  Users tables
    has_many :products
    has_many :tables
  Products tables
    has_many :select_items
    belongs_to :user
  SelectItem tables
	  belongs_to :product
    belongs_to :table
  Table tabeles
	   has_many :select_items
     belongs_to :user
     has_many :products, through: :select_items
```
   Thats it! Yay! I've finished my project. NO, I'm kidding. After the foundation there is a lot of work going on but this is just a great start and makes everything after a lot more easier.
	 The biggest lesson for me was the space after the end of the quotation mark.  ` ENV['GITHUB_CLIENT' ]`. 
 While trying to setup** Omniauth - Github**  an error occurred. I belive the space after the quotation mark was sending different url requests and I was getting a 404 error.  
	
	

