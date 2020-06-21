# The Art of Invisibility

## Ch 1 - Your Password Can be Cracked

* Provide clever answers on security questions
* If email is breached
  * Change password
  * Check if there is a forwarding config setup to forward emails to the attacker
* Strong password
  * Use password manager, preferably open-source ones that store data locally on your computer
  * 25 characters minimum in Desktop
  * 7 characters minimum in Mobile
* Enable 2FA
* Use separate device to conduct financial transactions

## Ch 2 - Who Else is Reading Your Email? 

* Use OpenPGP for end to end encryption
* Use Tor browser
* Use a separate device reserved only for anonymous browsing
* Keep anonymous account/device separate from regular browsing
* When creating new email account, use Tor
* Use only free mail server to avoid putting credit card that can be tracked to you
* Use a burner phone for free email registration
  * Pay a random strangers to purchase it
  * Activate only over the Web to avoid being recorded
  * Register with fake address, birth date, etc
* Don't search on while logged in this email 

## Ch 3 - Wiretapping 101

* Your phone is a tracking device
* Using burner phone in close proximity with your real phone will reveal who you are
* 2G networks are not secure, and IoT possibly uses this
* Phones (mobile or landlines) can be tapped easily
* Prefer secure VoIP system

## Ch 4 - If You Don't Encrypt, You're Unequipped

* Expect all mobile carriers to retain your text messages forever
* Use open source messaging app instead of native text message
* Archived data on messaging app often is not encrypted
* Use OTR (off-the-record) messaging app with PFS (perfect forward secrecy)

## Ch 5 - Now You See Me, Now You Don't

* US can charge you for erasing things on your computer (Sarbanes-Oxley Act of 2002)
* Search engine provider can store your search history, what you search today might come back to haunt you tomorrow
  * Turn off personalized search on your search engine provider (i.e., Google account)
  * Use privacy focused search engine (i.e., DDG)
* Avoid collecting those data such as browser history on the first place
* Use plugin HTTPS everywhere on browser
* Disable location tracking on your browser, or spoof it
  * Use proxy with https
  * But beware of free proxies, it can inject malware and can be done legally, read proxy EULA to avoid trap
  * Use Tor browser
* Be careful on syncing devices, it can sync in public computer as well
  * Always sign out after use on public computer
  * Setup different user account on family computer

## Ch 6 - Every Mouse lick You Make, I'll Be Watching You

* Even HTTPS does not encrypt the actual URL string you visit
* Your browser fingerprint is unique and can be used to identify you
  * Check on panopticlick.com 
* Use VM on top of your OS and run your browser inside a VM
* Popups often used for silent tracking, disable popups
* Use plugins to disable script, for example
  * Adblock Plus
  * Ghostery
  * NoScript
  * ScriptBlock
* Have multiple emails for different purposes so online tracker have harder time building your profile
  * For shopping
  * For social media
  * For job/professional purposes
* Use email address that's generic and unrelated to you
  * Don't use your name
  * Don't use your hobby terms
* Clean your cookies
* Don't use OAuth
  * It exposes a lot of data about you
  * When you delete/stop your OAuth provider you lose access to the service account
* Remove useless toolbars because it might contain tracking
* Block Canvas fingerprinting
  * CanvasBlocker
  * CanvasFingerprintBlock
* Credit Card companies flag us if we live use Tor for fraud detection
  * For example if the credit card account says NY but the Tor node says Germany
  * Configure torrec file to use exit nodes located in your home country
  * But don't use the same exit nodes everytime
  
## Ch 7 - Pay Up or Else

* Your WiFi router can be used by strangers to access illegal material therefore pointing the crime to you
* Secure your router with password, at minimum 15 characters
* Update your router firmware often
* Change your default WiFi name to something generic to avoid leaking WiFi model
* Hide the router's SSID entirely
* Use WPA2 or WPA, don't use WEP encryption
* Don't use WPS
* Use whitelisting instead of letting any device enter your router
* Cover your laptop webcam
* Do not click attachments from random stranger's email
* Do not click links from random stranger's email
* Be careful on email from fake websites (fake Facebook, fake Amazon etc)
* Cryptowall is still dangerous and even FBI advise you to pay up

