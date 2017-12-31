# AudioCodes MP264DB WPA Wordlist

The AudioCodes MP264DB Router uses the routers serial number (printer on the base of the unit) as the default WPA passphrase. Based on images found online, the serial number appears to be 2 upper case letters (VT) followed by 7 numbers.

The router appears to be used by DODO, iPrimus and Commander ISPs in Australia.

Default SSIDs for these routers (DODO example): `DODOxxxx` - where `xxxx` is the last 4 characters of the MAC address of the router 

I've created 2 wordlists that can be used to find the WPA(2) passphrase from a MP264DB WPA handshake if the default passphrase is still in use.

## Wordlists
Wordlists have been compressed to reduce their size. You can exctract them using the following command:
`tar zxf mp264db_VTxxxxxxx.lst.tgz`

mp264db_VTxxxxxxx.lst - VT letters in upper case followed by any 7 numbers - based on images found online showing serial and WPA key on labels

XXxxxxxxx - Any 2 upper case letters followed by any 7 numbers - in case VT are not the only letters used in the serial number

## Hashcat mask
The following mask can be used in Hashcat instead of using a wordlist
`hashcat ... -1 V -2 T ?1?2?d?d?d?d?d?d?d`
`hashcat ... ?u?u?d?d?d?d?d?d?d`

Where `...` are the other options for your cracking session

## Disclaimer
Intended for educational or lawful use only against your own equipment or during authorised penetration tests.