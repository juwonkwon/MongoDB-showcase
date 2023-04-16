# AirBnB MongoDB Analysis

This [airbnb listings](data/listings.csv) was obtained from the airbnb website. It contains information on Great Manchester, UK area listings in CSV format. No scrubbing seemed necessary, as the existence of other datas did not seem to bother the results from the mongodb queries.

1. show exactly two documents from the listings collection in any order
code:
```
db.listings.find().limit(2);
```
result:
```
{ _id: ObjectId("643ad82124ed4983860f1217"), id: 4468181, listing_url: 'https://www.airbnb.com/rooms/4468181', scrape_id: Long("20230327145459"), last_scraped: '2023-03-27', source: 'city scrape', name: 'Double Room in shared apartment', description: 'Close to Motorway links, free on street public parking, within 10 mins walk from Tram, Media city within 20 mins on tram. Monton bars/restaurants within 10 mins walk. Room includes Single Divan Bed, Memory foam Mattress, Wardrobe, Bedside cabinet, Chest of Drawers, Table Lamp, Drop leaf table and chair. The apartment is shared with one tenant and Landlord, common areas include bathroom, Lounge/Dining area and Hallway.<br /><br /><b>The space</b><br />Make yourself at home, use the kitchen and cooking facilities. Towels and bedding provided.<br /><br /><b>Guest access</b><br />Use the Lounge, Hall, Kitchen and bathroom', neighborhood_overview: '', picture_url: 'https://a0.muscache.com/pictures/5284eef5-392d-4148-a9c8-c8ca89081b6f.jpg', host_id: 23182584, host_url: 'https://www.airbnb.com/users/show/23182584', host_name: 'Michael', host_since: '2014-10-31', host_location: 'Manchester, United Kingdom', host_about: 'Hi I am an easy going person. I am Irish and like outdoor activities including hiking and cycling. I work as a chartered surveyor in Manchester. I like good friends, family, music and the odd social drink. ', host_response_time: 'N/A', host_response_rate: 'N/A', host_acceptance_rate: 'N/A', host_is_superhost: 'f', host_thumbnail_url: 'https://a0.muscache.com/im/users/23182584/profile_pic/1414768927/original.jpg?aki_policy=profile_small', host_picture_url: 'https://a0.muscache.com/im/users/23182584/profile_pic/1414768927/original.jpg?aki_policy=profile_x_medium', host_neighbourhood: '', host_listings_count: 1, host_total_listings_count: 1, host_verifications: "['email', 'phone']", host_has_profile_pic: 't', host_identity_verified: 'f', neighbourhood: '', neighbourhood_cleansed: 'Salford District', neighbourhood_group_cleansed: 'Salford', latitude: 53.48526, longitude: -2.34232, property_type: 'Private room in rental unit', room_type: 'Private room', accommodates: 1, bathrooms: '', bathrooms_text: '1 bath', bedrooms: 1, beds: 1, amenities: '["Iron", "TV", "Essentials", "Hangers", "Washer", "Smoke alarm", "Lock on bedroom door", "Heating", "Wifi", "Kitchen"]', price: '$100.00', minimum_nights: 2, maximum_nights: 14, minimum_minimum_nights: 2, maximum_minimum_nights: 2, minimum_maximum_nights: 14, maximum_maximum_nights: 14, minimum_nights_avg_ntm: 2, maximum_nights_avg_ntm: 14, calendar_updated: '', has_availability: 't', availability_30: 29, availability_60: 59, availability_90: 89, availability_365: 364, calendar_last_scraped: '2023-03-27', number_of_reviews: 4, number_of_reviews_ltm: 0, number_of_reviews_l30d: 0, first_review: '2016-10-06', last_review: '2017-01-20', review_scores_rating: 4.75, review_scores_accuracy: 4.25, review_scores_cleanliness: 4.75, review_scores_checkin: 4.67, review_scores_communication: 4.75, review_scores_location: 3.67, review_scores_value: 5, license: '', instant_bookable: 'f', calculated_host_listings_count: 1, calculated_host_listings_count_entire_homes: 0, calculated_host_listings_count_private_rooms: 1, calculated_host_listings_count_shared_rooms: 0, reviews_per_month: 0.05 }, 

{ _id: ObjectId("643ad82124ed4983860f1215"), id: 157612, listing_url: 'https://www.airbnb.com/rooms/157612', scrape_id: Long("20230327145459"), last_scraped: '2023-03-27', source: 'city scrape', name: 'New attic space/single & Dble room', description: 'The loft space is a small but cosy, private and secure semi independent flat, with good views across Manchester and Salford. A shared front door entrance up to the 2nd floor comprises of mini kitchen/lounge,  bathroom. 2 bedrooms for up to 3 guest.<br /><br /><b>The space</b><br />A new private loft conversion is available in Salford. This is the perfect place to stay if  you want the be  near Salford Quays and Manchester city centre, as both are just a short journey  away. There is a safe cycle track from the house going straight into Manchester  centre (about 10 minutes)<br /><br />The recently renovated loft  is a comfortable double or single room and comes with a  mini kitchen, bathroom and lounge area. The space is clean, cosy and comes furnished with a TV and wireless internet. Welcome snacks are provided for light breakfast. This is a great place for those who want privacy plus (for longer stays) you get use of the washer, secluded garden and there is  parking.  Would ideally su', neighborhood_overview: 'There is a public park within easy walking distance. Shops and transport are also local and easily accessible. Manchester town centre and Salford Quays are about 2 miles away. There is a local swimming pool/leisure centre and library with community facilities.', picture_url: 'https://a0.muscache.com/pictures/18150718/745ae3aa_original.jpg', host_id: 757016, host_url: 'https://www.airbnb.com/users/show/757016', host_name: 'Margaret', host_since: '2011-06-29', host_location: 'Salford, United Kingdom', host_about: 'Hi we are Tom and Margaret. retired Engineer and Social Worker.\n' + 'We like to spend our free time travelling and socialising with friends and family. Also meeting people through Air bnb has been a very interesting experience. \n' + 'Tom enjoys keeping busy with DIY and gardening. We are active walkers and like to holiday abroad  \n', host_response_time: 'within a day', host_response_rate: '100%', host_acceptance_rate: '81%', host_is_superhost: 't', host_thumbnail_url: 'https://a0.muscache.com/im/users/757016/profile_pic/1369149741/original.jpg?aki_policy=profile_small', host_picture_url: 'https://a0.muscache.com/im/users/757016/profile_pic/1369149741/original.jpg?aki_policy=profile_x_medium', host_neighbourhood: '', host_listings_count: 1, host_total_listings_count: 3, host_verifications: "['email', 'phone']", host_has_profile_pic: 't', host_identity_verified: 't', neighbourhood: 'Salford, United Kingdom', neighbourhood_cleansed: 'Salford District', neighbourhood_group_cleansed: 'Salford', latitude: 53.50114, longitude: -2.26429, property_type: 'Entire loft', room_type: 'Entire home/apt', accommodates: 3, bathrooms: '', bathrooms_text: '1.5 baths', bedrooms: 2, beds: 2, amenities: '["Iron", "Self check-in", "Shampoo", "Toaster", "Books and reading material", "Body soap", "HDTV", "Hot water kettle", "Oven", "First aid kit", "City skyline view", "Conditioner", "Essentials", "Hangers", "Smoke alarm", "Dishes and silverware", "Bikes", "Wine glasses", "Lockbox", "Bed linens", "Breakfast", "Central heating", "Hot water", "Carbon monoxide alarm", "Wifi", "Outdoor furniture", "Dedicated workspace", "Free driveway parking on premises", "Cooking basics", "Private backyard \\u2013 Fully fenced", "Hair dryer", "Microwave", "Luggage dropoff allowed", "Fire extinguisher", "Refrigerator", "Dining table", "Free street parking", "Extra pillows and blankets", "Cleaning products", "Drying rack for clothing", "Coffee", "Long term stays allowed", "Free washer", "Shower gel", "Room-darkening shades", "Kitchen", "Clothing storage: closet and dresser"]', price: '$41.00', minimum_nights: 2, maximum_nights: 365, minimum_minimum_nights: 2, maximum_minimum_nights: 2, minimum_maximum_nights: 365, maximum_maximum_nights: 365, minimum_nights_avg_ntm: 2, maximum_nights_avg_ntm: 365, calendar_updated: '', has_availability: 't', availability_30: 11, availability_60: 20, availability_90: 37, availability_365: 282, calendar_last_scraped: '2023-03-27', number_of_reviews: 123, number_of_reviews_ltm: 20, number_of_reviews_l30d: 2, first_review: '2012-02-13', last_review: '2023-03-12', review_scores_rating: 4.92, review_scores_accuracy: 4.93, review_scores_cleanliness: 4.93, review_scores_checkin: 4.98, review_scores_communication: 4.94, review_scores_location: 4.66, review_scores_value: 4.92, license: '', instant_bookable: 'f', calculated_host_listings_count: 1, calculated_host_listings_count_entire_homes: 1, calculated_host_listings_count_private_rooms: 0, calculated_host_listings_count_shared_rooms: 0, reviews_per_month: 0.91 }
```
1. show exactly 10 documents in any order, but "prettyprint" in easier to read format, using the pretty() function.
code:
```
db.listings.find().limit(10).pretty();
```
first three findings:
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
  },
  {
    _id: ObjectId("643ad82124ed4983860f1216"),
    id: 1241309,
    listing_url: 'https://www.airbnb.com/rooms/1241309',
    scrape_id: Long("20230327145459"),
    last_scraped: '2023-03-27',
    source: 'city scrape',
    name: '★Glass Roof★Walkable★Full Kitch★Office★Deck★Garden',
    description: '✔︎Walk Score 75 (most errands can be accomplished on foot)<br />✔︎ Fully equipped + stocked kitchen<br />✔︎ Onsite washer + dryer<br />✔︎ Extremely safe neighborhood<br />✔︎ Parking is available on street outside the property<br />✔︎ Rear deck + garden to rear of property<br /><br />➠ 2 min stroll to local shops and park<br />➠ 10 min walk to Sale Town Centre<br />➠ 2 min walk to Ashton-on-Mersey village<br />➠ Sale Metrolink into Manchester City Centre journey time 8 mins<br />➠ 20 min drive to Manchester City Centre<br /><br /><b>The space</b><br />To the rear of the property there is a small, enclosed decked area with a lawned garden beyond (note the garden is not fully enclosed - for those of you travelling with adventurous toddlers).<br /><br />Ground Floor<br />• Entrance<br />• Living space<br />• Lounge and dining area (with TV, DVD hard drive recorder and telephone/answerphone)<br />• Fully equipped kitchen (with all appliances including washer/dryer & dishwasher)<br />• Offic',
    neighborhood_overview: 'You will find my personal recommendations in my Guidebook.',
    picture_url: 'https://a0.muscache.com/pictures/miso/Hosting-1241309/original/cfa01cd1-6aac-4757-9886-2a165fadb068.jpeg',
    host_id: 6766640,
    host_url: 'https://www.airbnb.com/users/show/6766640',
    host_name: 'Amy',
    host_since: '2013-06-06',
    host_location: 'Sale, United Kingdom',
    host_about: "I've lived here all my life and I love Airbnb.  \n" +
      ' \n' +
      "That means you'll get high service and local recommendations!  \n" +
      ' \n' +
      'Feel free to book or message me first, happy to answer any specific questions in advance.  \n' +
      ' \n' +
      'By day, I am a small business owner.  \n' +
      ' \n' +
      'By night, I enjoy reading, and preparing extravagant meals.  \n' +
      ' \n' +
      'I am a well traveled Airbnb guest. I know what a host should do to create a comfortable guest experience. My favorite countries visited: Australia, Canada, USA, Germany ',
    host_response_time: 'within an hour',
    host_response_rate: '100%',
    host_acceptance_rate: '53%',
    host_is_superhost: 't',
    host_thumbnail_url: 'https://a0.muscache.com/im/pictures/user/eb6d0834-0f21-4c98-88ef-1562704b287f.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/pictures/user/eb6d0834-0f21-4c98-88ef-1562704b287f.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: '',
    host_listings_count: 3,
    host_total_listings_count: 6,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: 't',
    host_identity_verified: 't',
    neighbourhood: 'Sale, Greater Manchester, United Kingdom',
    neighbourhood_cleansed: 'Trafford District',
    neighbourhood_group_cleansed: 'Trafford',
    latitude: 53.42985,
    longitude: -2.34018,
    property_type: 'Entire home',
    room_type: 'Entire home/apt',
    accommodates: 4,
    bathrooms: '',
    bathrooms_text: '1 bath',
    bedrooms: 2,
    beds: 3,
    amenities: '["Iron", "Dryer", "Shampoo", "Patio or balcony", "Coffee maker", "Baking sheet", "Oven", "First aid kit", "Pack \\u2019n play/Travel crib", "Dishes and silverware", "Essentials", "Hangers", "TV", "Smoke alarm", "Crib", "Bed linens", "Heating", "Children\\u2019s books and toys", "Stove", "Washer", "Bathtub", "Hot water", "High chair", "Carbon monoxide alarm", "Baby bath", "Wifi", "Dedicated workspace", "Outlet covers", "Cooking basics", "Hair dryer", "Microwave", "Dishwasher", "Fire extinguisher", "Backyard", "Refrigerator", "Free street parking", "Extra pillows and blankets", "Long term stays allowed", "Children\\u2019s dinnerware", "Shower gel", "Baby safety gates", "Private entrance", "Kitchen", "Room-darkening shades"]',
    price: '$100.00',
    minimum_nights: 7,
    maximum_nights: 365,
    minimum_minimum_nights: 7,
    maximum_minimum_nights: 7,
    minimum_maximum_nights: 365,
    maximum_maximum_nights: 365,
    minimum_nights_avg_ntm: 7,
    maximum_nights_avg_ntm: 365,
    calendar_updated: '',
    has_availability: 't',
    availability_30: 0,
    availability_60: 17,
    availability_90: 47,
    availability_365: 47,
    calendar_last_scraped: '2023-03-27',
    number_of_reviews: 1,
    number_of_reviews_ltm: 0,
    number_of_reviews_l30d: 0,
    first_review: '2021-11-30',
    last_review: '2021-11-30',
    review_scores_rating: 5,
    review_scores_accuracy: 5,
    review_scores_cleanliness: 5,
    review_scores_checkin: 5,
    review_scores_communication: 5,
    review_scores_location: 4,
    review_scores_value: 4,
    license: '',
    instant_bookable: 'f',
    calculated_host_listings_count: 3,
    calculated_host_listings_count_entire_homes: 3,
    calculated_host_listings_count_private_rooms: 0,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 0.06
  }
