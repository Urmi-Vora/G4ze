

<h4 align="center"> 
  <a href="https://odysee.com/@spyboy:b/R4ven">
    ▶️ Watch Video - How To Use!
  </a>
</h4>




The tool hosts a fake website which uses an iframe to display a legit website and, if the target allows it, it will fetch the Gps location `(latitude and longitude)` of the target, capture multiple pictures of the target along with `IP Address` and `Device Information`.

<h4 align="center"> This tool is a Proof of Concept and is for Educational Purposes Only. </h4> 

Using this tool, you can find out what information a malicious website can gather about you and your devices and why you shouldn't click on random links or grant permissions like Location to them.

### Key Features:

- IP address and GPS location tracking
- Collection of device system information
- Capturing images from the device's camera
- Integration with Discord for data presentation
- User interaction for location permission
- Display of a website through an embedded iframe
- Regular interval-based data collection
- Access to and upload webcam images
- Formatting and presentation of data in Discord messages
- Links to Google Maps and Google Earth based on location
- Error handling for denied location permission
- User feedback and error messages

---
### On the link click

```diff
+ It will automatically fetch the IP address and device information
! If location permission is allowed, it will fetch the exact location of the target.
! If camera permission is allowed, it will capture non-stop from the front camera.
```

### Limitation

```diff
- It will not work on laptops or phones that have no GPS or no Camera, 
# browsers that block javascript,
# or if the target is mocking the GPS location.
# or if a target is using VPN or spoofing IP

- Some browsers auto block location and camera permission like(Brave, Safari etc)
+ Location accuracy will be more accurate if you use this on a smartphone.

```

### IP location VS. GPS location

```diff
- Geographic location based on IP address is NOT accurate,
# Does not provide the location of the target. 
# Instead, it provides the approximate location of the ISP (Internet service provider)
```
```diff
+ GPS fetch almost exact location because it uses longitude and latitude coordinates.
@@ Once location permission is granted @@
# Accurate location information is received to within 20 to 30 meters of the user's location.
# (it's almost the exact location)
```
---

<h4 align="center">
  OS compatibility :
  <br><br>
  <img src="https://img.shields.io/badge/Windows-05122A?style=for-the-badge&logo=windows">
  <img src="https://img.shields.io/badge/Linux-05122A?style=for-the-badge&logo=linux">
  <img src="https://img.shields.io/badge/Android-05122A?style=for-the-badge&logo=android">
  <img src="https://img.shields.io/badge/macOS-05122A?style=for-the-badge&logo=macos">
</h4>

<h4 align="center"> 
Requirements:
<br><br>
<img src="https://img.shields.io/badge/Python-05122A?style=for-the-badge&logo=python">
<img src="https://img.shields.io/badge/Git-05122A?style=for-the-badge&logo=git">
<img src="https://img.shields.io/badge/Discord webhook-05122A?style=for-the-badge&logo=discord">
</h4>

### ⭔ Installation
---

```
git clone https://github.com/spyboy-productions/r4ven.git
```
```
cd r4ven
```
```
pip3 install -r requirements.txt
```
```
python3 r4ven.py
```

`NOTE:` If you're not going to use `localhost`
- choose module(all, cam, ip, gps), open file `index.html` replace `"http://127.0.0.1:8000/image"` with the `URL` you wish to use.

OR

Please use the `-t` flag to choose a different URL.

Use the following command to make r4ven executable:

```
chmod +x r4ven.py
```
- To change the Image URL use 
```
python3 r4ven.py [-t target]
```
- To change Port
```
python3 r4ven.py [-p port]
```
- For Both Image-URL and port
```
python3 r4ven.py [-t target] [-p port]
```

**Example:** `python3 r4ven.py -t https://example.com/r4ven/images -p 8000`

---

```Enter your discord webhook URL (set up a channel in your discord server with webhook integration)```

https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks

`if not have discord account and sever make one, it's free.`

https://discord.com/

---

📍 _Track info data will be sent to your discord webhook channel._

- why discord webhook? Conveniently, you will receive a notification when someone clicks on the link.

---

#### ⭓ To change website template

- choose module(all, cam, ip, gps), open file `index.html` replace the `src` in the iframe. (Note: not every website supports iframe)

---

#### ⭓ port forwarding:

- It automatically port forwards with Serveo, but you can choose to use your preferred method for port forwarding.
- The default port is 8000 or any port you specified.

⭓ Other cmd to port-forward...

TryCloudflare: `cloudflared tunnel --url http://localhost:8000`

Tunnelmole: `tmole 8000`

Ngrok: `ngrok http 8000`

Ssh: `ssh -R 80:localhost:8000 ssh.localhost.run`

Serveo: `ssh -R 80:localhost:8000 serveo.net`

```diff
- Make sure you port forward else it will not work on the smartphone's browser
```


#### 😴🥱😪💤 ToDo:

- Mask port forwarded URL using our tool Facad1ng
- PHP code to host a website without Python
- Iframe can be warned ..make a phishing template or bypass the iframe warning.

---

---




