# SWE
## A. User Requirements:

*	The System should enable the user to book a ride to anywhere & at any time.
* A user (driver) shall be able to confirm / reject request while being on online mode.
* He (driver / rider) can cancel the trip by specifying the reason. 
*	User (driver / rider) can report about an issue or lost item during the trip to the help center and support will guide them in the process.
*	A user (rider) shall be able to rent a car with his driving liscence.
*	Hr can review the drivers applications to accept or decline them.
*	He (driver / rider) shall be able to login to the application to start booking a ride.
*	User (driver) can choose the driver mode that he desire.
*	A user (rider / driver) shall be to register into the application.
* A user can apply for the application to be a driver.
*	I (rider) can edit/update my trip like change the destination or add multiple stops .
* The system should provide different payment method in the application like cash , wallets , credit cards.
*	User ( rider) also can contact with driver or the support.
*	A user (rider / driver) shall be to view the history of rides. 
*	The user feels free to give a rating about driver or the trip or vise versa .
* guarantee user safety like adding real-time tracking .
* the user should be able to see his history of rides .


***

## B. Functional Requirements

### 1. manage request:

* Description / Action:
    * Driver shall be able to confirm or reject a ride after receiving a request

* Requirements / Inputs:
    * trip information which includes pick-up, drop-off location, cost, estimated time and type of trip which can be a reserved trip or instant trip.

* Source:
    * Source is System.

* Pre-Condition:
    * Driver must have chosen online mode which enable him to receive requests.

* Post-Condition:
    * if driver confirmed request, system should increment driver's number of rides
    * if driver rejected request, match will be executed again.

* Output:
    * If driver confirmed the request, the ride should start, pickup location, rider info and estimated time should appear and driver should head to it.
    Otherwise, system displays other requests

---

### 2. Cancel ride:

* Description / Action:
    * The driver/rider shall be able to cancel the ride

* Requirements / Inputs:
    * trip information
    * the reason why driver/rider wants to cancel the ride

* Source:
    * system and driver/rider

* Pre-Condition:
    * Rider must have Booked a ride, be matched with a driver and the ride started.
    * Checking the number of cancels the driver/rider made through the day.
    If it exceeds the maximum allowed number of cancels per day,
      the driver/rider should be informed that if he/she cancels the drive, he/she will pay a fine.

* Post-Condition:
    * System should increment driver/rider 's number of cancels 

* Output:
    * message that confirms the cancellation
---

### 3. Help:

* Description / Action:
    * Driver/Rider shall be able to report for a situation or for lost/found personal belongings.
    * support can review reports and take the appropriate decision.

* Requirements / Inputs: string halala(---------){}
    * rider/driver information
    * type of report which can be issue with account, help with a trip and guide.

    <!-- ##### must specify which user. Driver/rider or support
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
                * include all needed information about the application -->
        
    <!-- ###### In case of Support:
        * Support can review reports and take the appropriate decision. -->
* Source:
    * Source can be driver/rider and system

* Pre-Condition:
    *

* Post-Condition:
    * system should notify customer support that there is a new report

* Output:
    * a message states that report state is pending till support contacts the reporter.

---
### 4. match :
    
    * Description / Action:
        * rider is matched with a driver that is within the area .

    * Requirements / Inputs:
        * pick-up location, driver location, driver information

    * Source:
        * system

    * Pre-Condition:
        * rider must have booked a ride.
        * driver must have chosen online mode.

    * Post-Condition:
        * 

    * Output:
        * rider and driver will be matched and each one will view other's information

---

### 4. generate path:
    
    * Description / Action:
        * this functionality generates path according to pick-up location and drop-off location of the ride.

    * Requirements / Inputs:
        * pick-up location, drop-off location

    * Source:
        * system

    * Pre-Condition:
        * rider must have booked a ride.

    * Post-Condition:
        *

    * Output:
        * path is generated and is displayed for rider and driver

---

<!-- ### 4. GIS:
*TO BE ADDED :
 he must choose between these:
    1- only one dest 
    2- multi dest with no wait time 
    3- with waiting time 
    
    
* Description / Action:
    * driver/rider/customer support shall be able to open the maps integrated in the application and track the car and route.

* Requirements / Inputs:
    * pick-up and drop-off locations.
    * support can view map and track rides.

* Source:
    * db & user

* Pre-Condition:
    *

* Post-Condition:
    * --

* Output:
    * map is displayed

--- -->

### 5. rent car:

* Description / Action:
    * Rider shall be able to rent a car for himself to use it and return it back at the agreed time.

* Requirements / Inputs:
    * renting duration, rider information and driving license

* Source:
    * rider

* Pre-Condition:
    * Rider should have enough money in his wallet/visa in order to make this functionality start.
    * Rider can use this functionality once his rating stars are greater than 3.

* Post-Condition:
    * system should track the car & make sure the rider returned the car at the agreed time.
    * if the rider is late, rider will be charged a fine that increases every hour that passes. 

* Output:
    * confirmation message 

---


### 7. track live location:

* Description / Action:
    * monitor the current whereabouts of the car during the trip .

* Requirements / Inputs:
    * the location of car .

* Source:
    * system 

* Pre-Condition:
    * the trip must start first .

* Post-Condition:
    * the postion of the car will be shown/drawn on the map .

* Output:
    * the car with the route to destination will be shown on the map and could be shared to other platforms .

---

### 7. evaluate job application:

