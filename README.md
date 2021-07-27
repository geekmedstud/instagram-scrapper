# instagram-scrapper
Tried some code out there

pip install instagramy

from instagramy import Instagram 


# Connecting the profile 
user = Instagram("geeks_for_geeks") 

# printing the basic details like 
# followers, following, bio 
print(user.is_verified()) 
print(user.popularity()) 
print(user.get_biography()) 

# return list of dicts 
posts = user.get_posts_details() 

print('\n\nLikes', 'Comments') 
for post in posts: 
	likes = post["likes"] 
	comments = post["comment"] 
	print(likes,comments)

from instagramy import Instalysis 

# Instagram user_id of ipl teams 
teams = ["chennaiipl", "mumbaiindians", 
		"royalchallengersbangalore", "kkriders", 
		"delhicapitals", "sunrisershyd", 
		"kxipofficial"] 

data = Instalysis(teams) 

# return the dataframe 
data_frame = data.analyis() 
data_frame
