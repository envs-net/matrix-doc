---
title: "First steps"
date: 2021-08-03T20:30:00+02:00
---

# First steps - How to use Matrix?

## Matrix-Login

!!! note
    We recommend using the Element desktop client, because this avoids most problems users have with Matrix, e.g. end to end encryption.

Downloads for: [:fontawesome-solid-download: Windows](https://packages.riot.im/desktop/install/win32/x64/Element%20Setup.exe){ .md-button } [:fontawesome-solid-download: macOS](https://packages.riot.im/desktop/install/macos/Element.dmg){ .md-button } [:fontawesome-solid-download: Linux](/clients/install_linux){ .md-button }

After a desktop installation, make sure to use the existing account. Here the example of Element:

![Selected login button in the element matrix client](/images/01_Login_en.png)

This is done by clicking on **Change**. Then you will not accidentally end up on the wrong server...

![Change login page with focus on the homeserver button](/images/02_Change-Homeserver_en.png)

Now you can manually specify the home server: `matrix.envs.net`

![Input field to change the home server with the input matrix.envs.net](/images/03_Set-Homeserver_en.png)

Afterwards the login with username and password must be carried out:

The drop-down menu "Log in with:" should be left at "Username". Then the following entries must be made:

**Username**

**Password**

An alternative login, e.g. using the e-mail address, is **NOT** possible during the first, initial login, only after the second login.

After the first login there is also no e-mail / confirmation mail.

Analogous to e-mail addresses, this results in matrix addresses with the following structure:

`@username:envs.net`

![Login window with request to enter Username and Password](/images/04_Username_en.png)

## Convenient use of end-to-end encryption (E2EE)

Matrix not only encrypts transports to and from the home server of envs.net but also allows the use of end-to-end encryption (E2EE). For this, cryptographic keys have to be exchanged between all devices that want to write end-to-end encrypted. This technical necessity sounds and is complicated, but in the meantime it has become very convenient for the users. The many cryptographic keys created by the client are stored on the respective device. If this is a tab in a browser, for example, there is a risk that this tab will be closed unintentionally. Then all encrypted contents are no longer readable. To prevent this from happening, a key protection is offered on the home server of the envs.net, on which (protected with a security phrase (or security key that can be calculated from it) all cryptographic keys are stored encrypted.

!!! danger
    It is highly recommended to use this key backup (with a secure security phrase which is **NOT** your login password)!
   
![Prompt to generate the security key or enter a security phrase](/images/11_Setup-Key_en.png)
![Prompt to enter a password for the key backup](/images/12_Enter-Key_en.png)
Alternatively, instead of the security phrase, you can also have a security key generated that serves the same purpose as the security phrase. Furthermore, the security key is generated in addition to the security phrase and should be kept safe and retrievable as an emergency key (e.g. save it as .txt file AND print it out) 
![Display of the security key to write or save away](/images/13_Present-Key_en.png) 

[Other important settings](/settings/) may improve your Matrix experience!


## Requests to setup the key backup

![Screenshot of the prompt to enter a security phrase](/images/01_Restore-Session_en.png)

If you skipped the request to setup the key backup, the next screen would look like this:

![Confirmation of skipping the input of a security phrase](/images/03_Cancel-Restore_en.png)

Key protection is highly recommended for worry-free end-to-end encryption. For this reason, a smaller tooltip will prompt you to set up the encryption even after you skip further:
   
![Chat view showing a tooltip to set up encryption. Marking the confirm field](/images/04_Notification_en.png)

If you omit this here as well, you will get a last warning if you log off consciously. If no key backup is set up at the latest, encrypted calls that may have already taken place cannot be accessed later. If the tab is closed, this also corresponds to a logout.
   
![Query if messages should be encrypted](/images/05_Logout-Notify_en.png)

Avoid this situation by setting up a key backup!

## Privacy policy

Privacy policy: [Link](https://envs.net/privacy-policy/)

## Impressum

Impressum: [Link](impressum.md)
