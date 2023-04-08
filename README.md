# SWE
## A. User Requirements:

 * The System helps the user to book a ride to anywhere & at any time.

 * User can contact the driver or customer service for complaints

 * User can also control his trip.

 * User can choose the best payment method for him.

 * A user shall be able to view the history of his rides.

 * A user shall be able to rent a car.

 * The user feels free to give a rating about driver or the trip.

 * A user shall be able to login (register).

 <!-- *  Accepting & decline trip make sure The driver is online  ? -->

 * As a user i can change my destination during the trip.

 * The system provide support help for any problems.

***

## B. Functional Requirements

### 1. Confirm / reject request:

* Description / Action:
    * Driver shall be able to confirm or reject a ride after receiving a request

* Requirements / Inputs:
    * driver have to open the application and wait for a request. // driver mode
    * select confirm button or reject button

* Source:
    * Source is Driver.

* Pre-Condition:
    * Driver must have chosen online mode

* Post-Condition:
    * if driver confirmed request, system should increment driver's number of rides

* Output:
    * If driver confirmed the request, the ride should start, pickup location should appear and driver should head to it.
    Otherwise, the system should match driver with another ride.

---

### 2. Cancel ride:

* Description / Action:
    * The driver, rider and customer support shall be able to cancel the ride at any time.

* Requirements / Inputs:
    * Rider/Driver should click on "cancel ride" button // input
    * specify the reason why he/she want to cancel the ride from checkbox and if he/she chose "other", then he/she can write in text field.
    * support can cancle ride if app is not responding.

* Source:
    * The Source can be DRIVER/rider/customer support

* Pre-Condition:
    * Rider must click on Book a ride, be matched with a driver and the ride start.
    * Checking the number of cancels the driver/rider made through the day.
    If it exceeds the maximum allowed number of cancels per day,
      the driver/rider should be informed that if he/she cancels the drive, he/she will pay a fine.

* Post-Condition:
    * System should increment driver/rider 's number of cancels 

* Output:
    * The one who cancelled will be able to specify the reason he/she cancelled, and then return to the main widget.   ?????

---

### 3. Report / Help:

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
    <!-- * Open account-page and click on help/report button. -->

* Post-Condition:
    * system should notify customer support that there is a new report

* Output:
    * if report is under evaluation, a message will be displayed(Thank you for reporting, we will get back to you soon!).
    * if issue is solved nothing will appear.

---

### 4. GIS:
*TO BE ADDED :
 he must choose between these:
    1- only one dest 
    2- multi dest with no wait time 
    3- with waiting time 
    
    
* Description / Action:
    * driver/rider/customer support shall be able to open the maps integrated in the application and track the car and route.

* Requirements / Inputs:
    * rider/driver can view map, search for a location and select places to review.
    * support can view map and track rides.

* Source:
    * db & user

* Pre-Condition:
    * rider must have started the process of booking a ride
    * rider/driver can view maps while in trip.
    
* Post-Condition:
    * --

* Output:
    * map is displayed

---

### 5. Rentals:

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

---

### 6. Free drive:

// fe hagat hna 
* Description / Action:
    * Rider shall be able to book a ride with no specific destination. / Driver shall be able to choose this mode too.

* Requirements / Inputs:
    <!-- * rider/driver should click on "Free drive" button, rider should contact the available driver and specify the pick up location -->

* Source:
    * Source is rider.

* Pre-Condition:
    * Rider can use this functionality once his rating stars are greater than 3.

* Post-Condition:
    * 

* Output:
    * Ride starts

---

### 7. evaluate driver's application:

* Description / Action:
    * Hr shall be able to review driver's application, evaluate it and take the appropriate decision.

* Requirements / Inputs:
    * hr should be notified that there is a new application, review it and check that that person is qualified to be a driver.

* Source:
    * HR & DB ??

* Pre-Condition:
    * 

