=====
Staff Guide
=====

Effective Moderation
------------

.. important::
    :ref:`This page has been recently updated to reflect slash command usage. Please ensure you view which commands are slash-supported and which ones are not (/ vs !).`

- **Developer IDs**

On Discord, every username can have 9999 variants of it before it becomes unavailable. 
Trying to ban someone by just putting "Eternalll" is extremely dangerous. 
This is why we use `Developer IDs`_ instead, they provide a number such as 349909910995206145 (my ID) that ensures you are punishing the correct person.
Please enable this feature immediately.

.. _`Developer IDs`: https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID


- **Moderation Bot**

Edward Richtofen#5103 is the main moderation bot for all things. Main moderation commands use **/** while all of the rest use the **!** prefix.

Issuing Punishments
------------

.. warning::
    :ref:`Be aware that all bot-issued punishments are direct-messaged to the user. Refrain from using vague or immature reasons.`

.. tip::
    :ref:`Slash commands are more intelligent than regular text-based commands and will ensure requirements are met.`

+-----------+----------------------------------------+
| Command   | Description                            |
+===========+========================================+
| !rule     | Verbal warning not sent to modlog.     |
+-----------+----------------------------------------+
| /warn     | A warning sent to the user.            |
+-----------+----------------------------------------+
| /mute     | A temporary mute of the user.          |
+-----------+----------------------------------------+
| /kick     | Kick the user from the server.         |
+-----------+----------------------------------------+
| /softban  | Same as kick but purges messages.      |
+-----------+----------------------------------------+
| /ban      | Permanently ban the user.              |
+-----------+----------------------------------------+

Verbal Warning
------------

.. code-block:: none

    !rule<#> (id)

Verbal warning, unrelated to the modlog system. You may optionally use an ID or mention in order to direct the warning to the user.

    .. image::  /media/punishments/rule.png

.. important::
    :ref:`At this time, slash commands for the rule command are not supported. Please continue to use the ! prefix until this is implemented.`

.. important::
    :ref:`Do not actually use the <brackets> and (parenthesis), they denote required and optional input.`

Warning
------------

.. code-block:: none

    /warn <user> <reason>

Warn the user, logging to the modlog and DMing the user. Warns cannot be appealed and are a recommended first action after or with a verbal warning.

    .. image::  /media/punishments/warn.png

.. important::
    :ref:`Remember, the user is DMed. Please provide an appropriate and at least a semi-descriptive reason so that the member can remediate their behavior.`

Mute
------------

.. code-block:: none

    /mute <user> <time> <reason>

Mutes a user, preventing them from talking (and viewing certain channels). You must disconnect the user if they are in voice.

    .. image::  /media/punishments/mute.png

Users who evade mutes by leaving become permanently muted when rejoining. They must reach out to Modmail to get this fixed as it is their fault.

When selecting a time, there are several pre-defined options that you may choose. It is at moderator discretion to choose a time appropriate for the punishment. 

.. tip::
    :ref:`A time period of a day is usually suggested as a generic minimum period as punished users will be less likely to retaliate after 24 hours have passed.`

Kick
------------

.. code-block:: none

    /kick <user> <reason>

Kicks remove the member from the server without deleting messages.

    .. image::  /media/punishments/kick.png

Reserve this punishment for new-ish members who need a reality check to come back when they are ready to read the rules and play nice.

Most unused, but can make a statement if necessary.

.. warning::
    :ref:`Will remove all activity ranks (not reset rank itself). Therefore, the member returning must level up once to regain all their roles back.`

Softban
------------

.. code-block:: none

    /softban <user> <reason>

Softban removes a member from the server, deleting 1 day of messages.

    .. image::  /media/punishments/softban.png

Reserve this punishment for those who you wish to kick, at the same time wanting to delete their messages alongside it.

Calls the user purge portion of the API by immediately banning and unbanning the user.

.. warning::
    :ref:`Will remove all activity ranks (not reset rank itself). Therefore, the member returning must level up once to regain all their roles back.`

Ban
------------

.. code-block:: none
    
    /ban <user> <reason>

Bans and DMs the user a link where they may appeal (first offense only) and purges 1 day of messages.

    .. image::  /media/punishments/ban.png

.. important::
    :ref:`Members may appeal their punishment via ban appeal website, but only ones made in error are ever accepted.`

Substitutions
------------

Substitutions are a way of increasing your efficiency in issuing punishments by pre-filling text with the rule documentation and text itself. 
When using brackets around a \"**rule#**\", it will replace the text with the rule that it corresponds to.

.. code-block:: none

    /warn <user> [rule5]

translates to the following full command:

.. code-block:: none

    /warn <user> Rule 5 Violation | Discussing or Committing Piracy

This is a time-saver as long as the reason for punishment is indeed that rule and made obvious to the user by a bit of extra text added to the end.

Modlog Management
------------

- **Invoking the Modlog**

To search a user's modlog, you will run **!warnings <id>**. This will invoke an embed, beginning with an overview of their punishment history.

.. important::
    :ref:`Do not actually use the <brackets> and (parenthesis), they denote required and optional input.`

To interact with the modlog, you will need to use the arrow reactions to populate a single infraction. 

.. warning::
    :ref:`Do not interact with the modlog overview. Use the reactions to scroll to a specific reaction.`

- **◀️, ▶️ and ❌**

The left and right reactions scroll through the modlog. Pressing ❌ will close the embed.

- **✏️ and 🗑️**

After scrolling to an individual punishment, ✏️ will allow you to edit the reason. Useful if you made a typo or were not specific enough in your punishment reason. 
🗑️ allows you to clear the modlog entry.

.. important::
    :ref:`Edits made to the modlog do not update for the punished user in their direct messages.`

.. warning::
    :ref:`Cleared mutes will automatically unmute the user. Please keep this in mind when modifying the modlog.`

Warden System
------------

- **Confidentiality**

The Call of Duty Zombies Warden System is a confidential multi-tool system that performs intelligent auto-moderations based on bot-observed behaviors and other triggers.

.. warning::
    :ref:`Disclosures of bypasses or detailed functions of the Warden system is an immediate dismissal from Staff and potential ban depending on severity. 
    We take the security and protection of our members very seriously.`

- **Assistance**

Warden effectively assists moderators by means of acting like 10 tireless Staff members that sometimes need intervention.

The intervention channel is where the bot asks for behavioral checks and notifies about things it sees, but has low confidence to take action on.

The executions channel is where the bot had high confidence in its logic and took action on a (most likely) blatant rule break.

.. note::
    :ref:`Warden is not a replacement for human moderation. The bot is not omniscient and cannot possibly cover all chats and their situations like a human can.`