```
1. choose two hosts (by reffering to their host_id values) who are superhosts (available in the host_is_superhost field), and show all of the listings offered by both of the two hosts
code:
```
db.listings.find( {host_is_superhost: "t"} , {host_id: 1});
```
chose host id 757016 and 6766640:
```
db.listings.find({ $or:[ {"host_id":757016}, {"host_id":6766640}] }, {_id:0,name:1,price:1,neighbourhood:1,host_name:1,host_is_superhost:1}).pretty();
```
first three findings:
```
{
    name: 'New attic space/single & Dble room',
    host_name: 'Margaret',
    host_is_superhost: 't',
    neighbourhood: 'Salford, United Kingdom',
    price: '$41.00'
  },
  {
    name: '★Glass Roof★Walkable★Full Kitch★Office★Deck★Garden',
    host_name: 'Amy',
    host_is_superhost: 't',
    neighbourhood: 'Sale, Greater Manchester, United Kingdom',
    price: '$100.00'
  },
  {
    name: 'Bright, Light and Calm Two Bedroom Townhouse, M33',
    host_name: 'Amy',
    host_is_superhost: 't',
    neighbourhood: 'Greater Manchester, England, United Kingdom',
    price: '$139.00'
  },
  {
    name: 'Spacious Calm 3 bedroom house with deck & parking.',
    host_name: 'Amy',
    host_is_superhost: 't',
    neighbourhood: '',
    price: '$139.00'
  }
