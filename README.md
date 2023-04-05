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

#### 4. GIS:

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

#### 5. Rentals:

* Description / Action:
    * Rider shall be able to rent a car for himself to use it and return it back at the agreed time.

* Requirements / Inputs:
    * In order to start, rider should click on "rent a car" button, choose the type of car he/she wants from the available ones, specify the time of picking up and dropping off and pay a diposit.

* Source:
    * Source is the Rider(user) & database

* Pre-Condition:
    * Rider should have enough money in his wallet/visa in order to make this functionality start.
    * Rider can use this functionality once his rating stars are greater than 3.

* Post-Condition:
    * system should track the car & make sure the rider returned the car at the agreed time.
    * if the rider is late, rider will be charged a fine that increases every hour that passes. 

* Output:
    * car's location should be displayed & timer begins once the rider takes the car.

***

#### 6. Free drive:

* Description / Action:
    * Rider shall be able to book a ride with no specific destination.

* Requirements / Inputs:
    * rider should click on "Free drive" button, specify the pick up location

* Source:
    * Source is rider.

* Pre-Condition:
    * Rider can use this functionality once his rating stars are greater than 3.

* Post-Condition:
    * 

* Output:
    * Ride starts

#### 7. evaluate driver's application:

* Description / Action:
    * Hr shall be able to review driver's application, evaluate it and take the appropriate decision.

* Requirements / Inputs:
    * hr should be notified that there is a new application, review it and check that that person is qualified to be a driver.

* Source:
    * HR & DB ??

* Pre-Condition:
    * 

* Post-Condition:
    * 

* Output:
    * an email is sent to the desired person states if he is accepted or not, depend on Hr's evaluation.

***

#### 8. Log in:

* Description / Action:
    * driver/rider shall be able to log in with his valid email and passcode

* Requirements / Inputs:
    * driver/rider should enter his email or phone number and passcode.
    * system must compare this data with the data in database

* Source:
    * source is USER and DB? (validate with db?)

* Pre-Condition:
    * driver/rider must have an account first

* Post-Condition:
    * --

* Output:
    * if driver/rider logg in successfully, home page will be displayed. Otherwise, message that states "email or passcode is incorrect" will be displayed

***

#### 9. driver mode:

* Description / Action:
    * driver shall be able to choose his mode

* Requirements / Inputs:
    * driver choose between online and offline modes. In online mode, driver can receive requests. Otherwise, driver cannot receive requests

* Source:
    * Driver

* Pre-Condition:
    * driver can't change his mode to offline while he is in ongoing ride.

* Post-Condition:
    * 

* Output:
    * In case of online mode, searching widget will be displayed till he receives a request.
    * In case of offline mode, nothing changes.
