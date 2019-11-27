# Introduction
Consider a social platform for coffee lovers. Users connect via a smartphone app to the Coffee Club server. The job is to design a database that will support these software features.

# Business requirements
## Cafes
The names, addresses, map locations and opening hours of about ten thousand cafes are visible in the app. Users can browse cafes either via an alphabetical list or a map interface. 

When viewing a café’s profile, a user can see the café’s average rating, as well as reviews and photos uploaded by other users.

For each café we record the opening and closing time for each of the seven days of the week,each café stores a menu of the drinks it sells and their prices. Drink names must be drawn from a standard list of about 100 drinks maintained in the system. Some cafés may also sell other items (such as cakes) but we don’t record these in our system.
## Ratings, photos and favourites
Users can rate cafes. A rating consists of a whole number of “stars” between 1 and 5 inclusive, along with an optional piece of text (up to about 20 words). A user can only rate a given café once. Users can also upload photos they take of a cafe: these can later be browsed by other users. Users can also mark particular cafes as “favourites”. 

A user’s app will beep if they pass within 500m of one of their favourite cafés, or if another user they are following checks in at a favourite cafe. Users can later “unfavourite” the café if they wish, and still later, “favourite” it again, and we need to keep a history of these actions.
## Posting to the Timeline
The Coffee Club app has a social media-style timeline, to which users can post text and photos. A post consists of a short piece of text (up to 1000 characters) with an optional photo. We expect users to post once per day each on average.

Other users can “like” a post, and if they wish, later “unlike” it. Users can also “comment” on posts, adding a short piece of text (again up to 1000 characters). However users cannot comment on comments.

The app allows users reading their newsfeed to sort the list of posts, either by the time each post was entered, or by the number of likes each post has received.
## Social Graph
Users can ‘follow’ other users. The social graph works like Twitter’s: user A can follow user B, without B needing to approve, nor B automatically becoming a follower of A. Users might for example choose to follow people they know offline, or celebrities, or expert members of the user community.
If a user decides to follow another, they can later choose to “unfollow” them if they wish: we need to keep track of these actions for later analysis.
## Locations
While a user’s phone is switched on, the Coffee Club app sends the user’s current location to the server every minute. Locations are recorded as a pair of numbers representing latitude and longitude. We use a precision of 4 decimal places.
## Check-ins
Users can use their app to “check in” at cafes that they visit. Optionally, the user can tag one other user in the checkin. Checkin data is used to enable the user’s followers to see when the user is present at the café. We mine checkin data periodically for business intelligence.
## News
The app has a ‘news’ page where users can browse system- generated stories about significant events such as sales or parties. A story consists of a heading and a short body of text (max 1000 characters) and a photo. Stories can be browsed either in date order or by café. We allow customers to like news stories, but not comment on them.
