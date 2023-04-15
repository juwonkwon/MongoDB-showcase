# AirBnB MongoDB Analysis

This [airbnb listings](data/listings.csv) was obtained from the airbnb website. It contains information on Great Manchester, UK area listings in CSV format


1. show exactly two documents from the listings collection in any order
code:
```
jk6240> db.listings.find().limit(2)
```
result:
```
{
    _id: ObjectId("643ad82124ed4983860f1217"),
    id: 4468181,
    listing_url: 'https://www.airbnb.com/rooms/4468181',
    scrape_id: Long("20230327145459"),
    last_scraped: '2023-03-27',
    source: 'city scrape',
    name: 'Double Room in shared apartment',
    description: 'Close to Motorway links, free on street public parking, within 10 mins walk from Tram, Media city within 20 mins on tram. Monton bars/restaurants within 10 mins walk. Room includes Single Divan Bed, Memory foam Mattress, Wardrobe, Bedside cabinet, Chest of Drawers, Table Lamp, Drop leaf table and chair. The apartment is shared with one tenant and Landlord, common areas include bathroom, Lounge/Dining area and Hallway.<br /><br /><b>The space</b><br />Make yourself at home, use the kitchen and cooking facilities. Towels and bedding provided.<br /><br /><b>Guest access</b><br />Use the Lounge, Hall, Kitchen and bathroom',
    neighborhood_overview: '',
    picture_url: 'https://a0.muscache.com/pictures/5284eef5-392d-4148-a9c8-c8ca89081b6f.jpg',
    host_id: 23182584,
    host_url: 'https://www.airbnb.com/users/show/23182584',
    host_name: 'Michael',
    host_since: '2014-10-31',
    host_location: 'Manchester, United Kingdom',
    host_about: 'Hi I am an easy going person. I am Irish and like outdoor activities including hiking and cycling. I work as a chartered surveyor in Manchester. I like good friends, family, music and the odd social drink. ',
    host_response_time: 'N/A',
    host_response_rate: 'N/A',
    host_acceptance_rate: 'N/A',
    host_is_superhost: 'f',
    host_thumbnail_url: 'https://a0.muscache.com/im/users/23182584/profile_pic/1414768927/original.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/users/23182584/profile_pic/1414768927/original.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: '',
    host_listings_count: 1,
    host_total_listings_count: 1,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: 't',
    host_identity_verified: 'f',
    neighbourhood: '',
    neighbourhood_cleansed: 'Salford District',
    neighbourhood_group_cleansed: 'Salford',
    latitude: 53.48526,
    longitude: -2.34232,
    property_type: 'Private room in rental unit',
    room_type: 'Private room',
    accommodates: 1,
    bathrooms: '',
    bathrooms_text: '1 bath',
    bedrooms: 1,
    beds: 1,
    amenities: '["Iron", "TV", "Essentials", "Hangers", "Washer", "Smoke alarm", "Lock on bedroom door", "Heating", "Wifi", "Kitchen"]',
    price: '$100.00',
    minimum_nights: 2,
    maximum_nights: 14,
    minimum_minimum_nights: 2,
    maximum_minimum_nights: 2,
    minimum_maximum_nights: 14,
    maximum_maximum_nights: 14,
    minimum_nights_avg_ntm: 2,
    maximum_nights_avg_ntm: 14,
    calendar_updated: '',
    has_availability: 't',
    availability_30: 29,
    availability_60: 59,
    availability_90: 89,
    availability_365: 364,
    calendar_last_scraped: '2023-03-27',
    number_of_reviews: 4,
    number_of_reviews_ltm: 0,
    number_of_reviews_l30d: 0,
    first_review: '2016-10-06',
    last_review: '2017-01-20',
    review_scores_rating: 4.75,
    review_scores_accuracy: 4.25,
    review_scores_cleanliness: 4.75,
    review_scores_checkin: 4.67,
    review_scores_communication: 4.75,
    review_scores_location: 3.67,
    review_scores_value: 5,
    license: '',
    instant_bookable: 'f',
    calculated_host_listings_count: 1,
    calculated_host_listings_count_entire_homes: 0,
    calculated_host_listings_count_private_rooms: 1,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 0.05
  },
  {
    _id: ObjectId("643ad82124ed4983860f1215"),
    id: 157612,
    listing_url: 'https://www.airbnb.com/rooms/157612',
    scrape_id: Long("20230327145459"),
    last_scraped: '2023-03-27',
    source: 'city scrape',
    name: 'New attic space/single & Dble room',
    description: 'The loft space is a small but cosy, private and secure semi independent flat, with good views across Manchester and Salford. A shared front door entrance up to the 2nd floor comprises of mini kitchen/lounge,  bathroom. 2 bedrooms for up to 3 guest.<br /><br /><b>The space</b><br />A new private loft conversion is available in Salford. This is the perfect place to stay if  you want the be  near Salford Quays and Manchester city centre, as both are just a short journey  away. There is a safe cycle track from the house going straight into Manchester  centre (about 10 minutes)<br /><br />The recently renovated loft  is a comfortable double or single room and comes with a  mini kitchen, bathroom and lounge area. The space is clean, cosy and comes furnished with a TV and wireless internet. Welcome snacks are provided for light breakfast. This is a great place for those who want privacy plus (for longer stays) you get use of the washer, secluded garden and there is  parking.  Would ideally su',
    neighborhood_overview: 'There is a public park within easy walking distance. Shops and transport are also local and easily accessible. Manchester town centre and Salford Quays are about 2 miles away. There is a local swimming pool/leisure centre and library with community facilities.',
    picture_url: 'https://a0.muscache.com/pictures/18150718/745ae3aa_original.jpg',
    host_id: 757016,
    host_url: 'https://www.airbnb.com/users/show/757016',
    host_name: 'Margaret',
    host_since: '2011-06-29',
    host_location: 'Salford, United Kingdom',
    host_about: 'Hi we are Tom and Margaret. retired Engineer and Social Worker.\n' +
      'We like to spend our free time travelling and socialising with friends and family. Also meeting people through Air bnb has been a very interesting experience. \n' +
      'Tom enjoys keeping busy with DIY and gardening. We are active walkers and like to holiday abroad  \n',
    host_response_time: 'within a day',
    host_response_rate: '100%',
    host_acceptance_rate: '81%',
    host_is_superhost: 't',
    host_thumbnail_url: 'https://a0.muscache.com/im/users/757016/profile_pic/1369149741/original.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/users/757016/profile_pic/1369149741/original.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: '',
    host_listings_count: 1,
    host_total_listings_count: 3,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: 't',
    host_identity_verified: 't',
    neighbourhood: 'Salford, United Kingdom',
    neighbourhood_cleansed: 'Salford District',
    neighbourhood_group_cleansed: 'Salford',
    latitude: 53.50114,
    longitude: -2.26429,
    property_type: 'Entire loft',
    room_type: 'Entire home/apt',
    accommodates: 3,
    bathrooms: '',
    bathrooms_text: '1.5 baths',
    bedrooms: 2,
    beds: 2,
    amenities: '["Iron", "Self check-in", "Shampoo", "Toaster", "Books and reading material", "Body soap", "HDTV", "Hot water kettle", "Oven", "First aid kit", "City skyline view", "Conditioner", "Essentials", "Hangers", "Smoke alarm", "Dishes and silverware", "Bikes", "Wine glasses", "Lockbox", "Bed linens", "Breakfast", "Central heating", "Hot water", "Carbon monoxide alarm", "Wifi", "Outdoor furniture", "Dedicated workspace", "Free driveway parking on premises", "Cooking basics", "Private backyard \\u2013 Fully fenced", "Hair dryer", "Microwave", "Luggage dropoff allowed", "Fire extinguisher", "Refrigerator", "Dining table", "Free street parking", "Extra pillows and blankets", "Cleaning products", "Drying rack for clothing", "Coffee", "Long term stays allowed", "Free washer", "Shower gel", "Room-darkening shades", "Kitchen", "Clothing storage: closet and dresser"]',
    price: '$41.00',
    minimum_nights: 2,
    maximum_nights: 365,
    minimum_minimum_nights: 2,
    maximum_minimum_nights: 2,
    minimum_maximum_nights: 365,
    maximum_maximum_nights: 365,
    minimum_nights_avg_ntm: 2,
    maximum_nights_avg_ntm: 365,
    calendar_updated: '',
    has_availability: 't',
    availability_30: 11,
    availability_60: 20,
    availability_90: 37,
    availability_365: 282,
    calendar_last_scraped: '2023-03-27',
    number_of_reviews: 123,
    number_of_reviews_ltm: 20,
    number_of_reviews_l30d: 2,
    first_review: '2012-02-13',
    last_review: '2023-03-12',
    review_scores_rating: 4.92,
    review_scores_accuracy: 4.93,
    review_scores_cleanliness: 4.93,
    review_scores_checkin: 4.98,
    review_scores_communication: 4.94,
    review_scores_location: 4.66,
    review_scores_value: 4.92,
    license: '',
    instant_bookable: 'f',
    calculated_host_listings_count: 1,
    calculated_host_listings_count_entire_homes: 1,
    calculated_host_listings_count_private_rooms: 0,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 0.91
  }

```
1. Find all restaurants in a particular genre (pick any genre as an example) with 3 stars or more, ordered by the number of stars in descending order.
```
SELECT * FROM restaurants WHERE rate_stars >= 3 AND category = 'Polish' ORDER BY rate_stars DESC;
```
1. Find all restaurants that are open now (see hint below).
```
SELECT * FROM restaurants WHERE strftime('%H:%M', 'now') BETWEEN opening AND closing;
```
1. Leave a review for a restaurant (pick any restaurant as an example).
```
INSERT INTO review (review_id, restaur_id, reviews, rating)
VALUES(1, 5, 'Food was ok, table was dirty.', 3);
```
1. Delete all restaurants that are not good for kids.
```
DELETE FROM restaurants WHERE kids = 'false';
```
1. Find the number of restaurants in each NYC neighborhood.
```
SELECT neighborhood, COUNT(*) FROM restaurants GROUP BY neighborhood;
```
## Part 2
Social media users table code:
```
CREATE TABLE user(
    id INTEGER PRIMARY KEY,
    email TEXT NOT NULL,
    password TEXT NOT NULL,
    handle TEXT NOT NULL
);
```
User post table code:
```
CREATE TABLE post(
    id INTEGER PRIMARY KEY,
    post_type TEXT NOT NULL,
    invisible TEXT NOT NULL,
    posts TEXT NOT NULL,
    user_from INTEGER NOT NULL,
    user_to INTEGER NOT NULL,
    time TEXT NOT NULL
);
```
This [user data](data/user.csv) and [post data](data/post.csv) were generated from [mockaroo.com](https://mockaroo.com/), and are 1000 rows of random users and post datas.

Data set for user was imported with this code:
```
.mode csv
.header on
.import data/user.csv user
```
Data set for post was imported with this code:
```
.import data/post.csv post
```
### Queries

1. Register a new User.
``` 
INSERT INTO user(email, password, handle) 
VALUES('jk6240@nyu.edu', 'djdfsnkne', 'jk6240');
```
1. Create a new Message sent by a particular User to a particular User (pick any two Users for example).
```
INSERT INTO post(post_type, invisible, posts, user_from, user_to, time)
VALUES('message', 'visible', 'hello how are you', '343', '231', '7:34');
```
1. Create a new Story by a particular User (pick any User for example).
```
INSERT INTO post(id, post_type, invisible, posts, user_from, user_to, time)
VALUES('1001, 'story', 'visible', 'time for a new mukbang', '342', '0', '12:33');
```
1. Show the 10 most recent visible Messages and Stories, in order of recency.
```
SELECT * FROM post WHERE invisible = 'visible' ORDER BY time DESC LIMIT 10;
```
1. Show the 10 most recent visible Messages sent by a particular User to a particular User (pick any two Users for example), in order of recency.
```
SELECT * FROM post WHERE post_type = 'message' AND user_from = '344' AND user_to = '343' ORDER BY time DESC LIMIT 10;
```
1. Make all Stories that are more than 24 hours old invisible.
```
UPDATE post SET invisible = 'invisible' WHERE post_type = 'story' AND ROUND((JULIANDAY('now') - JULIANDAY('2021-02-21 12:50:00')) * 24) > 24;
```
1. Show all invisible Messages and Stories, in order of recency.
```
SELECT * FROM post WHERE invisible = 'invisible' ORDER BY time DESC;
```
1. Show the number of posts by each User.
```
SELECT user_from, COUNT(*) FROM post GROUP BY user_from;
```
1. Show the post text and email address of all posts and the User who made them within the last 24 hours.
```
SELECT post.posts, user.email, user.id FROM post LEFT JOIN user ON user.id = post.user_from WHERE ROUND((JULIANDAY('now') - JULIANDAY('2021-02-21 12:50:00')) * 24) > 24;
```
1. Show the email addresses of all Users who have not posted anything yet.
```
SELECT user.email, user.id FROM user LEFT JOIN post ON user.id = post.user_from WHERE posts = '' GROUP BY user.id;
```
