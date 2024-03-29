# Live Bus Tracking Application
Description: An application developed to enable parents of school going children to track their buses real time as well as receive SMS notification informing them about successful and unsuccessful boarding by their children.  

## Installation:  
1.	Clone the repository and run npm i
2.	Run node app.js or npm test
3.	Parent Side UI address : http://localhost:4300/ParentApp/parentLanding.html
4.	Driver Side UI address : http://localhost:4300/DriverApp/driverLanding.html

## Architecture:
Server side built using Node.js (Express.js framework) and UI developed using HTML5, CSS, JS and Jquery. The Database is managed on MySQL. 
Chat rooms built using Socket.io library                                                                                                       Tests written using Mocha framework and Chai assertion library
Map API used: - Google
SMS API used: - Way2Sms

### Routes

/FindAllParentsSendNotification : Given two lists of students who have boarded and those who haven't,it fetches their respective parent phone numbers from the DB to send them success/failure SMS

/UpdateConductorRouteInfo : Given Bus number and shift, it returns its respective route id

/getConductorDetailsUsingRoute : Given route id, it returns the list of bus stops and the list of students associate with every bus stop.

/UpdateParentRouteInfo : Given phone number of parent, it returns the respective route id.

/GetAllStops : returns all bus stops stored in redis or if absent on redis, from the DB.

## Usage:
	                                                                    			                     
### Driver Side Landing Page 
![Screenshot (136)](https://user-images.githubusercontent.com/31110940/73436807-2fc49800-4371-11ea-8a15-aa9202853aa9.png)

### Parent Side Landing Page	
![Screenshot (138)](https://user-images.githubusercontent.com/31110940/73436851-47038580-4371-11ea-8873-cd288ab81e7f.png)

Post entering a bus No and shift the driver will be able to see a list of all stops and respective students from each Stop. He/she will mark all the students that have boarded and submit. This will send a “successfully boarded” message to their parents and “boarding unsuccessful” message to the rest of the parents.
After entering the registered phone number and child name (in case of multiple children) the parent will see a live tracking of the bus their child has boarded. 

### Driver Navigation Page
![dnav](https://user-images.githubusercontent.com/31110940/73436731-14598d00-4371-11ea-9862-96f15eafdef0.jpg)

### Parent Navigation Page
![Tracking on map](https://user-images.githubusercontent.com/31110940/73436880-54b90b00-4371-11ea-8276-82f08522a0e7.png)

 Authors/Contributors
1.	Gudia Rani
2.	Nitin Jhajharia















 


