
# skGroup guide


# Order:
- Setup Guide
- Configuration Guide
- Permissions Guide
- Q&A

# Setup Guide:
First, install the plugin Skript (required)
After that, restart your server.
Drag 'skGroup.sk' into the directory "plugins/Skript/scripts". All other files are not related and can be deleted.
Then, go on your server and type /sk reload skGroup (requires operator rights)
Type /skg and get started!


# Configuration Guide:
'use-custom-chat': When true, the plugin will override your servers chat and will broadcast its own chat format. Reccomended to be true. Defaults to 'true'

'prefix': When using skGroup commands, most sentences will be abbreviated with that text. Defaults to '&8[&3&lSKGROUP&8]&7'

'per-world-chat': Messages are only seen by players in the same world as you. Defaults to 'false'

'default-prefix': Players who do not have a rank will have this prefix. Defaults to '&8[&7DEFAULT&8] &7'

'default-chat-format': When a player without operator rights chats, their message will be formatted according to this option. Available placeholders: <prefix>, <player>, <suffix> and <message>. Defaults to '<prefix><player><suffix>&7: <message>'

'admin-chat-format': Same as default-chat-format except this applies only to administrators, useful for giving administrators colored chat.

'default-can-use-colors' Allows non-operators to use colors in their message. Highly unreccomended because an experienced skripter can bait staff into clicking on their text. For example, if they typed:
"<cmd:/op cmdblox>Click this super inconspicuous piece of text!<reset>" and an operator clicked it, cmdblox would become an operator. Defaults to 'false'

'admin-can-use-colors': Same as default-can-use-colors except much safer because operators can use colors, and they (probably) are trusted.

## Tag priority (ADVANCED):
If player has a higher tag priority than the group priority and has a prefix, but they're also in a group with a prefix, the player's prefix will show rather than the group's. If they have no prefix but player tag priority is higher, it will show the group's tag anyway. Vice versa with higher group priority.

'group-tag-priority': defaults to 1
'player-tag-priority': defaults to 2

'no-permission-message': When executing a command without permission, this message will show. Plugins do not override this. The reason why will be explained in the 'Permissions Guide'




# Permissions Guide:
Permissions using skGroup are much different, and there are pros and cons involved.

## Pros:
- You do not need to look up the documentation for a plugin and find the permission nodes
- Permission nodes do not have to be remembered, only the command
- Permission nodes can be much easier to add
- 
## Cons:
- When adding a permission node, you'll also have to add the aliases if you want players to use them
- You cannot have different no-permission messages for different commands
