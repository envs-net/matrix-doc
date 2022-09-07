---
title: "Message retention policies"
date: 2021-08-03T20:30:00+02:00
---

# Message retention policies

Message retention policies exist at a room level, follow the semantics described in [MSC1763](https://github.com/matrix-org/matrix-doc/blob/matthew/msc1763/proposals/1763-configurable-retention-periods.md), and allow server and room admins to configure how long messages should be kept in a homeserver's database before being purged from it.

!!! note
	Please note that, as this feature isn't part of the Matrix specification yet, this implementation is to be considered as experimental.

A message retention policy is mainly defined by its `max_lifetime` parameter, which defines how long a message can be kept around after it was sent to the room. If a room doesn't have a message retention policy, and there's no default one for a given server, then no message sent in that room is ever purged on that server.

MSC1763 also specifies semantics for a `min_lifetime` parameter which defines the amount of time after which an event can get purged (after it was sent to the room), but Synapse doesn't currently support it beyond registering it.

Both `max_lifetime` and `min_lifetime` are optional parameters.

!!! note
	Note that message retention policies don't apply to state events.

more information about Message retention policies can find [here](https://github.com/matrix-org/synapse/blob/master/docs/message_retention_policies.md).

## Lifetime limits on envs.net

Our current instance lifetime limits are:

```yaml
  allowed_lifetime_min: 30m
  allowed_lifetime_max: 10y
```

## Room configuration

To configure a room's message retention policy, a room's admin or
moderator needs to send a state event in that room with the type
`m.room.retention` and the following content:

* Type `/devtools`.
* Select "Explore room state" -> "Send custom state event"
* Set event type to `m.room.retention` ("State Key" can be left blank)

```json
{
    "max_lifetime": ...
}
```

Press `Send`

In this event's content, the `max_lifetime` parameter has the same
meaning as previously described, and needs to be expressed in
milliseconds. The event's content can also include a `min_lifetime`
parameter, which has the same meaning and limited support as previously
described.

!!! note
	Note that over every server in the room, only the ones with support for
	message retention policies will actually remove expired events. This
	support is currently not enabled by default in Synapse.
