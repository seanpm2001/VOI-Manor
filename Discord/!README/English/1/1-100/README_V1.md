
***

# VOI Manor

## Discord support

Discord does not have a proper way of exporting user data, and I have invested a lot of time into server setup. I wanted to make the process easier, and allow for a controlled backup format.

Thus the Disdat file format was born.

The Disdat file format is a non-encrypted ("plain text") data file format that contains the magic number `#$JSON_DISDAT//$` to define its type. The MIME type associated with this is `data/disdat-data-file` | it is not a registered format yet.

The syntax of this format is inspired by various languages, most prominently including JSON, Shell, Java, Python, and JavaScript.

Here is the very first sample data file of this format:

**DISCORD_SAMPLE.disdat**

```Java
#$JSON_DISDAT//$
##START##{
// This is a sample Discord server backup of a new Discord server for testing the DIScord DATa file format (*.disdat)
{{:LIBRARIES:}}
library.onload(discord(main)); // Main Discord library
library.onload(discord(cat)); // Category library
library.onload(discord(pref)); // Preferences library
library.onload(discord(rooms)); // Room library
library.onload(discord(roles)); // Roles library
{{:CATEGORIES:}}
**{Main}** {
{{:ROOMS:}}
*{General}* {
  this.channel(type == "text/media"); // Defines that this is a text channel with media uploads
  this.channel(type == "lobby"); // Special case for indicating that this is the starter room
  this.channel(roles.all == "true"); // Specifies that there are no roles and no rules
  **Role: admin** {
    this.role.admin(permissions = " ",  " ", " "); // Specifies the permissions for this user role
  }
  **Role: user** {
    this.role.user(permissions = " ",  " ",  " "); // Specifies the permissions for this user role
  }
}}
// This is pseudocode and serves as an example of the plans for this data file format.
// Time stamp: 2021 Friday, August 27th at 7:40 pm
// Line count: 31
// File type: Discord Data backup file (*.disdat)
// Syntax type: Custom (object oriented, syntax inspired by JSON, Shell, Java, Python, and JavaScript.
\\$DISDAT_END[]}
break;

```

No further information is available at this time.

***

## File info

**File type:** `Markdown document (*.md *.mkd *.markdown)`

**File version:** `1 (Friday, August 27th 2021 at 7:38 pm)`

**Line count (including blank lines and compiler line):** `67`

***