```
1. find all the unique host_name values (see the docs)
code:
```
db.listings.distinct("host_name");
```
first three findings:
```
'A',
  'A-K',
  'Aabhas',
  'Aadil',
  'Aaisha',
  'Aamir',
  'Aaron',
  'Aaron & Silvina',
  'Ab',
  'Abbas',
  'Abbey',
  'Abby',
  'Abdolreza',
  'Abdul',
  'Abdul Haseeb',
  'Abdul Wali',
  'Abdulbadea',
  'Abdullah',
  'Abdulrahman',
  'Abdurahman',
  'Abi',
  'Abiodun',...
```
1. find all of the places that have more than 2 beds in a neighborhood of your choice (referred to as either the neighborhood or neighbourhood_group_cleansed fields in the data file), ordered by review_scores_rating descending
code:
```
db.listings.distinct("neighbourhood_group_cleansed");
db.listings.find({ neighbourhood_group_cleansed: "Wigan", beds:{$gt:2}},{_id:0,name:1,beds:1,review_scores_rating:1,price:1}).sort({review_scores_rating:-1}).pretty();
```
first three findings:
```
{
    name: '3 bedroom flat for students or professionals',
    beds: 4,
    price: '$600.00',
    review_scores_rating: ''
  },
  {
    name: 'Spacious 3 Bedroom House (Leigh)',
    beds: 6,
    price: '$300.00',
    review_scores_rating: ''
  },
  {
    name: 'Spacious and Delightful - Sunshine Cottage',
    beds: 4,
    price: '$201.00',
    review_scores_rating: ''
  }
