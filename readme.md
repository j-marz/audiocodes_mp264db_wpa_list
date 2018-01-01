# AudioCodes MP264DB WPA Wordlist

The AudioCodes MP264DB router uses it's serial number (printed on the base of the unit) as the default WPA passphrase. Based on [images](./images/mp264db_dodo.png) found online, the serial number appears to be 2 upper case letters (VT) followed by 7 numbers.

From brief research, the router appears to be used by DODO, iPrimus and Commander ISPs in Australia.

The default SSIDs for these routers are a combination of the ISP name + the last 4 characters of the routers MAC address. DODO ISP example SSID: `DODO4455` - where `4455` is taken from `00:11:22:33:44:55`

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
These lists are intended for educational and/or lawful use only. You should only use these lists against your own equipment and/or during authorised penetration test of 3rd party equipment.

https://github.com/j-marz/audiocodes_mp264db_wpa_list/raw/master/images/mp264db_dodo.png