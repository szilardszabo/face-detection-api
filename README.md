API Reference
 
Overview
 
We're building a Face Recognition platform that lets you quickly integrate human identity features into your products and services—it's speedy, safe, and secure.

Kairos is a simple concept—you submit images into our API, and our deep learning algorithms analyze the faces found, then the API returns a bunch of useful data about the faces we find. You can use this to search, match and compare faces, or measure characteristics such as age, and gender.

 

 
Note: We have provided sample APP_KEY, APP_ID, and image URLs in the sandbox. Please replace with your keys / images during development.

 
Help and Support
 
We'd love to hear feedback from you and we're also here to help if you have any challenges. We have lots of answers to popular questions in our FAQ. Failing that, feel free to contact our support team.

 
Get Started with Face Recognition
Overview
Detect human faces in photos and images. Kairos returns information on facial features as coordinates on the image.

Base URL
api.kairos.com
Authentication
Requests must be authenticated with your API key. This must be sent as an HTTP header:

app_id:  "YOUR APP_ID"
app_key: "YOUR APP_KEY"
You can create and manage your API Keys via your dashboard. It's free to sign-up and start testing.

Requests
Requests return a JSON object with the header:

Content-Type: application/json
Usage
It's free to sign-up and start testing.

POST /enroll