## Ch 8 - Believe Everything, Trust Nothing

* Don't use public WiFi
* Your device usually connected to public WiFi automatically, disable this
* It is legal for someone to intercept traffic on public WiFi
* Use a VPN
  * Read the Privacy Policy of your VPN provider to make sure they don't keep traffic logs
  * Use a VPN that allows TCP for performance
* Turn off your device WiFi when not needed
* Change your device's MAC address every time you connect to a wireless network
* Don't use public PC 
  * Don't sign to your personal account there
  * If you must, delete history, cookies, and empty trash can

## Ch 9 - You Have No Privacy? Get Over It!

* Your digital picture contain metadata including your geographical location
* If you want to take down a digital media of yourself
  * Email "abuse@nameofthesite.com" or "admin@nameofthesite.com" and explain that you don't give permission for it
  * File a DMCA to "dmca@nameofthesite.com" or to the website ISP
* Keep as little as your digital personal information online
* Teach your kids about online social media privacy
* Don't display your birthday
* Don't accept random strangers friend request
  * It can be a scammer
  * It can be a government agency
* Companies, schools, organizations that you joined watch your online presence
* Don't trust companies' privacy policies

## Ch 10 - You Can Run but Not Hide

* Your cellphones/digital wearables are tracking devices even in Airplane mode
* Your face is tracked using facial recognition software on public photos

## Ch 11 - Hey, KITT, Don't Share My Location

* Uber app collect all geolocation data in the background and even when wireless network is off
* Transit systems and toll systems are experimenting with apps and NFC to tag riders
* Use cash to buy transit tickets/pass
* Police and toll photograph your car's license with ALPR technology daily and keep the data for longer than needed
* Rental car has GPS built in
* Cars store paired devices data
  * Don't pair your device with a rental car
  * Remove all your data when you sell your car 
* Car manufacturers collects all kinds of data including your driving ability
* Car electronics and software can be hacked remotely or at least nearby
* Cars communicate using V2X and V2V technology and by nature has to be unencrypted, so it can be intercepted
* Self-driving cars track more data 

## Ch 12 - The Internet of Surveillance

* Smart home systems can be hacked 
* Don't use analog baby monitor
* Smart home systems security is as weak as its network or hub
* Smart TV, speaker, smartphone (or the software therein, like the browser) etc listen, record your conversation, and send it to the cloud, even when it is not actively on
* Don't pair your smart device with your online logins 
* Put tape over your device's camera
* Put dummy mic in the microphone socket of your device
  * Using an old broken set of headphones, cut the wire near the microphone jack. Make sure the two wires don't touch
* Attacker can trigger false alarms (which you might have to pay) on your home monitoring system
* See shodan.io for a list of insecure IoT in all over the world
* Turn off (physically disconnect) your Internet-accessible webcams when they are not in use
  * Use proper authentication and strong password when they are in use

## Ch 13 - Things Your Boss Doesn't Want You To Know

* Every action you do on your company's devices are being tracked
* No law in the US that prohibit companies from tracking their employees
* Anything passing through a corporate network is tracked 
* Lock your computer when you are not in front of the screen
* Don't do anything personal at work or using work device for personal matter
* Don't use the company WiFi for anything personal
* Don't use company's printer or public printer to print personal confidential information
  * Printers are usually behind in their security best practices, therefore the weakest link in corporate networks
  * Printers keep temporary data in their hard drive
  * The hard drive is often not encrypted
* Phone gyroscope can be programmed to be sensitive enough to pick up slight air vibrations, including those produced by human speech
* Turn on your 2FA before an attacker turn it on for the first time for you
* Encrypt every file you send over the internet, regardless of providers
* Cloud data doesn't have the same Fourth Amendment protections as physical data

## Ch 14 - Obtaining Anonimity Is Hard Work

