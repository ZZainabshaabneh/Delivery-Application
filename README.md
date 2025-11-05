# Delivery-Application

## About the Project

TaxiApp is an integrated system, similar to Uber, designed to connect drivers and passengers in real time.

The app provides a user-friendly interface that allows passengers to request rides and enables drivers to track requests and their precise location.

# Key Features
### For Passengers:

Create an account and log in.

Request a ride and specify the destination using your location.

Track the driver's real-time location on the map.

Receive alerts when a request is accepted or when the driver arrives.

View details of previous trips (date, price, time, driver).

# For Drivers:

Log in and receive new requests.

Accept or decline trips.

Automatically send your location to the server every few seconds to update your vehicle's position.

Automatically calculate distance, time, and cost.

Communicate with passengers through the system.

## Technical Aspects
### Front End (Android App)

Language: Java

Environment: Android Studio

Technical Features:

Location tracking using LocationManager and LocationListener.

Sending updates to the server every 3 seconds via Handler.

Running the service in the background using Foreground Service.

Using WebSocket or API Gateway to communicate with the server in real time.

Storing data locally using SharedPreferences.

### Back End

#### Technologies:

AWS Lambda for serverless request processing.

API Gateway as the application interface.

DynamoDB for storing user, trip, and location data.


### System Flow

A passenger requests a ride through the app.

The request is sent to the server (API Gateway → Lambda → DynamoDB).

The driver receives the request in their app and chooses to accept or decline.

Upon acceptance, the system begins sending the driver's location every 3 seconds to track the trip.

After the trip ends, the fare is calculated and the data is sent to the server for storage and later display.

### Tools Used

Android Studio

Java

AWS Lambda

API Gateway

DynamoDB

WebSocket

JSON

SharedPreferences

