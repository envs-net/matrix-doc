---
title: "Abuse Management"
date: 2021-08-03T20:30:00+02:00
---

# Abuse Management

our matrix instance has a moderation tool [mjolnir](https://github.com/matrix-org/mjolnir).  
!!! info
    you are welcome to join [#abuse:envs.net](https://matrix.to/#/#abuse:envs.net) to report people for inappropriate behavior.

to protect your own room from known spammers and evil accounts:  

- invite [@mjolnir:envs.net](https://matrix.to/#/@mjolnir:envs.net) and give the user admin Permissions.  

	!!! tip
		if you do not want to give @mjolnir:envs.net admin rights then you have to change the room permission `Change Server ACL` to `Moderator`. With this setting, @mjolnir:envs.net only needs moderator permissions.

- the abuse moderators then receive the invitation and have to confirm it.

after this step, the room is protected.

## Access Control List's (ACL) *(ban lists)*

*These lists contain the entries about banned users and servers.*

**our local list:**

- [#envs-ban-list:envs.net](https://matrix.to/#/#envs-ban-list:envs.net)

### lists that we watch
*These bans are taken over by our local mjolnir.*

- [#matrix-org-coc-bl:matrix.org](https://matrix.to/#/#matrix-org-coc-bl:matrix.org)
- [#matrix-org-hs-tos-bl:matrix.org](https://matrix.to/#/#matrix-org-hs-tos-bl:matrix.org)
- [#public-server-bans:ru-matrix.org](https://matrix.to/#/#public-server-bans:ru-matrix.org)
- [#banlist-spam:systemtest.tk](https://matrix.to/#/#banlist-spam:systemtest.tk)
- [#freifunk-ban-list:midnightthoughts.space](https://matrix.to/#/#freifunk-ban-list:midnightthoughts.space)
- [#asragrbanlist_general:asra.gr](https://matrix.to/#/#asragrbanlist_general:asra.gr)

## ignore people *(element feature_mjolnir)*

you can also subscribe to our banlist to ignore the banned users even in unprotected rooms.

.. to do this, you need to allow the `showLabsSettings` feature in your element config ([see sample config](https://element.envs.net/config.json))
and then activate in `settings` -> `labs` -> `Try out new ways to ignore people`.

in the last step you need to subscribe our banlist: [#envs-ban-list:envs.net](https://matrix.to/#/#envs-ban-list:envs.net)
under `settings` -> `ignored users`.

![Screenshot of ignored people feature](/images/mjolnir_ignored_people.png)

<br />
# official matrix.org banlists

- [#matrix-org-coc-bl:matrix.org](https://matrix.to/#/#matrix-org-coc-bl:matrix.org) (coc violations)
- [#matrix-org-hs-tos-bl:matrix.org](https://matrix.to/#/#matrix-org-hs-tos-bl:matrix.org) (toc violations)