* Description / Action:
    * Hr shall be able to review applicant's application, evaluate it and take the appropriate decision.

* Requirements / Inputs:
    * job application

* Source:
    * system

* Pre-Condition:
    * there must be at leaset one application

* Post-Condition:
    * if driver is accepted, he should be able to use the application as a driver & his data should be added to database.
    * if there is missing data in the application, email is sent to the applicant
    * status of application is changed from pending into finished

* Output:
    * an email is sent to the desired person states if he is accepted or not, depend on Hr's evaluation.

---

### 8. Log in:

* Description / Action:
    * rider/driver/support shall be able to log in with his valid email and passcode

* Requirements / Inputs:
    * driver/rider/support 's phone number or email, password

* Source:
    * driver/rider

* Pre-Condition:
    * driver/rider must have an account first

* Post-Condition:
    * rider/driver/support 's data should be retrieved from database.

* Output:
    * if data is valid, driver/rider will be logged in successfully. Otherwise, message states that there is something that is incorrect.

---

### 9. change mode:

* Description / Action:
    * driver shall be able to choose between online and offline modes. In online mode, driver can receive requests. Otherwise, driver cannot receive requests

* Requirements / Inputs:
    * state of driver, driver info

* Source:
    * driver, system

* Pre-Condition:
    * driver can't change his mode to offline while he is in ongoing ride.

* Post-Condition:
    * In online mode, receiving requests will be enabled.
    * In offline mode, receiving requests will be disabled.

* Output:
    * message states that mode is switched

***

* register :
   
    * action : create an account for the user 
    * inputs : mail , password , phone number and username .
    * source :  by the rider .
    * pre-condition : the user must be a rider . 
    * post-condition : the user data will successfully be added to our database .
    * output : rider features will be enabled to the user .

---

 * fill job application :
    regarding age,
    
    * action : enable the user to use the app as a driver .
    * inputs : mail , username, phone number , age , password and more info about the cat and its owner like driver’s license status, driving experience ,driving history ,criminal record, provide proof of residency, along with proof of auto insurance , car registration and car insurance coverage.
    * source : through a form filled by the driver.
    * pre-condition : the driver data should be valid like the car license . ??
    * new pre : nothing 
    * post-condition : the driver application will be added to the system with status "pending" untill evaluation ends . 
    * output : the driver will receive a message to endicate a sucessfull application , awaiting screen will appear until the status changes to "accepted".

---

* book a ride :
  
    * action : 
        * enable the customer to book a trip defining a source and destination points considering adding multiple stops.
        * calculate cost and estimated time.
    * inputs : pick-up and drop-off points from the map .
    * source : form filled by the user .
    * pre-condition: the user must have an account and logged in succesfully .
    * post-condition: the app will look for the nearest cars around the customer area . 
    * output : the trip will start once there is a match and path is shown on the map .

---
* edit trip :
   
    * action : enabling the user to access and change in his trip like changing the destination , add multiple stops and path and change payment method in the current trip.
    * inputs : new drop-off location , other payment method , choose multiple locations for stops.
    * source : by the user  .
    * pre-condition : the trip must start first .
    * post-condition: the trip will get altered (the trip attributes/ specification will get altered to the user likes ).
    * output : the trip will get altered to the user likes .

---

* manage wallet :
    
     * action : enabling multiple methods for payment like cash , wallets , credit cards , payment services for the user to choose for an example the driver/rider should add/ remove card , the support should access the payment method during the trip in case of emergency situations . 
     * inputs :  choosing from these methods and extra info for credit card info .
     * source : user 
     * pre-condition :the user must have an account and logged in succesfully .
     * post-condition : The new payment method is successfully added to the user's account and is available for use when making a ride booking. 
     * output : The user can now select the newly added payment method as their preferred option when booking a ride. The payment will be processed using the account information provided during the setup process.

---

* contact :
     
     * action : enable the user to communicate with the dirver after the match through chat or calls . 
     * inputs :  phone number of both from the database , messages from both .
     * source: user , database
     * pre-condition : the match must happen first , good internet connection .
     * post-condition: A chat starts between both sides and have the access to eachother phone  number .
     * output : a chat is opened if they choose to communicate through chat .

---

* access history :
     
     * action : show the history of rides in detail for the user .
     * inputs :  price , pick-up , drop-off points , driver name .
     * source: database
     * pre-condition : the trip must be completed successfully .
     * post-condition: nothing
     * output : the user will be able to see all previous trips in detail . 

---

* rate :
     * action : enable the user to give his feedback and rate the driver / cutomer .
     * inputs : numerical rating or score, choosing from a scale of 1 to 5 . 
     * source: user 
     * pre-condition : the trip must end first 
     * post-condition: the new rate of the user will be calculated .
     * output : update the rating of the user .
---
* show profile info :
     * action : enable the user to show the profile info of others  .
     * inputs : id or name of the user . 
     * source: database .
     * pre-condition : both the user viewing and the user being viewed must have an account on the platform . 
     * post-condition:  more data will get fetched from the user table in the database .
     * output : the user profile will be showed to the viewer .

 * select multiple destination :
     * action : enable the user to add multiple stops in his trip .
     * inputs : multiple locations from the map. 
     * source: user .
     * pre-condition : the user must have an account and logged in succesfully and in the process of booking a trip . 
     * post-condition:  the trip specifications will get updated and the driver will get notified with the changes.
     * output : multiple stops will be shown in the trip map .
***

## C. Non-functional Requirements:
