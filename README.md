# HA-Sleep-Routine
Documentation on the sleep Routine linked to Home Assistant, Node Red, Alexa and iOS. This will dim lights when going to sleep and on wake up will trigger an Alexa Routine that will read my calendar and inform me of the weather. 

1. Start setting configuring the Alarm in iOS using Sleep | Wake up
   
   ![IMG_2233](https://github.com/user-attachments/assets/88dc092c-fc62-474d-b41e-f2502cb7d2df)
   
This defines the time for the wake up and sleep shortcuts that we will be making soon. 

3. Within Home Assitant make a helper (Settings > Devices and Settings > Helper)
4. Select 'Create Helper' and select 'Drop down' and add the following details
   ![image](https://github.com/user-attachments/assets/94533a2c-9fe7-4fc1-938a-55c5cf253581)

5. Within the shortcuts app setup the following shortcuts to update the input select options
   ![IMG_2226](https://github.com/user-attachments/assets/6a994248-cfa0-4245-88c5-e242e50e313c)
   ![IMG_2225](https://github.com/user-attachments/assets/76639be5-a5b5-4e94-ac2b-dce8e80a1928)
   ![IMG_2228](https://github.com/user-attachments/assets/b9a61605-a14a-44e6-aabd-8eeb6cb9ffac)
   ![IMG_2227](https://github.com/user-attachments/assets/72442804-63b2-46e8-b456-d825af827244)

   Note: the 3 second delay in the set awake is so that is does not clash with waking up.
   Note: the reference to plug 2 is if i decide to snooze, it will not repeat the Alexa routine every snooze

6. These shortcuts are then linked to an Automation based on the alarm triggers.
   ![IMG_2230](https://github.com/user-attachments/assets/6a47cce7-352e-4b9c-a3a7-cf7a35a90eb7)
   ![IMG_2232](https://github.com/user-attachments/assets/1cd48e45-3767-4d8a-b190-041998959da2)
   ![IMG_2231](https://github.com/user-attachments/assets/257992a6-5898-4127-b700-d69d97d32608)
   ![IMG_2229](https://github.com/user-attachments/assets/f78c01db-f1c5-4502-b842-dfa1f678a74a)

The Snooze Alarm

I am a person that likes to snooze, and to avoid Alexa running her Routine every 9 min I am using a spare plug as a way to trigger Alexa only when i want. To do that i have have a automation seup with Home Assistant that is triggered when the Sleep status channges from "Bedtime Begins" to "Waking Up"
YAML Code for automation is attched to project. 

The Alexa Routine

The Alexa routine is triggered when the Plug powered on, I did try using a virtual switch but for some reason it would not work. 
  ![Alexa Routine](https://github.com/user-attachments/assets/8453e9b4-8e85-4433-b006-b4b7c4503165)