```
findings show that if there are no score, it is just a blank field.
1. show the number of listings per host
code:
```
db.listings.aggregate([{$group: {_id:"$host_name",listings:{$sum:1}}}]);
```
first three findings:
```
{ _id: 'Arthur', listings: 1 },
  { _id: 'Sili', listings: 1 },
  { _id: 'Rahim', listings: 1 },
  { _id: 'Alberto', listings: 1 },
  { _id: 'Riz', listings: 1 }
```
findings show that most hosts have one listing each.
1. find the average review_scores_rating per neighborhood, and only show the ones above a 95, sorted in descending order of rating (see the docs)
code:
```
let groupByNight = {$group:{_id:"$neighbourhood",minNight:{$avg:"$minimum_nights"}}};
let matchGT = {$match: {minNight:{$gt:7}}};
let sortByAvg = {$sort: {minNight: -1}};

db.listings.aggregate(groupByNight, matchGT, sortByAvg);
```
first three findings:
```
  { _id: 'Oldham, Aberdeenshire, United Kingdom', minNight: 999 },
  {
    _id: 'Denshaw, England, United Kingdom',
    minNight: 334.3333333333333
  },
  { _id: 'Altrincham, Cheshire, United Kingdom', minNight: 28 },
  { _id: 'Greater Manchester, United Kingdom', minNight: 25.25 },
  { _id: 'England, United Kingdom', minNight: 24 },
  { _id: 'Manchester , Manchester, United Kingdom', minNight: 18 },
  { _id: 'Royton, England, United Kingdom', minNight: 15.5 },
  {
    _id: 'Chorlton-Cum-Hardy, Manchester, United Kingdom',
    minNight: 14
  },
  { _id: 'Middleton, England, United Kingdom', minNight: 11.6 },
  { _id: 'Whalley Range, England, United Kingdom', minNight: 8 },
  {
    _id: 'Atherton, England, United Kingdom',
    minNight: 7.333333333333333
  },
  {
    _id: 'Manchester, England, United Kingdom',
    minNight: 7.025974025974026
  }
```
For this problem, the original query had no returnings, so it was modified to contain minimum nights and
aggregated by minimum night greater than 7 descending listings. This returned that default value could be 999, as there cannot be airbnbs that request 999 nights.
