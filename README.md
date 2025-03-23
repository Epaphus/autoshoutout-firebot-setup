## **IN BETA**  

Auto Shoutout and Shoutout queuing system for Firebot made by Epaphus (EpaphusUK On Twitch)    
   
This system will:   
- Auto shouts out raids (Raiders will be put to the front of the queue)  
- Auto shoutout viewers who have the autoshoutout role when they first speak in chat
- Queue up standard "!so" shoutouts 
   
The queue set setup to allow enough time between shoutouts for the Twitch /shoutout command to cool down.   
By default the shoutout queue will be paused for 15 minutes at the start of the steam, this allows time for viewers to build to up so the early birds are not shouted out to themselves.   

For a fresh setup use the file "Auto Shoutout.firebotsetup"  
If updating from an older version please use "Auto Shoutout - Update.firebotsetup", failure to do so will remove all exsting users from the AutoShoutout role.  
   
   
---   
   
### Shoutout command   

This is setup to take the standard "!so Username" command and then adds it to a queue, the queue spaces out the shoutouts so that Twitches /shoutout command has time to cool down and become available again.   
To edit the shoutout message go to Commands and edit the "!so-effect" command.   

The "!so" command runs the "!so-effect" command within the queue at a standard priority, when raid comes in this triggers the "!so-raider" which adds the raiders shoutout to the queue with high priority, this will put them next in the queue if there are already shoutouts in the queue.  


### Adjusting the default queue start timer   

To ajust the default timer from 15 minutes go to Events -> Autoshoutout and edit the "[ASO] Enable SO Queue - Stream Started" event, then change the delay timer and update the chat feed text.   

### Disabling the default queue start timer  

If you would like the queue to run all the time   
Go to Events -> Autoshoutout and disable the "[ASO] Enable SO Queue - Stream Started" event.   
Edit the "[ASO] Clear Auto Shoutout list" and disable the "Pause Shoutout Queue" Run Effect List.

You can also start and stop the queue manually via the "[ASO] Shoutout queue - Start" and "[ASO] Shoutout queue - Stop" Preset Effect Lists and can be controlled via StreamDeck or similar.

