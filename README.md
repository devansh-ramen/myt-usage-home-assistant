# my.t Usage (Home Assistant)

Custom Home Assistant component to get remaining monthly data from the my.t (Mauritius Telecom) portal.

## Setup
Copy the entire "myt_usage" folder to your custom_components folder. If you have never installed any custom Home Assistant component, create a folder named "custom_components" in your Home Assistant configuration folder.

Add the following to your configuration.yaml:
```yaml
sensor:
  - platform: myt_usage
    username: !secret myt_username
    password: !secret myt_password
    scan_interval: 7200
```

`username` and `password`: Use the same credentials that you use to log in to [internetaccount.myt.mu](https://internetaccount.myt.mu). If you don't know your username or password, please contact the Mauritius Telecom Hotline.

`scan_interval`: This value is in seconds and will determine how often the script will check the my.t portal for the remaining data. I don't know if Mauritius Telecom has any limit to the number of times you can log in to the portal but I've found that a value of 7200 (2 hours) is good enough for me. I would not recommend setting it below 1800 (30 minutes) as I don't believe the portal is updated *that* often.

## Credits

This project uses MechanicalSoup to scrap
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5NjA1NDE3MzIsLTE1NzA2Njk4MDksLT
c4NTU0NjY1MSw2NDE4MDEzNjVdfQ==
-->