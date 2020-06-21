# Intern-Assignment-Full-Throttle
# Model
- In models.py, i created two models of user and activity_period with respective fields as follows
   ## user
   - id(user_id) as a primary key : To be unique and prevents duplicates
   - tz(time_zone)
   - name
   ## activity_period 
   - start_time
   - end_time
   - user_id as a foreign key : From user model we take user_id as frogienkey, this provides us the unique identification of the activity_periods fields which are associated with the user_id

# Serialization
  - The data is in JSON format and the data needs to serialized so that i created a serialization model in a serializers.py file, in which two models which are UserSerializer and ActivityPeriodSerializer.
   ## UserSerializer
   - Fields : user_id, name, time_zone, activity_period
   - Create function
   #ActivityPeriodSerializer
   - Fields : start_time, End_time
# View
- In views.py, i created a UsersView in this i created the following methods
  ## post
  - In the model UserSerializer the inputs are user_id, real_name, time_zone, Activiy_periods where the activity_periods are in the form of nested JSON to post the data it needs to be added to the server one at a time with respect to the user_id so i created a create method which does the work. 
  ## get
  - In the get method user_id is passed and the representation of the user_id of the specified field is retrieved from the server data. 
  ## delete
  - In the delete method user_id is passed the representation of the specified field is erased from the server data
  
  # Screenshots:
  
  ## POST
  ![create user](https://raw.githubusercontent.com/g-m-b/Full-Throttle-Intern-Assignment/master/screenshots/create_user.png)
  
  ## GET
  ![get_user](https://raw.githubusercontent.com/g-m-b/Full-Throttle-Intern-Assignment/master/screenshots/get_user.png)
  
  ## DELETE
  ![delete_user](https://raw.githubusercontent.com/g-m-b/Full-Throttle-Intern-Assignment/master/screenshots/delete_user.png)
