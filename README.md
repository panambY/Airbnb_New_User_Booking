# Airbnb_New_User_Booking
Where will a new guest book their first travel experience?

<p align="center">
  <img src="https://github.com/panambY/Airbnb_New_User_Booking/blob/master/image/airbnb_new_user_booking.jpg">
</p>

Instead of waking to overlooked "Do not disturb" signs, <a href="https://www.airbnb.com/">Airbnb</a> travelers find themselves rising with the birds in a whimsical treehouse, having their morning coffee on the deck of a houseboat, or cooking a shared regional breakfast with their hosts.

New users on Airbnb can book a place to stay in 34,000+ cities across 190+ countries. By accurately predicting where a new user will book their first travel experience, Airbnb can share more personalized content with their community, decrease the average time to first booking, and better forecast demand.

In this recruiting competition, Airbnb challenges you to predict in which country a new user will make his or her first booking. Kagglers who impress with their answer (and an explanation of how they got there) will be considered for an interview for the opportunity to join Airbnb's <a href="https://www.airbnb.com/careers/departments/data-science-analytics">Data Science and Analytics team</a>.

## Data Description

In this challenge, you are given a list of users along with their demographics, web session records, and some summary statistics. You are asked to predict which country a new user's first booking destination will be. All the users in this dataset are from the USA.

There are 12 possible outcomes of the destination country: 'US', 'FR', 'CA', 'GB', 'ES', 'IT', 'PT', 'NL','DE', 'AU', 'NDF' (no destination found), and 'other'. Please note that 'NDF' is different from 'other' because 'other' means there was a booking, but is to a country not included in the list, while 'NDF' means there wasn't a booking.

The training and test sets are split by dates. In the test set, you will predict all the new users with first activities after 7/1/2014 (note: this is updated on 12/5/15 when the competition restarted). In the sessions dataset, the data only dates back to 1/1/2014, while the users dataset dates back to 2010. 

## File descriptions

- train_users.csv - the training set of users <br>
- test_users.csv - the test set of users <br>
-- id: user id <br>
-- date_account_created: the date of account creation <br>
-- timestamp_first_active: timestamp of the first activity, note that it can be earlier than date_account_created or date_first_booking because a user can search before signing up <br>
-- date_first_booking: date of first booking <br>
-- gender <br>
-- age <br>
-- signup_method <br>
-- signup_flow: the page a user came to signup up from <br>
-- language: international language preference <br>
-- affiliate_channel: what kind of paid marketing <br>
-- affiliate_provider: where the marketing is e.g. google, craigslist, other <br>
-- first_affiliate_tracked: whats the first marketing the user interacted with before the signing up <br>
-- signup_app <br>
-- first_device_type <br>
-- first_browser <br>
-- country_destination: this is the target variable you are to predict <br>
- sessions.csv - web sessions log for users <br>
-- user_id: to be joined with the column 'id' in users table <br>
-- action <br>
-- action_type <br>
-- action_detail <br>
-- device_type <br>
-- secs_elapsed <br>
- countries.csv - summary statistics of destination countries in this dataset and their locations <br>
- age_gender_bkts.csv - summary statistics of users' age group, gender, country of destination <br>
- sample_submission.csv - correct format for submitting your predictions <br>
