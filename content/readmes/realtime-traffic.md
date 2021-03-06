---
title: realtime-traffic
date: 2020-12-12T08:27:16+0000
draft: false
---
# realtime-traffic

## Backend for the Traffic Analysis Project

### Update Request(on change of traffic light state) (For Python Deveopers)
```
url: https://realtime-traffic.herokuapp.com/post
method: POST
```
#### request structure
```javascript
{
	"lno":"<lane number>",
	"col":"<color of traffic light>",
	"noc":"<number of cars>"
}
```
#### SAMPLE
#### request body
```javascript
{
	"lno":"1",
	"col":"red",
	"noc":"4"
}
```

#### response
```javascript
{
  "message": "success"
}
```


### Front-end Ajax Request (For Front-end Deveopers)
```
url: https://realtime-traffic.herokuapp.com/get
method: GET
```
#### response structure
```javascript
{
  "<lane_number(unique)>": {
    "col": "<color>",
    "noc": "<number of cars>",
    "lno": "<lane number>",
    "status": "<no use on front-end>"
    },
    ...
}
```

#### SAMPLE
#### response
```javascript
{
  "1": {
    "col": "red",
    "noc": "4",
    "lno": "1",
    "status": "sent"
  },
  "45": {
    "col": "yellow",
    "noc": "54",
    "lno": "45",
    "status": "sent"
  }
}
```


