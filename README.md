Distance Function – Nearest Road Distance
📌 Project Overview

Distance Function is a Java-based cloud function that calculates the nearest main road for a given geographic location (latitude and longitude). It uses the Google Maps API to fetch nearby road data and compute the closest road accurately. The application is designed to run as a serverless service using Google Cloud Run / Google Cloud Functions.

🛠️ Technologies Used

Java 

Google Cloud Functions Framework

Google Maps Services API

Google Cloud Run

Maven

Gson (JSON parsing)

SLF4J (logging)

📂 Project Structure
nearest-road-distance
│
├── pom.xml
├── src/main/java/functions
│   ├── Background.java
│   ├── Function.java
│   ├── LocationRequest.java
│   ├── RoadDetails.java
│   ├── RoadResponse.java
│   └── NearestRoadDistance.java
└── README.md

🧩 File Descriptions

NearestRoadDistance.java
Entry point of the cloud function. Handles incoming requests and orchestrates the distance calculation.

Function.java
Implements the Google Cloud Functions interface and processes HTTP requests.

Background.java
Handles background or helper operations required by the function.

LocationRequest.java
Model class representing the input request containing latitude and longitude.

RoadDetails.java
Model class to store details of nearby roads retrieved from Google Maps API.

RoadResponse.java
Model class representing the final response returned to the user.

⚙️ Features

Accepts latitude and longitude as input

Fetches nearby roads using Google Maps API

Calculates the nearest main road

Lightweight and serverless execution

Scales automatically using Google Cloud Run

📥 Input Format (Example)
{
  "latitude": 28.6139,
  "longitude": 77.2090
}

📤 Output Format (Example)
{
  "roadName": "Rajpath Road",
  "distanceInMeters": 120.5
}

🔑 Prerequisites

Java

Maven

Google Cloud account

Google Maps API key

Enabled Google Cloud Functions / Cloud Run

📦 Maven Dependencies

Key dependencies used in this project:

Google Cloud Functions Framework

Google Maps Services API

Gson for JSON handling

SLF4J for logging

🚀 Build & Deployment
Build the Project
mvn clean package


This generates a shaded JAR using the Maven Shade Plugin.

Deploy to Google Cloud

Upload the JAR to Google Cloud

Deploy as a Cloud Function or Cloud Run service

Set the Google Maps API key as an environment variable

🌐 Use Cases

Navigation systems

Logistics and delivery optimization

Location-based analytics

Smart city and mapping applications

📄 License

This project is intended for educational and demonstration purposes. Licensing can be updated based on usage requirements.
