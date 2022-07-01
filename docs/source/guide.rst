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

+-----------+----------------------------------------+
| Command   | Description                            |
+===========+========================================+
| !rule     | Verbal warning not sent to modlog.     |
+-----------+----------------------------------------+
| !warn     | A warning sent to the user.            |
+-----------+----------------------------------------+
| !mute     | A temporary mute of the user.          |
+-----------+----------------------------------------+
| !kick     | Kick the user from the server.         |
+-----------+----------------------------------------+
| !softban  | Same as kick but purges messages.      |
+-----------+----------------------------------------+
| !ban      | Permanently ban the user.              |
+-----------+----------------------------------------+

- **Optional vs Required**

When navigating this section, be aware that items in <brackets> are required and that items in (parenthesis) are optional.

.. note::
    :ref:`You do not actually use brackets and parenthesis at all when issuing moderations, they are for reference.`

- **Verbal Warning**

.. code-block:: none

    !rule<#> (mention)

Verbal warning, unrelated to the modlog system. You may optionally use a mention (not ID) in order to direct the warning to the user.

- **Warning**

.. code-block:: none

    !warn <user> (reason)``::``

Warn the user, logging to the modlog and DMing the user. Warns cannot be appealed and are a recommended first action after or with a verbal warning.

- **Mute**

.. code-block:: none

        !mute <user> <time> (reason)

Times are in a shortened format, minute **m**, hour **h**, day **d**, week **w**.

Mutes a user, preventing them from talking (and viewing certain channels). You must disconnect the user if they are in voice.

Users who evade mutes by leaving become permanently muted when rejoining. They must reach out to Modmail to get this fixed as it is their fault.

.. warning::
    :ref:`Please ensure you specify a time and do not perma-mute users.`

- **Kick**

.. code-block:: none

    !kick <user> (reason)

Kicks remove the member from the server without deleting messages.

- **Softban**

.. code-block:: none

    !softban <user> (reason)

Kicks remove the member from the server without deleting messages.

- **Ban**

.. code-block:: none
    
    !ban <user> (reason)

Bans and DMs the user a link where they may appeal (first offense only) and purges 1 day of messages.

- **Examples**

+-----------+----------------------------------------+
| Punishment| Issued Command                         |
+===========+========================================+
| Verbal    | !rule4 @mention                        |
+-----------+----------------------------------------+
| Warn      | !warn <id> Spamming the server         |
+-----------+----------------------------------------+
| Mute      | !mute <id> Continually being off topic |
+-----------+----------------------------------------+
| Kick      | !kick <id> Read the rules please.      |
+-----------+----------------------------------------+
| Softban   | !softban <id> Multi channel spam       |
+-----------+----------------------------------------+
| Ban       | !ban <id> [rule5]                      |
+-----------+----------------------------------------+

- **Substitutions**

Wait a second, why did we use \"[rule5]\" in our ban reason in the example above? Simply put, Substitutions are a way of increasing your efficiency in issuing punishments. 
When using brackets around a \"rule#\", it will replace the text with the rule that it corresponds to.

.. code-block:: none

    !warn <id> [rule5]

translates to the following in the modlog:

.. code-block:: none

    Rule 5 Violation | Discussing or Committing Piracy

This is a time-saver you should get used to as long as the reason for punishment is indeed that rule and made obvious to the user.


Managing the Modlog
------------

- **Invoking the Modlog**

To search a user's modlog, you will run **!search <id>**. This will invoke an embed, beginning with an overview of their punishment history.

To interact with the modlog, you will need to use the arrow reactions to populate a single infraction. 

.. warning::
    :ref:`Do not interact with the modlog overview. Use the reactions to scroll to a specific reaction.`

- **◀️, ▶️ and ❌**

The left and right reactions scroll through the modlog. Pressing ❌ will close the embed.

- **✏️ and 🗑️**

.. warning::
    :ref:`Do not use these on the modlog overview. Use the reactions to scroll to a specific reaction.`

After scrolling to an individual punishment, ✏️ will allow you to edit the reason. Useful if you made a typo or were not specific enough in your punishment reason. 
🗑️ allows you to clear the modlog entry.

.. important::
    :ref:`Edits made to the modlog do not update for the punished user.`

.. important::
    :ref:`Cleared mutes will automatically unmute the user.`

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

