# CarInfoLookupAPI
This is the place where i will be putting the information about the car look up api that i am making, this data is currently under development. 

For now, you can use the link [https://carlookup.server.thomasdye.net/](https://carlookup.server.thomasdye.net/) to try it out and start adding to the DB. 

The API will be free, and will provide all the same information that we do on the web, however right now I am trying to build out the DB and I think the quickest way it to create this web page, that you can use. 
I hope people find this intresting. 

There is no private data here, all data is public in one form or another. I will no doute add to the keys and that over time. 
I have already build some code that will work out with relative accuracy what the type is, eg police car etc. 

![Reflector -2-30-29-3--27-8-24](https://github.com/user-attachments/assets/93a851aa-0250-4ccc-aadc-50920ed73d9e)



# API info 
The Api is a simple post request to the server, that contains a reg, and notes the notes are rquered however can be empty. 

you will get back.

200 code - the data structure of the car info. 
201 code - the reg is not valid in the backend/ we could not find info about that reg.
400 - there was a bad request 
429 - You have hit the rate limit of request by that IP address for the time frame, try waiting a while

``` bash
curl --location 'https://carlookup.server.thomasdye.net/api/v1/lookup' \
--header 'Content-Type: application/json' \
--data '{
    "reg":"oo00ooo",
    "notes":"someinfohere"
}'
```
