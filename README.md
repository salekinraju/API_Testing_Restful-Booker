# API_Testing_Restful-Booker
This is a project on an API testing site [Restful-Booker](http://restful-booker.herokuapp.com/), where users can get, create, update, and delete bookings. To do that, respective HTTP requests GET, POST, PUT, and DELETE are used in Postman with the appropriate base and relative URL.

## Testing Process

+ **Create Booking Info:** To create bookings, the POST HTTP method is used and in the pre-request script, random variables are set and saved in the environment. These variables can be used throughout all the APIs randomly without needing to edit every value manually.<br>
![create_booking](https://github.com/salekinraju/API_Testing_Restful-Booker/assets/58147883/d5438fda-ba5a-466d-80d6-d1341ec98a0e)

+ **Get the Created Booking Info:** To get the created booking info, the GET HTTP method is used and several API tests are conducted to verify the status code and validate the data received in the response body against stored environment variables. <br>
![get_booking](https://github.com/salekinraju/API_Testing_Restful-Booker/assets/58147883/fcca99fc-0744-4ff8-80ee-3bc6643d06ae)

+ **Create a Token to Update and Delete Bookings:** To update and delete bookings, a token needs to be generated. The token is created by providing the username and password within the body of a POST HTTP request, and this token is subsequently stored in the environment using variables.<br>
![create_token](https://github.com/salekinraju/API_Testing_Restful-Booker/assets/58147883/56c297a3-0284-4852-a82c-4a3611f3373c)

+ **Update the Booking Info:** The PUT method in the HTTP request is used in this context to replace the existing Booking data with new information. To grant authorization for updates, the token is automatically included in the header, sourced from a previously stored variable in the environment.<br>
![update_booking](https://github.com/salekinraju/API_Testing_Restful-Booker/assets/58147883/ed1391e0-210e-4215-835c-9f1836c23401)

+ **Get the Updated Booking Info:** To get the updated booking info, the GET HTTP method is used again, and again several API tests are conducted to verify the status code and validate the data. <br>
![get_booking_copy](https://github.com/salekinraju/API_Testing_Restful-Booker/assets/58147883/69d9c6e5-de15-481a-8cbd-cf2862621821)

+ **Delete the Booking Info:** The DELETE method is used to delete the booking info associated with the ID. And again the created token is used here for deletion permission. <br>
![delete_booking](https://github.com/salekinraju/API_Testing_Restful-Booker/assets/58147883/20a6c511-c22b-4ad8-9638-b598cbfa71b3)

## Report Generation using Newman
To generate Newman reports, the API collection and API environment are exported into a folder and in the exported folder directory, the following command line is used to generate the Newman report:<br>
newman run Restful-Booker_Salekin.postman_collection.json -e Restful-Booker_Salekin_Environment.postman_environment.json -r cli,htmlextra <br>
![07 10 2023_04 57 25_REC](https://github.com/salekinraju/API_Testing_Restful-Booker/assets/58147883/a43e15a8-e406-4a4f-9611-fc49234407a0)

## Technologies used in the project:

+ Postman
+ Newman
