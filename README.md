Develope a http microservice called number management service taht exposes a get rest api "/numbers" this api receives a list of url through query parameters this query param is called "url" it can appear more than once. when api/numbers is called your service shall retrieve each of these urls if they turn out to be syntactically valid urls each url will return a json data structure that looks like this: "numbers": [2,3,5,7,11,13].

Below are the acceptance criteria :

collect response from each valid URLs
merge integers received from each URLs
sort them in ascending order and ensure each integer appears only once
return response to the caller like
{
    "numbers": [merged unique integers]
}
your service must return the response as quickly as possible (never later than 500 milliseconds)

If remote URL takes too long to respond, it must be ignored. The timeout must be respected regardless of the size of the data.
