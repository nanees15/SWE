# SWE

### Functional Requirements

#### 1. Confirm / reject request:

* Description / Action:
    * Driver shall be able to confirm or reject a ride after receiving a request

* Requirements / Inputs:
    * driver have to open the application and wait for a request.

* Source:
    * Source is Driver.

* Pre-Condition:
    * Driver must apply to be a driver.
    * Driver must log in ??
    * Driver must state that he is available / can get requests

* Post-Condition:
    * if driver confirmed request, system should increment driver's number of rides

* Output:
    * If driver confirmed the request, the ride should start, pickup location should appear and driver should head to it.
    Otherwise, the system should match driver with another ride.

***

#### 2. Cancel ride:

* Description / Action:
    * The driver & rider shall be able to cancel the ride at any time.

* Requirements / Inputs:
    * Rider/Driver should click on "cancel ride" button
    * specify the reason why he/she want to cancel the ride from checkbox and if he/she chose "other", then he/she can write in text field.

* Source:
    * The Source can be DRIVER or USER

* Pre-Condition:
    * Rider must register an account. / Driver must apply to be a driver.
    * Driver/rider must log in ??
    * Rider must click on Book a ride, be matched with a driver and the ride start.
    * Checking the number of cancels the driver/rider made through the day.
    If it exceeds the maximum allowed number of cancels per day,
      the driver/rider should be informed that if cancellation done he/she will pay a fine.

* Post-Condition:
    * System should increment driver/rider 's number of cancels 

* Output:
    * The one who cancelled will be able to specify the reason he/she cancelled, and then return to the main widget.   ?????

***

#### 3. Report / Help:

* Description / Action:
    * Driver/Rider shall be able to report for a situation or for lost/found personal belongings

* Requirements / Inputs:
    ##### must specify which user. Driver/rider or support
    ###### In case of Driver/rider:
        * In order to start, driver/rider must specify the topic which can be:
            1. issue with account
                * all possible problems are stated with their solutions.
                * he/she can follow the guideline for his/her problem.
            2. help with a trip
                * he/she should choose the trip, see trip's details and should click on one button of:
                    * find/lost item
                    * report safety issue
                    * provide driver feedback
                    * get help 
                * any button would initiate a customer support chat with options,
                    driver/rider should report for what they want and follow the guidline.
            3. guide
                * include all needed information about the application
        
    ###### In case of Support:
        * Support can review reports and take the appropriate decision.
* Source:
    * Source can be DRIVER, RIDER or SUPPORT

* Pre-Condition:
    * Rider must register an account. / Driver must apply to be a driver.
    * Driver/rider must log in ??
    * Open account-page and click on help/report button.

* Post-Condition:
    * system should notify that there is a new report

* Output:
    * if report is under evaluation, a message will be displayed(Thank you for reporting, we will get back to you soon!).
    * if issue is solved nothing will appear.

***

#### 3. GIS:

* Description / Action:
    * 

* Requirements / Inputs:
    * 

* Source:
    * 

* Pre-Condition:
    * 

* Post-Condition:
    * 

* Output:
    * 

*** 

#### 4. Rentals:

* Description / Action:
    * 

* Requirements / Inputs:
    * 

* Source:
    * 

* Pre-Condition:
    * 

* Post-Condition:
    * 

* Output:
    * 
