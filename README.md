# Router-Cluster
Step by step guide on how to make a network cluster made up of old Routers to amplify wifi signal.

# You need at least one extra router

# Step 1:
You need to either plug the old router(s) into the power and connect to it(them)
via wifi or by plugging the ethernet port into both your computer and the router itself. **You will not be able to access an Internet Connection while doing this.**
**If there are any options that your router(s) don't have then just skip the step.**
Finally access the Router's web panel (192.168.x.xxx) find your gateway via the command line there are millions of guides online.
Log in to the panel The user should already be entered if not check the back of your router (in my case user is TELMEX) the passwd is usually the wifi password

**Step 2:** **(CRUCIAL)**
Disable DHCP Server.

This step is usually found in the LAN tab, this step is crucial because the DCHP Server is the one handing out IP's to devices so if any router(s) has the DHCP Server activated it will cause the main router to conflict with other routers.

**Step 3:**
WAN settings
Going to the selected router's WAN settings change connection type to Bridge or Access point (IF YOU DONT DO THIS ONCE YOU CONNECT IT TO THE MAIN ROUTER THE INTERNET WILL BE VERY SLOW,if this option isn't available then skip it) next you want to enable the number of ssids you want to have (in my case 1).

**Step 4:** **CRUCIAL IF YOU WANT TO ACCESS SETTINGS**
Go into the WLAN tab and change each of the router's Gateway IP's (in my case since I live in Mexico and use Infinitum Wifi my default Gateway IP for my main router is 192.168.1.254)
 So make sure to use a different one for each router (excluding your main router
dont change it's ip that would be bad) Since my main router is 192.168.1.254, I changed my other router's IPs to 192.168.1.253 and .252. Once you change that you SHOULD get kicked
off don't worry that's supposed to happen now re-log back in with your new IP.

**Step 5:**
Back to DHCP Settings
You will want to deactivate the option "use a specified range for DHCP" or similar" Next Deactivate DHCP IPv6 Server and finally Deactivate SLAAC This basically lets the router make its own ipv6 addresses which will cause conflicts with the main router if left on because only one can be making addresses.