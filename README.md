Tado-SmartThings integration

Tado (Connect): Smartapp and device Types to enable more smart thermostat's capabilities within SmartThings

Author: Stuart Buchanan


/*********************************************************************************************

Setup time: approximately about 5 minutes

PREREQUISITES

Your Tado Devices fully operational (and connected to wifi)
Your Tado credentials (username/password)
Developer access to SmartThings (e.g. http://graph.api.smartthings.com/)
Location set for your ST account
Under the ST mobile app, click on the 3-horizontal lines- "hamburger"- menu in the upper right corner, and then the "gear'" icon to review your location.

Determine your shard, please consult this thread:
https://community.smartthings.com/t/faq-how-to-find-out-what-shard-cloud-slice-ide-url-your-account-location-is-on/53923

If you are on a different shard, you need to change the links below for your right shard. As an example, in North America,

e.g. replace https://graph.api.smartthings.com/ide/apps by https://graph-na02-useast1.api.smartthings.com/ide/apps

INSTALLATION STEPS

For those with GitHub integration you can add my repository
Namespace:	fuzzysb
Repository:	Tado
Branch:	master

You need to update from Repo the Tado Connect Smart app and the three Device Types.

then select your SmartApp and then:

a) click the App Settings Button at the top right corner (in the code window)

b) click the OAuth link and then click on the Enable OAuth in Smart App Button

c) click the Update Button at the bottom left

d) Go back to the code window, and hit the "publish/for me" button at the top right corner

All Complete.

For those without Github integration please do the following steps

/*********************************************************************************************

1) Create new device Handlers

/*********************************************************************************************

a) Go to https://graph.api.smartthings.com/ide/devices

b) Hit the "+New Device Handler" at the top right corner

c) Hit the "From Code" tab on the left corner

d) Copy and paste the code from https://github.com/fuzzysb/Tado/blob/master/devicetypes/fuzzysb/tado-heating-thermostat.src/tado-heating-thermostat.groovy

e) Hit the create button at the bottom

f) Hit the "publish/for me" button at the top right corner (in the code window)

Complete steps a - e again for each of the following device Types

https://github.com/fuzzysb/Tado/blob/master/devicetypes/fuzzysb/tado-cooling-thermostat.src/tado-cooling-thermostat.groovy

https://github.com/fuzzysb/Tado/blob/master/devicetypes/fuzzysb/tado-hot-water-control.src/tado-hot-water-control.groovy

https://github.com/fuzzysb/Tado/blob/master/devicetypes/fuzzysb/tado-user-presence.src/tado-user-presence.groovy


/*********************************************************************************************

2) Create a Smart App (Tado (Connect))

/*********************************************************************************************

a) Go to https://graph.api.smartthings.com/ide/apps

b) Hit the "+New SmartApp" at the top right corner

c) Hit the "From Code" tab on the left corner

d) Copy and paste the code from https://github.com/fuzzysb/Tado/blob/master/smartapps/fuzzysb/tado-connect.src/tado-connect.groovy

e) Hit the create button at the bottom

f) Hit the "publish/for me" button at the top right corner (in the code window)

g) click the App Settings Button at the top right corner (in the code window)

h) click the OAuth link and then click on the Enable OAuth in Smart App Button

i) click the Update Button at the bottom left

g) Go back to the code window, and hit the "publish/for me" button at the top right corner

/*********************************************************************************************

3) Connect Smartthings to Tado

/*********************************************************************************************

You should already have an tado username and password, if not go to https://my.tado.com/webapp/#/account/sign-in and create a new login

Go through the authentication process using Tado (Connect)

If you get a blank screen after pressing 'Next or you get the following error: " Error - bad state. Unable to complete page configuration", you'd need to enable oAuth as specified in step 2h) above.

After being connected, click 'Next' and select your Tado device(s) (Heating, Cooling, Radiator Valves) that you want to control from Smartthings and, then press 'Next'

next enter the default heating and cooling temperatures to be used when a Setpoint has not been selected and also enter the default tado override method, these are Tado-Mode which applies the override only until the next Tado mode change, or manual which will apply the override until cancelled by the User

once complete you now have devices that have been created for each of the devices you selected during setup, you should enter the Tado (Connect) smartapp to add or delete these devices.

/*********************************************************************************************

4) Your device(s) should now be ready to process your commands

/*********************************************************************************************

You should see your device under

https://graph.api.smartthings.com/device/list

And

In the ST app, under myHome/Things.

countless hours have been devoted to developing this smartapp and connected devices. if you use and find useful please donate to aid further development of this product. any and all donations are very much appreciated.

https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CNRR3ER3CTYDQ
