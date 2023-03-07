# Request Timed Out (There was a problem loading the requested.)

## Fix #1.0 - Devices not on the same WiFi connection. (Most Commonly Suggested) 
To run the application on an iOS phone without manual connection, both the computer and the phone need to be on the same network.

## Fix #2.0 - Devices are on the same Network but...
If the devices are on the same network but is still not running, there could be any number of problems. A strong network connection is recommended.

### Fix #2.1 - Expo connecting to an alteranate IPv4 address.
Check to make sure Expo is using the desired network address.
[See also Fix #3.0]

<h5>References:</h5>
"What you need to do is:
Go to cmd and type "ipconfig" and see which network is using the ip shown in your expo app. if it's not your router IP address then what you need 
to do is to go and disable the network which expo is using:
    Control Panel -> Network and Internet -> Network Connections
    and here disable the network that expo is using. (it should be a LAN network connection)
    try to run "npm start" again, it should be working now.
If my solution is not clear feel free to ask me." - @raminghaderi on Jul 4, 2018 (Github)<br>

<h5>Links:</h5>
https://github.com/expo/create-react-native-app/issues/595#issuecomment-402445528
https://medium.com/@colin_78999/solving-network-response-timed-out-when-using-expo-on-windows-b486c22d5584

### Fix #2.2 - iOS device does not have proper settings enabled.
On your device navigate to Settings -> Expo Go and make sure you've allowed Expo to access your Local Network. Enabling Local Network allows Expo to display the app on your phone trhough use of your local network.

<h5>Links:</h5>
https://github.com/expo/create-react-native-app/issues/595#issuecomment-777223551

### Fix #2.3 - iOS device has the proper network settings.
Newer iOS updates may automatically apply a Private Wi-Fi Address setting that could hinder your app from connectivity to the local network enviorment. On your device navigate to Settings -> Wi-Fi -> [select your network or hit the information button], and disbale the Private Wi-Fi Address setting. This may temporarily interrupt your connection.

## Fix #3.0 - iOS device is not connecting correctly.
[See also Fix #1.0, #2.2, #2.3]
<!---->

## Fix #4.0 - Firewall, VPN, other apps and security features...
Some firewall protections, VPN settings, and other applications on your computer may be preventing access to the local network. Check relevant apps and make sure your connection is allowed.

### Fix #4.1 - Firewall disabling

<h5>References</h5>
"We’ve had people report issues with Windows Firewall blocking LAN urls in the past. Also, some routers don’t support connecting over LAN. You might try:
    Using a different network to see if that network allows it
    Checking your firewall settings (including possible corporate firewall)
    Switching to “tunnel” which will be slower but more likely to connect" - ben Expo Team on May '18 (Expo)

<h5>Links</h5>
https://forums.expo.dev/t/problem-loading-requested-app/9765


### Fix #4.2 - Firewall enabling
In your Firewall settings make sure to allow Node JS (there are sometimes more than one checkboxes) access.

### Fix #4.3 - VPN Settings
Many VPN's will block access to the localhost. Temporarily disbale your VPN or try a workaround.

<h5>Links</h5>
https://medium.com/@triplea1373/react-native-and-nat-problem-4b53462cd0b9
https://justinnoel.dev/2019/12/24/developing-react-native-apps-with-expo-over-a-vpn/

### Fix #4.4 - Various apps

<h5>Links</h5>
https://github.com/expo/create-react-native-app/issues/595#issuecomment-1139265615

### Fix #4.5 Ports

<h5>Links:</h5>
https://ntalam.com/2022/01/30/expo-network-response-time-out-error/#:~:text=To%20solve%20this%20error%20you,%2C%20click%20Run%20%2C%20type%20WF.

## Fix #5 - Various
These solutions are least common and likely will not solve any underlying issues but are worth mentioning. If you're desperate enough you'll try them.

### Fix #5.1 - Login Credintials
When setting up Expo on your computer you should be asked to login to your account. You can register with [npx expo register] or if you have an account already [npx expo login]. The account used in your program should be the same account used on your Expo Go application.

### Fix #5.2 - Odd Pairing
This is a longshot but it's been seen that on some occasions pairing your computer and phone through Bluetooth before scanning the QR code will allow the app to connect. If there is any correlation or if this is random coincidence... dunno.

### Fix #5.3 - Updating
Check to make sure both your Expo Go app, computer, and device are all updated and running the latest of version (or at least a recent compatible version) of Expo.

### Fix #5.4 - Reset Network Driver
In your computer settings, choose to Reset Network Driver. This will cause your computer to restart; after which, you can reconnect to your WiFi and npm start you app.

### Fix #5.5 - Restart / ReDownload
Try restarting your application, computer, or mobile device. You can also try to delete and redownload the Expo Go app.

### Fix #5.6 - Switch to Hotspot connection
Change the network connection and provide a route to the local network by using your mobile hotspot.

<h5>Links</h5>
https://github.com/expo/create-react-native-app/issues/138

<h5>References</h5>
"... if your phone supports "Mobile Hotspot" or "Tethering" try turning one of those on and joining your phone's WiFi network on your computer ..." - @anp on Apr 11, 2017 (Github)