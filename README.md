# SB-YT-Points-System
Streamer.Bot YouTube Basic Points System

## TUTORIAL
(coming soon to a YouTube near you)


## IMPORT

Get the import code from the file:
**YT Points System Streamerbot.txt**

## INSTALLATION
In Streamerbot select the Import button from the top left menu.
Copy the code from the text file and paste all the text into the Import String field.
There should be 13 actions and 5 Commands
![image](https://user-images.githubusercontent.com/107263697/220808561-e6edda42-d1d2-4ffa-9d91-31bc96f7ddfa.png)



## CONFIGURATION

#### C# Compiler
Make sure to add System.Core.dll to the C# compiler within Settings > C# Compiler > Common References > Right-Click > Add reference from file...

![image](https://user-images.githubusercontent.com/107263697/220821729-181e6c95-874d-4dbe-a19a-4ed0c6afee96.png)
![image](https://user-images.githubusercontent.com/107263697/220821811-1600f1de-0885-4f6f-be13-ac908411f9c1.png)

This will help make sure all the C# code found in the sub-actions compiles.

#### Present Viewers
Set "Action - Assign to Present Viewers Event" to the "Present Viewers" event found in Platforms > YouTube > Events.
![image](https://user-images.githubusercontent.com/107263697/220809514-31515e14-4c8d-4e64-aa75-f1fcaab84920.png)

This will give viewers points every MINUTE. The slider is meant to select how many minutes of inactivity to no longer consider a chatter as "active". For example, 5 minutes means that if the Present Viewers event runs and the chatter hasn't been active for 5 mins 12 secs, then the chatter will no longer be receiving points every minute.
To adjust the points given every minute change the %pointsPerMinute% argument in the action to the number value you want.
![image](https://user-images.githubusercontent.com/107263697/220811414-303ff453-cd39-4084-9f6f-d70ed431d07c.png)


#### First Words
Set "Action - Assign to First Words Event - First Words" to the "First Words" event found in Platforms > YouTube > Events.
![image](https://user-images.githubusercontent.com/107263697/220811960-9f2b8062-347f-4dac-9723-3d7ed356e862.png)

In the action "Action - Assign to First Words Event - First Words":
- Update/Add any users that you don't want triggering the "First Words" event.
![image](https://user-images.githubusercontent.com/107263697/220813034-df2c9299-fec8-4813-b16f-d8976e7aa9bc.png)
- Update/Add any user IDs that you don't want triggering the "First Words" event.
![image](https://user-images.githubusercontent.com/107263697/220813086-ee81be5b-a8d8-4b1d-ae7f-1f9bce7468cb.png)
- If you want brand new chatters to get some extra bonus points for being in your stream for the first time ever you can keep the below sub-action. If you don't want brand new chatters to get bonus points you can delete the following sub-action.
![image](https://user-images.githubusercontent.com/107263697/220812389-54c0e9f7-a99b-42e4-a41b-888f888a33d2.png)
- Update the poins every chatter receives for chatting the first time each stream.
![image](https://user-images.githubusercontent.com/107263697/220813221-0a7684ef-b071-4af7-a9fa-c126df4a493a.png)

In the action "Action - First Words Give Points for NEW Chatters":
- Update the points that brand new chatters receive one time for chatting in your stream for the first time ever.
![image](https://user-images.githubusercontent.com/107263697/220813366-a13ad423-deb3-406a-8c5b-3fde275bd29f.png)

#### Points Name and Command
The !setpointsname command sets the name of your loyalty points to whatever you want to call it. This is the format: 

```!setpointsname[space]["name"]```

```!setpointsname Coins```

In the !setpointsname command:
- Check the "enabled" box
- Go to User Permissions and move your Username to the "Allowed" column. This command should really only be for you because you will need to update the command for users to check their points balance if you ever change the name.
![image](https://user-images.githubusercontent.com/107263697/220817436-a22faad0-102f-49e0-bdd0-3d8d247080b7.png)

- Use the command during a stream to update the name to whatever you choose.
![image](https://user-images.githubusercontent.com/107263697/220817772-f717d07f-2ca5-4c86-92e0-1a4f6eab634a.png)

In the !points command:
- Check the "enabled" box
- Update the command to whatever points name you are using (if desired)
- You can also add a cooldown if you want to avoid people spamming the command
![image](https://user-images.githubusercontent.com/107263697/220817998-7bc10a30-5d6b-4278-a4ed-ea3d6dfe2536.png)
![image](https://user-images.githubusercontent.com/107263697/220818600-83cd509f-9c74-4b79-8b55-7e308c316494.png)



#### Add and Set Points Commands
The !addpoints command adds points to the viewer listed. This is the format: 

```[command][space][username]+[# of points to add]```

``` !addpoints Haunter+100```

You can also use the @ symbol if you are on desktop

``` !addpoints @Haunter+100```

In the !addpoints command:
- Check the "enabled" box
- Update the command to whatever points name you are using (if desired)
- Update the Group Permissions to "Moderators"

![image](https://user-images.githubusercontent.com/107263697/220819263-0b034d10-c5b9-4f5f-9f72-462c9ca090be.png)
![image](https://user-images.githubusercontent.com/107263697/220820224-58dd726c-66b3-4348-a45c-8da364f3bb04.png)

The !setpoints command adds points to the viewer listed. This is the format: 

```[command][space][username]=[# of points to set]```

``` !setpoints Haunter+100```

You can also use the @ symbol if you are on desktop

``` !setpoints @Haunter+100```

In the !setpoints command:
- Check the "enabled" box
- Update the command to whatever points name you are using (if desired)
- Update the Group Permissions to "Moderators"

![image](https://user-images.githubusercontent.com/107263697/220820362-031a96ba-717f-4f75-89f9-8434d2892a4b.png)
![image](https://user-images.githubusercontent.com/107263697/220820541-c7ceac6a-633f-47f8-acb6-0bbba13834ee.png)

PLEASE NOTE! - Due to the fact that YouTube does not require unique usernames, there is a small chance that two viewers with the same username are in your viewer records. If this happens the bot should send a message that there are duplicate usernames. They will have to change their username or get their points added another way.

ADD A PICTURE HERE

#### Shout-Out
The !so command puts a link in chat for the user who was shouted-out. This is the format: 

```!so [username]```

```!so Haunter```

In the !so command:
- Check the "enabled" box
- Update the Group Permissions to "Moderators"

![image](https://user-images.githubusercontent.com/107263697/220821194-fad9b840-4fb3-41ad-9b1f-43b2cf132893.png)
![image](https://user-images.githubusercontent.com/107263697/220821375-de3e650d-2215-48a3-9382-1e38d2fb3725.png)

#### Points Redeem




## EXAMPLE USE




## CONTRIBUTORS