* Post-Condition:
    * evaluated application is closed.
    * if driver is accepted, he should be able to use the application as a driver & his data should be added to database.

* Output:
    * an email is sent to the desired person states if he is accepted or not, depend on Hr's evaluation.

---

### 8. Log in:

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
    * app can be used.

* Output:
    * if driver/rider logg in successfully, home page will be displayed. Otherwise, message that states "email or passcode is incorrect" will be displayed

---

### 9. driver mode:

* Description / Action:
    * driver shall be able to choose his mode

* Requirements / Inputs:
    * driver choose between online and offline modes. In online mode, driver can receive requests. Otherwise, driver cannot receive requests

* Source:
    * Driver

* Pre-Condition:
    * driver can't change his mode to offline while he is in ongoing ride.

* Post-Condition:
    * In online mode, receiving requests will be enabled.

* Output:
    * In case of online mode, searching widget will be displayed till he receives a request.
    * In case of offline mode, nothing changes.

***

* register :
   
    * action : create an account for the user 
    * inputs : mail , password , phone number and username .
    * source :  by the rider .
    * pre-condition : type must be rider . 
    * post-condition : the user data will successfully be added to our database .
    * output : rider features will enabled to the user .

---

 * apply :
    
    * action : enable the user to use the app as a driver .
    * inputs : mail , username, phone number , password and car info .
    * source : through a form filled by the driver.
    * pre-condition : the driver data should be valid like the car license .
    * post-condition : the driver application will be added to the system with status "pending" untill evaluation ends . 
    * output : the driver will receive a message to endicate a sucessfull application , awaiting screen will appear until the status changes to "accepted".

---

* book a ride :
    * specify the max time for the multi stops feature 
   - 
    * action : enable the customer to book a trip defining a source and dest points considering adding multi stops  .
    * inputs : pick-up and drop-off points from the map .
    * source : form filled by the user .
    * pre-condition: all the parts of this form should be filled and the match process ends sucessfully .
    * post-condition: the app will look for the nearest cars around the customer area . 
    * output : the trip will start once there is a match .

---
* control trip :
   -
    * action : enabling the user to access and change in his trip like changing the destination , add multiple stops and change payment method.
    * inputs : new drop-off location , other payment method , choose multiple locations for stops.
    * source : through a form from the customer  .
    * pre-condition : the given inputs should be valid .
    * post-condition: the trip will get altered .
    * output : the trip will get altered to the user likes .

---

* payment :
     * to be added 
      consider the driver/rider => add / remove card  
      and support => access the payment method during the trip 
      
     * action : enabling multiple methods for payment like cash , wallets , credit cards , payment services for the use to choose . 
     * inputs :  choosing from these methods and extra info for credit card info .
     * source: user 
     * pre-condition : the user must choose a payment method and for for credit card the card info should be valid .
     * post-condition : The new payment method is successfully added to the user's account and is available for use when making a ride booking. 
     * output : The user can now select the newly added payment method as their preferred option when booking a ride. The payment will be processed using the account information provided during the setup process.

---

* contact :
     
     * action : enable the user to communicate with the dirver after the match through chat or calls . 
     * inputs :  phone number of both from the database , messages from both .
     * source: user , database
     * pre-condition : the match must happen first , good internet connection .
     * post-condition: both sides can communicate with eachother .
     * output : nothing .

---

* history :
     
     * action : show the history of rides in detail for the user .
     * inputs :  price , pick-up , drop-off points , driver name .
     * source: database
     * pre-condition : the trip must be completed successfully .
     * post-condition: nothing
     * output : the user will be able to see all previous trips in detail . 

---

* rating :
     * action : enable the user to give his feedback and rate the driver / cutomer .
     * inputs : numerical rating or score, choosing from a scale of 1 to 5 . 
     * source: user 
     * pre-condition : the trip must end first 
     * post-condition: the new rate of the user will be calculated .
     * output : update the rating of the user .

***

## C. Non-functional Requirements:
