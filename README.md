# TMS OnConnect API

This library is a simple wrapper for the TMS OnConnect API by Gracenote.
Each method returns a "thenable" object.

## Alert

> These APIs are not yet stable. I expect them to change until this alert is removed. Apologies in advance.

## Usage
This library is build on top of Bluebird and uses promises heavily.

```javascript
var api = new Gracenote(api_key);

api.lineups.find().then(function(response){
    
    //... do something with response.

});

//or

api.lineups.find()
    .then(doSometing)
    .then(doSometingElse)
    .then(finallyDoSometing);
```

## Implemented:

- Prorgrams
    - `api.programs`
        - `.search(query, params)`
- Lineups
    - `api.lineups`
        - `.find`
        - `.details`
        - `.channels`
        - `.grid`
- Shows
    - `api.shows`
        - `.newTonight`
        - `.details`
        - `.airings`
- Series
    - `api.series`
        - `.details`
        - `.airings`
- Stations
    - `api.stations`
        - `.details`
        - `.airings`

## TODO:

- Public Plan Methods
- Programs
- Series (episodes)
- Movies On TV
- Movies In Theatres
- Movies Trailers
- Sports
- Celebrities
- Video and Social APIs
