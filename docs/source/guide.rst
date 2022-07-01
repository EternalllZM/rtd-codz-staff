=====
Staff Guide
=====

Effective Moderation
------------

.. warning::
    :ref:`All information here is considered semi-confidential. There is no reason for a non-Staff member to read this information.`

- **Developer IDs**

On Discord, every username can have 9999 variants of it before it becomes unavailable. 
Trying to ban someone by just putting "Eternalll" is extremely dangerous. 
This is why we use `Developer IDs`_ instead, they provide a number such as 349909910995206145 (my ID) that ensures you are punishing the correct person.
Please enable this feature immediately.

.. _`Developer IDs`: https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID



- **Moderation Bot**

Edward Richtofen#5103 is the main moderation bot for all things. 
The prefix is **!** for all their commands. With great power comes great responsibility.

Issuing Punishments
------------

.. warning::
    :ref:`Be aware that all bot-issued punishments are direct-messaged to the user. Refrain from using vague or immature reasons.`

- **Optional vs Required**

When navigating this section, be aware that items in <brackets> are required and that items in (parenthesis) are optional.

.. note::
    :ref:`You do not actually use brackets and parenthesis at all when issuing moderations, they are for reference.`

- **Verbal Rule Warnings**

    !rule<#> (mention)
    ``::``

Verbal warning, unrelated to the modlog system. You may optionally use a mention (not ID) in order to direct the warning to the user.

- **Warning**

    !warn <user> (reason)
    ``::``

Warn the user, logging to the modlog and DMing the user. Warns cannot be appealed and are a recommended first action after or with a verbal warning.

- **Muting**

> !mute <user> <time> (reason)

Times are in a shortened format, minute **m**, hour **h**, day **d**, week **w**.

Mutes a user, preventing them from talking (and viewing certain channels). You must disconnect the user if they are in voice.

Users who evade mutes by leaving become permanently muted when rejoining. They must reach out to Modmail to get this fixed as it is their fault.

.. warning::
    :ref:`Please ensure you specify a time and do not perma-mute users.`
