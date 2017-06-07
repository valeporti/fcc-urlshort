# Request Header Parser Microservice API
Free Code Camp APIs URL Shortener Microservice

https://urlshort-vp.herokuapp.com/

## What is this?
This is a microservice API project for Free Code Camp that is intended to return the information of the url requested.

If the url does exist, it shows the "short number" of the url.

If the url doesn't exist, it assigns a "short number" and the shows you the result of the url and its "short number" associated.

If the url is a number associated to an url, it sends you to the respective associated url.

* If you pass a valid url without https or http, it will assign automatically an https to the beginning

## User stories:
1) I can pass a URL as a parameter and I will receive a shortened URL in the JSON response.

2) If I pass an invalid URL that doesn't follow the valid http://www.example.com format, the JSON response will contain an error instead.

3) When I visit that shortened URL, it will redirect me to my original link.

## Usage:
Wrong Entry:
`https://urlshort-vp.herokuapp.com/htts//:good432`

Right Entries:
[`https://urlshort-vp.herokuapp.com/https://www.google.com`](https://urlshort-vp.herokuapp.com/https://www.google.com)

[`https://urlshort-vp.herokuapp.com/www.google.com`](https://urlshort-vp.herokuapp.com/www.google.com)

[`https://urlshort-vp.herokuapp.com/3`](https://urlshort-vp.herokuapp.com/3)     ** as a short URL **

## Example Response:
Error response from Wrong Entry:

`{"error":"Sorry, wrong entry : 'htts//:good432', please try another Url"}`

Response from Right Entries:

`{"long_url":"https://www.google.com","short_url":8}`

`Or... Directly to the requested url page`
