---
title: "Bot's Overview"
date: 2021-08-03T20:30:00+02:00
---

# local Bot's on envs.net

> all our bots are from Maunium's [maubot](https://github.com/maubot/maubot).

feel free to use our bot's in your room!

## Overview

[Anti-Thread Bot](#anti-thread_bot) |
[Audio Preventer](#audio_preventer) |
[Cat Disruptor](#cat_disruptor) |
[CommitStrip](#commitstrip) |
[Dice Bot](#dice_bot) |
[echobot [envs]](#echobot_envs) |
[Factorial Bot](#factorial_bot) |
[fetch Image Bot](#fetch_image_bot) |
[Github Bot](#github_bot) |
[Karma Bot](#karma_bot) |
[media Bot](#media_bot) |
[ntfy Bot](#ntfy_bot) |
[Poll Bot](#poll_bot) |
[Reminder](#reminder) |
[RSS Bot](#rss_bot) |
[sed Bot](#sed_bot) |
[social Preview Bot](#social_preview_bot) |
[Timer](#timer) |
[Translator](#translator) |
[urbandictionary Bot](#urbandictionary_bot) |
[urldownload Bot](#urldownload_bot) |
[version checker](#version_checker) |
[Weather Bot](#weather_bot) |
[Wolfram Alpha Bot](#wolfram_alpha_bot) |
[XKCD](#xkcd)

!!! info
	there is also [@maubot:envs.net](https://matrix.to/#/@maubot:envs.net) which includes all bots except for [Cat Disruptor](#cat_disruptor) and [Anti-Thread Bot](#anti-thread_bot).  
	you can try all the bots in [`#test:envs.net`](https://matrix.to/#/#test:envs.net).

***

## Anti-Thread Bot

**name:** [`@antithread:envs.net`](https://matrix.to/#/@antithread:envs.net)  
**src:** [https://github.com/maubot/antithread](https://github.com/maubot/antithread)

A simple maubot that redacts all thread messages.

Simply invite it to your room, give it moderator permission (or whatever is necessary to redact messages), and it will delete new thread messages as they're sent.

## Audio Preventer

**name:** [`@audio_preventer:envs.net`](https://matrix.to/#/@audio_preventer:envs.net)  
**src:** [https://github.com/MTRNord/maubot-audio-preventer](https://github.com/MTRNord/maubot-audio-preventer)

A Bot to prevent voice or audio messages to be sent into a room.

***Note: Bot account requires redact, kick and ban permissions.***

The Audio Preventer is instructed to auto redact those, warn you 3 times as text, then kick you 5 times and then ban you. The counter are per user and across all rooms the bot is in. If you reach the ban level it will ban you on a new voice or audio message also in the other rooms the Audio Preventer is active in.

## Cat Disruptor

A Bot plugin that disrupts monologues cat pictures and react to some messages.

**name:** [`@cat:envs.net`](https://matrix.to/#/@cat:envs.net)  
**src:** [https://github.com/maubot/disruptor](https://github.com/maubot/disruptor)

You can use it 3 times per day with `🐈️` _(\:cat2:)_.

## CommitStrip

A Bot to fetch [CommitStrips](https://www.commitstrip.com/en/) and to get notifications about new comics.

**name:** [`@commitstrip:envs.net`](https://matrix.to/#/@commitstrip:envs.net)  
**src:** [https://github.com/maubot/commitstrip](https://github.com/maubot/commitstrip)

**Usage:** `!commitstrip` _OR_ `!commitstrip <subcommand> [...]`

**Subcommands:** `search`, `subscribe`, `unsubscribe`

## Dice Bot

A Bot that rolls dice. Has built-in calculator.

**name:** [`@dice:envs.net`](https://matrix.to/#/@dice:envs.net)  
**src:** [https://github.com/maubot/dice](https://github.com/maubot/dice)

**Usage:**

The base command is `!roll`. To roll dice, pass `XdY` as an argument, where `X`
is the number of dice (optional) and `Y` is the number of sides in each dice.
Most Python math and bitwise operators and basic `math` module functions are
also supported, which means you can roll different kinds of dice and combine
the results however you like.

## echobot [envs]

A simple Bot that echoes pings and other stuff.

**name:** [`@echo:envs.net`](https://matrix.to/#/@echo:envs.net)  
**src:** [https://github.com/maubot/echo](https://github.com/maubot/echo)

**Usage:**

- `!ping` - Reply with "Pong!" and the time it took for the message to reach the bot.
- `!echo <message>` - Reply with the given message

## Factorial Bot

A Bot that calculates expected and unexpected factorials in messages.

**name:** [`@factorial:envs.net`](https://matrix.to/#/@factorial:envs.net)  
**src:** [https://github.com/maubot/factorial](https://github.com/maubot/factorial)

**Usage:**

Simply type a number followed by one or more exclamation marks. Note that multiple exclamation marks means a double factorial, not a factorial applied twice.

Example:

`1! 2! 3!`

> 1! = 1  
> 2! = 2  
> 3! = 6

`over 9000!`

>9000! ≈ 8.09958 × 10<sup>31681</sup>

## fetch Image Bot

A Bot to fetch an image from an URL.

**name:** [`@fetchimage:envs.net`](https://matrix.to/#/@fetchimage:envs.net)  
**src:** [https://github.com/shukon/maubot-fetchimage](https://github.com/shukon/maubot-fetchimage)

**Usage:** `!fetch-image https://example.org/some_image.jpg`

## Github Bot

A GitHub client and webhook receiver for maubot.

**name:** [`@github:envs.net`](https://matrix.to/#/@github:envs.net)  
**src:** [https://github.com/maubot/github](https://github.com/maubot/github)

**Usage:** `!github  <subcommand> [...]`

- `login [flags]` - Log into GitHub.
- `ping` - Check your login status.
- `raw <query>` - Make a raw GraphQL query.
- `create [owner/repo] <title and body>` - Create an issue. Title on first line, body on other lines
- `webhook  <subcommand> [...]` - Manage webhooks.

<br />
1. **Use `!github login` to log in.**

   After inviting your bot / client to a matrix channel, use the `!gh` or
   `!github` command to use the github instance.

   Using `!gh login` first is mandatory and needed once **per instance**.

   The bot will reply with a link leading to your personal Github's allowed
   OAuth apps page, where you shall grant the necessary rights to the bot
   OAuth app.

   By default, the bot will request access to all public repos and to add
   webhooks. You can control the permissions it wants with some flags:

   - `--no-repo` makes it not ask for repo access at all.
     Only `!github webhook add` will work, other commands like `!github create`
     will not.
   - `--no-hook` makes it not ask for webhook access.
     `!github webhook add` will not work.
   - `--private` makes it ask for private repo access. Necessary if you want to
     use the bot to manage private repos.

<br />
2. **Use `!github webhook add <owner>/<repo>` to add webhooks.**

   This will let you see in the current channel all the commits, comments,
   issues, stars, forks, pull requests, and so on, for that given repository.

   You must have admin rights on the repositories you want to track, as adding
   webhooks to a repository requires manager access rights to a project.

   Once you create a webhook and track a repository, it will be tracked
   **only in the room from which you are in**.

## Karma Bot

A Bot that tracks the karma of users.

**name:** [`@karma:envs.net`](https://matrix.to/#/@karma:envs.net)  
**src:** [https://github.com/maubot/karma](https://github.com/maubot/karma)

**Usage:** `!karma  <subcommand> [...]`

- `up <Event ID>` - Upvote an event
- `down <Event ID>` - Downvote a message
- `stats` - View global karma statistics
- `view [user ID]` - View your or another users karma
- `export` - Export the data of your karma
- `breakdown` - View your karma breakdown
- `top` - View the highest rated users
- `bottom` - View the lowest rated users
- `best` - View the highest rated messages
- `worst` - View the lowest rated messages

## Media Bot

A simple Bot that posts MXC URIs of uploaded images.

**name:** [`@media:envs.net`](https://matrix.to/#/@media:envs.net)  
**src:** [https://github.com/maubot/media](https://github.com/maubot/media)

## ntfy Bot

This is a bot to subscribe to ntfy topics and send messages to a matrix room.

**name:** [`@ntfy:envs.net`](https://matrix.to/#/@ntfy:envs.net)  
**src:** [https://gitlab.com/999eagle/maubot-ntfy](https://gitlab.com/999eagle/maubot-ntfy)

**Usage:**

Use `!ntfy subscribe server/topic` (for example `!ntfy subscribe ntfy.envs.net/my_topic`) to subscribe the current room to the ntfy topic. Future messages will be sent to the room.

To unsubscribe, use `!ntfy unsubscribe server/topic`.

## Poll Bot

A Bot that creates a poll in a room and allows users to vote.

**name:** [`@poll:envs.net`](https://matrix.to/#/@poll:envs.net)  
**src:** [https://github.com/TomCasavant/PollMaubot](https://github.com/TomCasavant/PollMaubot)

**Usage:** `!poll <subcommand> [...]`

- `new <poll_setup>` - Creates a new poll with "Question" "choice" "choice" "choice" ...
- `results` - Prints out the current results of the poll
- `close` - Ends the poll

Example:

`!poll new  "Question" "Choice1" "Choice2" "Choice3"` - Creates a new poll with given (at least 1) choices

The user can now also create polls with line-breaks:
```
!poll new What is my question?
Choice1
Choice2
Choice3
```

`!poll results` - Displays the results from the poll

`!poll close` - Ends the poll

Users vote by adding the matching emoji to the poll (i.e. if the first choice has a :thumbsup: then in order to pick that choice the user has to react with :thumbsup:)

## Reminder

A Bot to remind you about things.

**name:** [`@reminder:envs.net`](https://matrix.to/#/@reminder:envs.net)  
**src:** [https://github.com/maubot/reminder](https://github.com/maubot/reminder)

**Usage:** `!remind <date> [message]` _OR_ `!remind <subcommand> [...]`

**Subcommands:** reschedule, help, list, locales, locale, timezone

`<date>` can be a time delta (e.g. `2 days 1.5 hours` or `friday at 15:00`) or an absolute date (e.g. `2020-03-27 15:00`).

To set the timezone for date parsing and output for your messages, use `!remind tz <timezone>`.
It's recommended to use a [TZ database name](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones),
but anything supported by Pytz will work.

Similarly, you can set the locale for date parsing with `!remind locale <list of locales>`. If you
provide multiple locales, each one will be tried for parsing your input until one matches. Unlike
the timezone, the locale only affects input, not output. You can view available locales using
`!remind locales`. You can also contribute new locales by making a pull request
(see [locales.py](https://github.com/maubot/reminder/blob/master/reminder/locales.py), content warning: long regexes).

To list your upcoming reminders, use `!remind list`

## RSS Bot

**name:** [`@rss:envs.net`](https://matrix.to/#/@rss:envs.net)  
**src:** [https://github.com/maubot/rss](https://github.com/maubot/rss)

A Bot that posts RSS feed updates to Matrix.

**Usage:** `!rss  <subcommand> [...]`

- `subscribe <feed URL>` - Subscribe this room to a feed.
- `unsubscribe <feed ID>` - Unsubscribe this room from a feed.
- `template <feed ID> <new template>` - Change the notification template for a subscription in this room
- `notice <feed ID> [true/false]` - Set whether or not the bot should send updates as m.notice
- `subscriptions` - List the subscriptions in the current room.

## sed Bot

A Bot to do sed-like replacements.

**name:** [`@sed:envs.net`](https://matrix.to/#/@sed:envs.net)  
**src:** [https://github.com/maubot/sed](https://github.com/maubot/sed)

Example:

> this is a wrong txt.

**Usage:** `s/txt/text/g`

**sed output:**
> this is a wrong text.

## social Preview Bot

A simple Bot that responds to a Reddit/Instagram/YouTube link with the video title and thumbnail.

**name:** [`@youtube:envs.net`](https://matrix.to/#/@youtube:envs.net)  
**src:** [https://github.com/ggogel/SocialMediaDownloadMaubot](https://github.com/ggogel/SocialMediaDownloadMaubot)

the 'social Preview Bot' contains also a plugin to find and convert Spotify links shared in rooms automatically to your preferred streaming service.

**src:** [https://github.com/HarHarLinks/maubot-idonthavespotify](https://github.com/HarHarLinks/maubot-idonthavespotify)

## Timer

A Bot that can be used as a timer.

**name:** [`@timer:envs.net`](https://matrix.to/#/@timer:envs.net)  
**src:** [https://github.com/pedantic-git/maubot-timer](https://github.com/pedantic-git/maubot-timer)

**Usage:**

```!timer 60```

This will start a timer for 60 seconds. The name will be chosen for you:

> ⏳ Timer alfa started for 60 seconds

... 60 seconds later ...

> ⏰ Timer alfa: time's up!

```!timer 30 foo```

This will name the timer:

> ⏳ Timer foo started for 30 seconds

## Translator

A Bot to translate words using Google Translate. (DeepL is planned too)

**name:** [`@translate:envs.net`](https://matrix.to/#/@translate:envs.net)  
**src:** [https://github.com/maubot/translate](https://github.com/maubot/translate)

**Usage:** `!translate <language> [text]`

After inviting the bot to your room, simply use the `!translate` command:

`!translate en ru Hello world.`
    
which results in

>Translator:  
> > rubo77  
> > !translate en ru Hello world.

> Привет, мир.

You can also use the alias `tr`:

`!tr en ru Hello world.`

The first parameter (source language) can be set to `auto` or omitted entirely
to let Google Translate detect the source language. Additionally, you can reply
to a message with `!tr <from> <to>` (no text) to translate the message you
replied to.

**supported languages:**

- de: (german)
- en: (english)
- zh: (chinese)
- ...

Full list of supported languages: [https://cloud.google.com/translate/docs/languages](https://cloud.google.com/translate/docs/languages)

## urbandictionary Bot

A Bot to fetch definitions from [Urban Dictionary](https://www.urbandictionary.com/). Returns a specified or random entry.

**name:** [`@urban:envs.net`](https://matrix.to/#/@urban:envs.net)  
**src:** [https://github.com/dvdgsng/UrbanMaubot](https://github.com/dvdgsng/UrbanMaubot)

**Usage:** `!ud [term] [index]`

Examples
```
!ud
!ud foo
!ud foo 2
```

## urldownload Bot

Implementing URL downloads in matrix rooms.

**name:** [`@urldownload:envs.net`](https://matrix.to/#/@urldownload:envs.net)  
**src:** [https://codeberg.org/LukeLR/matrix-url-download](https://codeberg.org/LukeLR/matrix-url-download)

**Usage:** `!urldownload <subcommand> [...]`

- `enable` - Enable downloading of URLs in this chat
- `disable` - Disable downloading of URLs in this chat
- `status` - Get status of URLDownloader in this chat
- `debug [State of debug mode]` - Manage or get debug status in this room

## version checker

A Bot to check the version of servers in rooms.

**name:** [`@version:envs.net`](https://matrix.to/#/@version:envs.net)  
**src:** [https://mau.dev/maubot/rsvc](https://mau.dev/maubot/rsvc)

**Usage:**

- `!servers` - Test all servers in room and report aggregated tests.
- `!servers retest <name>` - Re-test a server and update the previous results.
- `!servers match <software> [operator] <version>` - Show all servers with the
  given software and version. Operator can be `>`, `<`, `>=`, `<=`, `!=`, `=`
  or empty.
- `!server test <name>` - Test one server, independently of any previous whole-room tests.
- `!server`, `!version` and `!versions` are aliases for `!servers`, `recheck`
  is an alias for `retest`.

## Weather Bot

A Bot that gets the weather from [wttr.in](http://wttr.in) and returns the text to the chat.

**name:** [`@weather:envs.net`](https://matrix.to/#/@weather:envs.net)  
**src:** [https://github.com/kellya/maubot-weather](https://github.com/kellya/maubot-weather)

**Usage:**

- `!weather` - Reply with the weather based on the default config value (Germany, Berlin)
- `!weather <location>` - Reply with the location for the specified `<location>` where
`<location>` can be an airport code, or a city
- `!moon` - Display lunar phase information

## Wolfram Alpha Bot

a Bot to search on [Wolfram Alpha](https://www.wolframalpha.com/).

**name:** [`@wolframalpha:envs.net`](https://matrix.to/#/@wolframalpha:envs.net)  
**src:** [https://github.com/ggogel/WolframAlphaMaubot](https://github.com/ggogel/WolframAlphaMaubot)

**Usage:** `!wolfram some search term`

## XKCD

A Bot to fetch xkcd comics and to get notifications about new comics.

**name:** [`@xkcd:envs.net`](https://matrix.to/#/@xkcd:envs.net)  
**src:** [https://github.com/maubot/xkcd](https://github.com/maubot/xkcd)

**Usage:** `!xkcd [number]` _OR_ `!xkcd <subcommand> [...]`

**Subcommands:** `reindex`, `lucky`, `search`, `subscribe`, `unsubscribe`
