# mac_hideuseraccount
Deactivate and Hide User accounts on Mac OS 
# General
- always reboot after changes
- keep a backup account and remember your ***user*** name

### View all Users
```
ls /users
```

### Show User config File
```
chsh <username>
```

## Hide <-> Show
This will switch between showing the Account Image and the Option "Other user" where you need to type username and Password

### Hide User-Account from Login-Screen
```
sudo dscl . create /Users/<username> IsHidden 1
```

### Show User-Account from Login-Screen
```
sudo dscl . create /Users/<username> IsHidden 0
```




## Disable <-> Enable
This will completly hide the account from the Login Screen. You need to have a second account to reactivate the disabled account

### Disable User-Account
```
sudo chsh -s /usr/bin/false <username>
```


### Enable User-Account
```
sudo chsh -s /bin/bash <username>
```
