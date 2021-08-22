# metaweather_api_test_suite #

**Background:**

This test suite tests the MetaWeather API (https://www.metaweather.com/api/). The focus of the suite is testing specific dates with a specific location (using Yahoo's woeid API). Invalid locations and dates have also been added.

**Instructions:**

Before running the test suite, please ensure that you have Node.js and Cypress installed. Instructions on how this is to be done can be found here:

https://docs.cypress.io/guides/getting-started/installing-cypress.html#System-requirements

Afterwards, depending on where the directory with the tests is located, run the following command(s):

cd xxx/meta_weather_api/ node_modules/.bin/cypress open

This should open Cypress for you with the following screen:

![Cypress_](https://user-images.githubusercontent.com/89274203/130360180-d1c1e03b-2411-4e19-81ad-c0a73a3ce0af.png)


**Tests in Cypress:**

In order to the tests, you either select 'Run all specs' or click on the specific test you wish to run.

Here's the follinbg tests:

1. bristol_date_test.spec.js

2. invalid_date_test.spec.js

3. invalid_location_date_test.spec.js

4. london_date_test.spec.js

5. no_location_test.spec.js

6. nottingham_date_test.spec.js

The test related to the requirements is:

**6. nottingham_date_test.spec.js**

**Issues and Bugs**

As setting up Node.js and Cypress took up the longest (issues with sudo and folder permissions), I was not able to find a reliable way on how to test the data returned from the response. Several attempts were made, but more investigation / time would be required 

A bug that was encountered relatively late deals with Javascript's new Date() method. It returns the wrong date which can cause some intermittent failures. I tried to use 'Date.now()' as an argument but it returned the same result. Again, more time and familiarity with Javascript would be required to investigate this further.
