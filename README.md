# Backend Developer Coding Test

Be sure to read **all** of this document carefully, and follow the guidelines within.

## Problem Description

Lomis have been deployed into the world and now we need to keep track of cycles and aggregate data for analysis.

## Requirements

You will develop a ***REST API***  which will store information about the lomi cycles

In order to accomplish this, the API must fulfill the following use cases:

- **POST to store a lomi to the database**

  A lomi must have
            
    1. lomiId
    2. nickname
    3. serialNumber
    4. manufactureDate

  **Sample Post Request**
  ```   
    POST /lomi

    Body
    {
        nickname: "test-lomi
        serialNumber: 12356789
        manufactureDate: 20220822
    }
  ```
    **Sample Response**
    ```
        Body
        {
            lomiId: 10
        }
    ```
    

- **POST lomi cycle information**

    a lomi must have the ability to post information on the latest cycle that was ran.

    **Sample POST Request**
    
    ```
    POST /cycle

    Body
    {
        lomiId: 10
        datatime: '2011-10-05T14:48:00.000Z'
        powerused: 1.1
        weightreduced: 2
    }
    ```
    

- **Reports**

  The API must offer the following reporting endpoints:

    1. Power consumption filterable by lomi id and date range
        **Sample Request**
        ```
            GET /reports/power?lomiid=10&datefrom=20220822&dateto=20220830
        ```
        **Sample Response:**
        ```
            {
                lomiId: 10
                dateFrom: 20220822
                dateTo: 20220830
                powerUsed: 40
            }
            
        ```
    1. Weight reduced filterable by lomi id and date range
         **Sample Request**
        ```
            GET /reports/weight?lomiid=10&datefrom=20220822&dateto=20220830
        ```
        **Sample Response:**
        ```
            {
                lomiId: 10
                dateFrom: 20220822
                dateTo:20220830
                weightReduced: 500
            }
            
        ```

---------------------------------------
## Submission
Please upload your code to a git repository and email us a link
Include any instructions needed to build/run your project

---------------------------------------

## Notes

1. You can use your language and framework of choice, bonus points for serverless js/ts project
2. No authentication is needed 
3. We care about proper programming and architecture techniques, so factor that in
4. Please don't spend more than few hours on this.
5. Please send us any questions you have
