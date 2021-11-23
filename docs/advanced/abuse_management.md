---
title: "Abuse Management"
date: 2021-08-03T20:30:00+02:00
---

# Abuse Management

our matrix instance has a moderation tool [mjolnir](https://github.com/matrix-org/mjolnir).  
you are welcome to join [#abuse:envs.net](https://matrix.to/#/#abuse:envs.net) to report known spammers and evil peoples.  

to protect your own room from known spammers and evil accounts, you can simply give [@mjolnir:envs.net](https://matrix.to/#/@mjolnir:envs.net)  
an **invite and admin Permissions to your room**.  
(if you do not want to give @mjolnir:envs.net admin rights then you have to change the room permission `Change Server ACL` to `Moderator`. With this setting, @mjolnir:envs.net only needs moderator rights.)  

the abuse moderators then receive the invitation and have to confirm it.  
after this step, the room is protected.

***notice:***

you can also subscribe to our banlist to ignore the banned users even in unprotected rooms.

.. to do this, you need to allow the `showLabsSettings` feature in your element config ([see sample config](https://element.envs.net/config.json))
and then activate in `settings` -> `labs` -> `Try out new ways to ignore people`.

in the last step you need to subscribe our banlist: [#envs-ban-list:envs.net](https://matrix.to/#/#envs-ban-list:envs.net) (`!UyrSHIwWgbGsHjabGe:envs.net`)
under `settings` -> `ignored users`.

***official matrix.org banlists:***

- [#matrix-org-coc-bl:matrix.org](https://matrix.to/#/#matrix-org-coc-bl:matrix.org) (coc violations)
- [#matrix-org-hs-tos-bl:matrix.org](https://matrix.to/#/#matrix-org-hs-tos-bl:matrix.org) (toc violations)
