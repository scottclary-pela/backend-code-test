# Backend Developer Coding Test

Be sure to read **all** of this document carefully, and follow the guidelines within.

## Problem Description

Lomis have been deployed into the world and now we need to keep track of cycles and aggregate data for analysis.

## Requirements

You will develop a ***REST API***  which will store information about the lomi cycles

In order to accomplish this, the API must fulfill the following use cases:

- **store a lomi to the database**

  A lomi must have
            
    1. id
    2. nickname
    3. serialnumber
    4. manufactorDate
    

- **POST lomi cycle information**

    a lomi must have the ability to post information on the latest cycle that was ran.

    Example of Cycle POST Request
    
    ```
    {
        lomiId: 10
        datatime: '2011-10-05T14:48:00.000Z'
        powerused: 1.1
        weightreduced: 2
      }
    ```

- **Reports**

  The API must offer the following reports:

    1. Power consumption filterable by lomi id and date range
    2. Weight reduced filterable by lomi id and date range


---------------------------------------

## Notes

1. You can use your language and framework of choice, bonus points for serverless js/ts project
2. No authentication is needed 
3. We care about proper programming and architecture techniques, so factor that in
4. Please don't spend more than few hours on this.
