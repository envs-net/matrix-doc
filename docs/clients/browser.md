---
title: "Element Web (Browser)"
date: 2021-08-03T20:30:00+02:00
---

# Using the Element webclient

Start here: [https://element.envs.net](https://element.envs.net)

![Start page of Element Webclient with login button](/images/01_Welcome_en.png "Start page of Element Webclient with login button")

Registration is necessary, the service can be used by clicking on "Create Account" on the homepage [https://element.envs.net](https://element.envs.net).

After the Registration you need to confirm your account. Check your mail Inbox.

Now you can Login to your webclient.

![Login window with request to enter Username and Password](/images/02_Login1_en.png "Login window with request to enter Username and Password")

The drop-down menu "Log in with:" should be left at "Username". Then the following entries must be made:

**Username**

Enter here your username from envs.net starting with a `@` sign followed by your username and the text `:envs.net`. For the user `isabell` it should like `@isabell:envs.net`.

**Password**

Analogous to e-mail addresses, this results in matrix addresses with the following structure:

`@username:envs.net`

!!! note
	If you want to start immediately with a [Matrix Client](/clients/) instead of the above mentioned website (Element Web-App hosted on envs.net), it is important to change the homeserver from the usually default `matrix.org` to `matrix.envs.net` (shown in the following three screenshots)

![Change login page with focus on the homeserver Button](/images/02_Login2_en.png "Change login page with focus on the homeserver Button")

1. click on change
![Input field to change the homeserver with the input matrix.envs.net](/images/02_Login3_en.png "Input field to change the homeserver with the input matrix.envs.net")
2. mark the preset homeserver address and remove it
3. entry of the matrix homeserver address of envs.net

## Browser settings

### Browser selection

Recommended are the browsers [Firefox](https://www.mozilla.org/de/firefox/new/), [Chromium](https://www.chromium.org/getting-involved/download-chromium), newer versions of MS Edge (based on Chromium). Older or unsuitable browsers may only show a white page.

### NoScript

Many people use script blockers to protect themselves from [Tracking](https://tu-dresden.de/tu-dresden/newsportal/news/datenschutz-beim-website-tracking) and malware in the browser, for example with the addon [NoScript](https://addons.mozilla.org/de/firefox/addon/noscript/). Here you have to make the following settings (for the integration manager, e.g. Jitsi/Etherpad)

![Browser plugin settings NoScript with envs.net selected as trusted script sources](/images/10_Sicherheit2_en.png "Browser plugin settings NoScript with envs.net selected as trusted script sources")

### Cookies

Do you also allow cookies from

- envs.net
