# Termux Workaround & Fixes
How to fix several services problem on Termux
## Navigation
- **[First Important Steps](#fix-first)**
- **[How to fix Storage problem](#storage)**
- **[How to fix Microphone probem](#microphone)**
- **[How to fix Camera problem](#camera)**
- **[How to fix Location problem](#location)**
- **[How to fix other Access problem](#other)**
- **[Other problems](#

<br>

## First Steps <a name=fix-first></a>
1. Install **[Termux API from GitHub](https://github.com/termux/termux-api/releases)** 
2. Open Termux, run the following commands:
```
pkg update
pkg upgrade -y
pkg install -y termux-api
```

---
<br>

## How to fix Storage problem <a name=storage></a>
If you getting trouble to get Android Storage access in Termux and Termux Desktop, then run the following command and Grant the permission:
```
termux-setup-storage
```
> After this a directory `storage` will apper in your home directory 

---
<br>

## How to fix Microphone probem <a name=microphone></a>
If you getting trouble to get Microphone access in Termux and Termux Desktop, then:
1. run the following command and Grant the permission:
```
termux-microphone-record -d 4
```
2. Start the PulseAudio, which automatically starts when you start the desktop by using `termux-xfce4`
3. Start the SLES module, which automatically starts when you start the desktop by using `termux-xfce4`

> After that you can use Microphone on Termux and Termux Desktop, meaning you can do VC on Discord without any problem

---
<br>

## How to fix Camera problem <a name=camera></a>
If you getting trouble to get Camera access in Termux and Termux Desktop, then run the following command and Grant the permission:
```
termux-camera-photo -c 0 photo.jpg
```
> [!NOTE]
> After granting the permission, it may take a photo using camera.

---
<br>

## How to fix Location problem <a name=location></a>
If you getting trouble to get Microphone access in Termux and Termux Desktop, then run the following command and Grant the permission:
```
termux-location
```
> [!NOTE]
> Granting Location permission can surely increase battery consumption than usual
---
<br>

## How to fix other Access problem <a name=other></a>
If you are getting any other service problem then visit Termux & Termux APi wiki & GitHub for checking its command

---

### If you have any other problem, contact me on my Discord server by [Clicking here](https://discord.gg/xCMJwG5gGK) <a name=bhai-prob></a>
