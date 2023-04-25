
# RE-FLEX


## Install

Copy and paste the following command into terminal:
`pip install requests pyaes pbkdf2 yagmail`


## Disclaimer
This is spoofing the Android App, you should be able to use it still if you use iPhone, but when you set the version you are following the Android Version number

**WARNING**!: Never copy the `userdata` folder to another device. If you need to use a different device, have a fresh script with a blank userdata folder and do the sign in process on that device. The challenge link itself can be done anywhere as long as the maplanding is pasted into the script terminal

## Usage
Everything is done from `Script_Dock.py` (double click the script to run it, or type `python Script_Dock.py` in terminal)



## Setup

**Set_App_Version**
Put the latest Android Flex app version here and click save (currently `3.87.2.1.0`)

**Set_User_Agent**
Select a device from the list and click set, or click random. Once set, this button will not be here in the future when running script dock to prevent different user agent devices.

**Choose_Station_Filter:**
Select the stations you want to work at, and click Generate List, you can close this


**Set_Filter_Values:**
Set your filters based on whatever criteria you desire, then click save. 

| Value | Description |
|--|--|
| Headstart | How far (in minutes) in the future a block must be to be considered  |
| Minlength | The minimum block length (in hours) you want to work *(i.e. if set to 3 will not book any 2 hour blocks)* |
| Rate | The hourly block rate you want to work for *(i.e. if set to $20 it will not book blocks paying less per hour)* |
| Lowprice | The lowest total pay you would work a block for *(i.e. if set to $70 it will not book blocks that are paying $54)* |


**Start Main**
Click to start, you may get a message in the console with a long URL. Copy that into your browser and log in with your Flex account. You'll reach a page that says "this page can't be found" - that's OK - copy the URL (will include word "maplanding") and paste back into the terminal that Script_Dock opened with. Scanning will start. Stop scanning using stop button. 


**Check_Logs**

This will let you know if everything is working.

## Setting Up Notifications
You can get notified when a block gets booked for you. The script uses Yagmail, which can be configured in the `yagmail_alert.py` file

Yagmail works with GMail, but requires special setup due to new security rules from Google. 

Go to myaccount.google.com and log in. You must have 2-Factor enabled on your account. If it is not, set it up. Once set up, go to "security" tab on left. Then look on this page for a small button that says "app passwords" under the "signing in with google" section and click that. 

There is a section that says "*select app and device to generate app password for*" - select "other" from dropdown and type in `Yagmail` for name. Click generate and it will give you password. Copy and paste that into `yagmail_alert.py` file, in the space that by default says "apppassword"

Update `"second email"` with the gmail email from the above steps.

Update `"main email"` with an email address to send notifications to (can be non-gmail)