* Cards with NFC can be cloned for spoofing
* When you travel to a hostile country
  * Clean up any sensitive data and perform a full backup
  * Leave the data there but encrypt it with a strong key
  * Do not keep the entire of the passphrase with you
  * Upload the encrypted data to a cloud service, download and uploas as needed
  * Create a hidden encrypted file folder on your hard drive
  * Whenever entering a password, cover yourself and your computer
  * Seal your devices in an envelop and sign it, put it in the hotel room safe, put camera inside the safe and send it to cellular phone in real time
  * Carry your devices with you at all times
* Your devices can be searched without a warrant within one hundred air miles of the US border
* Whenever you travel internationally, CBP and ICE uses ATS to create a profile about you
* Wiping data is not the same as deleting data
* SSD wiping is very difficult, use regular HDD to ease wiping by using file shredding software
* Don't pair your device with someone else
* US enforcement cannot demand your password, but can force your fingerprints to unlock the device
* Repressive government might attempt to install tracking software on your device
* Use an unlocked burner phone and purchase a SIM card in the country you are visiting
* Use an USB bootable OS such as Tails
* When using cloud provided encryptions, don't use the same cloud provider to store the key
* Your hotel room can be searched
* Hotel room safes are not really that safe
* Don't use hotel WiFi, if you must, use VPN
* To use Internet privately while travelling
  * Purchase prepaid giftcards anonymously
  * Use open Wi-Fi after changing your MAC address
  * Always use Tor whenever accessing anything
  * Find an email provider that allows you to sign up without SMS validation
  * Using your anonymous email address, sign up to a site to get a Bitcoin wallet, buy a supply of Bitcoin, pay them using the prepaid gift cards
  * Setup a secondary anonymous email address and new secondary Bitcoin wallet, use a different TOR network while doing so
  * Use Bitcoin laundering service (be careful because there are many scams), have the laundered Bitcoin sent to second Bitcoin address
  * Sign up for a VPN service using laundered Bitcoin that doesn't log traffic or IP connections (check the privacy policy)
  * Have a stranger obtain a burner portable WiFi device on your behalf, give him/her cash to purchase it
  * To access the Internet, use the burner WiFi device away from home, work and your other cellular devices
  * Once powered up, connect to VPN through the burner hotspot device
  * Use Tor to browse the Internet

## Ch 15 - The FBI Always Gets Its Man

* Never link anonymous online persona with your real-world persona

## Ch 16 - Mastering the Art of Invisibility

* Use a stand alone laptop only for anonymous online activities
* Get a second device only for online banking
  * If invisibility is not the goal, but security, you can use non laptop devices such as iPad or iPhone and Apple account
  * Else, use Linux based laptop
* Purchase these devices with cash
* Install Tails and Tor
* Don't login to any sites or apps under your real identity
* Turn off your wireless router before you boot your anonymous laptop at home
* Use your own wireless router instead of the standard provided by service provider
* Never use your anonymous laptop at home or work ever and never use it for non anonymous activities
* Hire a random stranger to anonymously purchase gift cards ($100 each) by cash, don't purchase any refillable cards
* Hire a random stranger to purchase a burner phone by cash
* Use a free open WiFi and sit in a spot where potentially have no cameras around (i.e., in an adjacent site)
* Each time your connect to a free WiFi, reset your MAC address
* Hire a random stranger to purchase a personal WiFi that's only strictly for anonymous online activities
* Don't use personal anonymous WiFi in thes same spot for too long
* Sign up to a couple of anynymous email accounts using Tor
* Use free email address and use the burner phone for phone verification
* Signup for Bitcoin wallets
* Use prepaid giftcards to buy initial Bitcoin
* Launder the Bitcoin (see Ch 14)
* Dispose the gift cards using shredder and throw it in random dumpster away from home or office
* Sign up for a VPN service (always check their privacy policy and make sure they do not retain logs)
* All it takes to screw this setup
  * Forget to never ever turn the anonymous device/WiFi/phone at home/work
  * Forget to never turn on your personal device/WiFi/phone where you use your anonymous device/WiFi/phone
* The way you type is unique and can be associated to you
  * The website you visit can record your keystrokes style, for example, financial institutions
  * Use browser plugin to introduce randomness in your normal keystroke cadence
