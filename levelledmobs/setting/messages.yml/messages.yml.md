---
sidebar_position: 2
---

# 🌟 messages.yml

:::tip

这里是语言文件,对语言文件的汉化很快就会进行!

:::


<details>

<summary>Click to view a comprehensive list of all options within Messages.YML</summary>

```yaml
#
#   ---------------  -  ------------------------------
#        Section 01  |  Common Messages
#   ---------------  -  ------------------------------
#
common:
  prefix: '&b&lLevelledMobs:&7'
  no-permission:
    - '%prefix% You don''t have access to that.'
  players-only:
    - '%prefix% Only players have access to that.'
  player-offline:
    - '%prefix% Player ''&r%player%&7'' is offline.'
  invalid-command:
    - '%prefix% Invalid command.'


#
#   ---------------  -  ------------------------------
#        Section 02  |  Default Command Messages
#   ---------------  -  ------------------------------
#
command:
  levelledmobs:
    main-usage:
      - '%prefix% Available commands:'
      - '&8 &m->&b /%label% debug &8- &7various commands relating to debugging'
      - '&8 &m->&b /%label% egg &8- &7create spawner eggs'
      - '&8 &m->&b /%label% help &8- &7show URL to the wiki'
      - '&8 &m->&b /%label% info &8- &7view info about the plugin'
      - '&8 &m->&b /%label% kill &8- &7mass kill levelled mobs'
      - '&8 &m->&b /%label% reload &8- &7reload the configuration files'
      - '&8 &m->&b /%label% rules &8- &7printout of the rules system'
      - '&8 &m->&b /%label% summon &8- &7summon specific levelled mobs'


    #
    #   ---------------  -  ------------------------------
    #        Section 03  |  Summon Command Messages
    #   ---------------  -  ------------------------------
    #
    summon:
      invalid-amount:
        - '%prefix% Invalid amount ''&b%amount%&7''.'
      invalid-entity-type:
        - '%prefix% Invalid entity type ''&b%entityType%&7''.'
      invalid-level:
        - '%prefix% Invalid level ''&b%level%&7''.'
      invalid-summon-type:
        - '%prefix% Invalid summon type ''&b%summonType%&7''.'
      invalid-summon-type-console:
        - '%prefix% Only players may use summon type ''&bhere''&7, you must use ''&batPlayer&7'' or ''&batLocation&7'' instead.'
      invalid-location:
        - '%prefix% Invalid location.'
      here:
        usage:
          - '%prefix% Usage: &b/%label% summon <amount> <entity> <level> here'
        success:
          - '%prefix% Spawned &b%amount%&7 of &fLvl.%level% &b%entity%(s)&7 at your location.'
      atLocation:
        usage:
          - '%prefix% Usage: &b/%label% summon <amount> <entity> <level> atLocation <x> <y> <z> [world]'
        success:
          - '%prefix% Spawned &b%amount%&7 of &fLvl.%level% &b%entity%(s)&7 at &8(&b%x%&7, &b%y%&7, &b%z%&7 in world ''&b%world%&7''&8)&7.'
        usage-console:
          - '%prefix% Usage (console): &b/%label% summon <amount> <entity> <level> atLocation <x> <y> <z> <world>'
        invalid-world:
          - '%prefix% Invalid world ''&b%world%&7''.'
        invalid-location:
          - '%prefix% Invalid location.'
      atPlayer:
        usage:
          - '%prefix% Usage: &b/%label% summon <amount> <entityType> <level> atPlayer <player>'
        success:
          - '%prefix% Spawned &b%amount%&7 of &fLvl.%level% &b%entity%(s)&7 at &r%targetDisplayname%&7''s location.'
      usage:
        - '%prefix% Summon command syntax:'
        - '&8 &m->&b /%label% summon <amount> <entity> <level> here'
        - '&8 &m->&b /%label% summon <amount> <entity> <level> atPlayer <player>'
        - '&8 &m->&b /%label% summon <amount> <entity> <level> atLocation <x> <y> <z> [world]'
      amount-limited:
        min:
          - '%prefix% Summon amount limited to a minimum of &b1&7 mob.'
        max:
          - '%prefix% Summon amount limited to a maximum of &b%maxAmount%&7 mobs.'
      level-limited:
        min:
          - '%prefix% Level limited to a minimum of &bLvl.%minLevel%&7.'
        max:
          - '%prefix% Level limited to a maximum of &bLvl.%maxLevel%&7.'
      not-levellable:
        - '%prefix% &b%entity%&7 is not levellable.'


    #
    #   ---------------  -  ------------------------------
    #        Section 04  |  Kill Command Messages
    #   ---------------  -  ------------------------------
    #
    kill:
      usage:
        - '%prefix% Usage: &b/%label% kill <all/near>'
      all:
        invalid-world:
          - '%prefix% Invalid world ''&b%world%&7''.'
        success:
          - '%prefix% Killed &b%killed%&7 levelled mobs in &b%worlds%&7 world(s) &8(&b%skipped%&7 mobs were skipped&8)&7.'
        usage:
          - '%prefix% Usage: &b/%label% kill all [world/*]'
        usage-console:
          - '%prefix% Usage (console): /%label% kill all <world/*>'
      near:
        invalid-radius:
          - '%prefix% Invalid radius ''&b%radius%&7''.'
        invalid-radius-min:
          - '%prefix% Specified radius has been adjusted to the minimum radius &8(&b%minRadius%&8)&7.'
        invalid-radius-max:
          - '%prefix% Specified radius has been adjusted to the maximum radius &8(&b%maxRadius%&8)&7.'
        success:
          - '%prefix% Killed &b%killed%&7 levelled mobs within a radius of &b%radius%&7 block(s) &8(&b%skipped%&7 mobs were skipped&8)&7.'
        usage:
          - '%prefix% Usage: &b/%label% kill near <radius>'


    #
    #   ---------------  -  ------------------------------
    #        Section 05  |  Spawner Command Messages
    #   ---------------  -  ------------------------------
    #
    spawner:
      usage:
        - '%prefix% Spawner command syntax:'
        - '&8 &m->&b /%label% spawner create'
        - '&8 &m->&b /%label% spawner copy'
        - '&8 &m->&b /%label% spawner info'
        - ' '
        - '&fSample syntax:'
        - '&8 &m->&b /%label% spawner create &3/minlevel&b 1 &3/maxlevel&b 10 &3/name&b "My customized LM spawner" &3/customDropId&b Id1'
      no-value:
        - '%prefix% No value was specified for key ''&b%keyname%&7''.'
      no-player:
        - '%prefix% Command can only be run by a player unless the &b/giveplayer&7 parameter is specified.'
      invalid-value:
        - '%prefix% Invalid value for &b%keyname%&7, must be a number.'
      no-level-specified:
        - '%prefix% You must specify minLevel and/or maxLevel.'
      inventory-full:
        - '%prefix% Your inventory is full.'
      spawner-give-message:
        - '%prefix% Gave you a LM spawner.'
      spawner-give-message-console:
        - '%prefix% Gave &r%playername%&7 a LM spawner. &8|&7 minLevel: &b%minlevel%&7, maxLevel: &b%maxlevel%&7'
      permission-denied:
        - '%prefix% You don''t have permission to update or convert a LM spawner.'
      spawner-converted:
        - '%prefix% Converted vanilla spawner into a LM spawner with name "%spawnername%".'
      spawner-updated:
        - '%prefix% Updated LM spawner from spawn egg. Spawner name: "%spawnername%"'
      info:
        status-enabled:
          - '%prefix% Spawner info is &aenabled&f.'
        status-not-enabled:
          - '%prefix% Spawner info is &cnot enabled&f.'
        enabled:
          - '%prefix% Spawner info is &aenabled&f. Right-Click any Spawner for details!'
        disabled:
          - '%prefix% Spawner info has been &cdisabled&f.'
      copy:
        vanilla-spawner:
          - '%prefix% Spawner copy only works with LM spawners.'
        status-enabled:
          - '%prefix% Spawner copy is &aenabled&f.'
        status-not-enabled:
          - '%prefix% Spawner copy is &cnot enabled&f.'
        enabled:
          - '%prefix% Spawner copy is &aenabled&f. Right-Click a LM Spawner to make a copy.'
          - 'Your hand must be empty.'
        disabled:
          - '%prefix% Spawner copy has been &cdisabled&f.'


    #
    #   ---------------  -  ------------------------------
    #        Section 06  |  Spawn Egg Command Messages
    #   ---------------  -  ------------------------------
    #
    spawn_egg:
      usage:
        - '%prefix% egg command syntax:'
        - '&8 &m->&b /%label% egg /minlevel <level> /maxlevel <level> /entity <entity type>'
        - '&7&o Sample Spawn Egg'
        - '&7/%label% egg &b/minlevel&7 1 &b/maxlevel&7 10 &b/name&7 "My customized LM spawn egg" &b/customDropId&7 Id1'
      no-paper:
        - '%prefix% This feature is only available on servers running Paper or forks of Paper'
      no-value:
        - '%prefix% No value was specified for: &b%keyname%&7'
      no-player:
        - '%prefix% Command can only be run by a player unless /giveplayer is specified'
      no-player-specified:
        - '%prefix% No player was specified'
      invalid-value:
        - '%prefix% Invalid value for &b%keyname%&7, must be a number'
      no-level-specified:
        - '%prefix% You must specify minLevel, maxLevel and entity'
      inventory-full:
        - '%prefix% &4Your inventory is full!'
      give-message:
        - '%prefix% Gave you a LM spawn egg'
      give-message-console:
        - '%prefix% Gave &r%playername%&7 a LM spawn egg. &8|&7 minLevel: &b%minlevel%&7, maxLevel: &b%maxlevel%&7, entity: &b%entitytype%&7'


    #
    #   ---------------  -  ------------------------------
    #        Section 07  |  Rules Command Messages
    #   ---------------  -  ------------------------------
    #
    rules:
      incomplete-command:
        - '%prefix% Incomplete command'
      console-rules:
        - '%prefix% Rules have been printed on the console'
      discord-invite:
        - '%prefix% Click for Discord invite'
      wiki-link:
        - '%prefix% Click to open the wiki'
      rules-reprocessed:
        - '%prefix% Rules Reprocessed for &b%entitycount%&7 mobs in &b%worldcount%&7 world(s)'
      reset:
        - '%prefix% Running this command will reset your rules to one of 4 defaults.'
        - 'You must select if you want vanilla/basic/average/advanced/extreme difficulty.'
        - 'A backup will be made and your rules.yml reset to default.'
      resetting:
        - '%prefix% Resetting rules to %difficulty%'
      reset-syntax:
        - '%prefix% To reset your rules to %difficulty% difficulty, type in the following command:'
        - '%label% rules reset %difficulty% confirm'
      reset-complete:
        - '%prefix% rules.yml updated successfully'
      invalid-difficulty:
        - '%prefix% Invalid difficulty: %difficulty%'
      rule-name-missing:
        - '%prefix% Must specify a rule name.'
      rule-name-invalid:
        - '%prefix% No rule was found with name %rulename%'
      showing-rules:
        - 'Showing all values for rule: &b%rulename%&r'
      no-entities-visible:
        - '%prefix% Must be looking at a nearby entity'
      no-entities-near:
        - '%prefix% No entities were found within a 10 block radius'
      effective-rules:
        - '%prefix% Showing effective rules for: %entitytype% (lvl %level% %mobname%) in %world%, %location%'
      no-effective-rules:
        - '%prefix% No effective rules were found'

    #
    #   ---------------  -  ------------------------------
    #        Section 08  |  System Command Messages
    #   ---------------  -  ------------------------------
    #
    reload:
      started:
        - '%prefix% Reloading configuration files...'
      finished:
        - '%prefix% Reload complete.'
      usage:
        - '%prefix% Usage: &b/%label% reload'
    info:
      about:
        - ' '
        - '&b&lLevelledMobs&b v%version%'
        - '&7&o%description%'
        - ' '
        - '&7Maintainers: &f%maintainers%'
        - '&7Contributors: &f%contributors%'
        - '&7Support for: &fMC &f%supportedVersions%'
        - ' '
      listSeparator: '&7, &f'
      usage:
        - '%prefix% Usage: &b/%label% info'
    compatibility:
      notice:
        - '%prefix% Compatibility checks have been printed to your logs. Please check the console :)'
      usage:
        - '%prefix% Usage: &b/%label% compatibility'


#
#   ---------------  -  ------------------------------
#        Section 09  |  Other Messages
#   ---------------  -  ------------------------------
#
other:
  compatibility-notice:
    enabled: true
    messages:
      - '%prefix% LevelledMobs compatibility notice:'
      - '&8 &m->&r &b%incompatibilities% &7possible incompatibilities were found. Please run ''&b/levelledmobs compatibility&7'' to check them.'
      - '&8 &m->&7 This message is sent as you have the permission &blevelledmobs.compatibility-notice&7. You can disable this message in &bmessages.yml&7.'
      - '&8 &m->&7 Please ensure you have followed all instructions on the plugin''s Wiki page.'
  update-notice:
    messages:
      - '&b&nLevelledMobs Update Checker Notice:'
      - '&7Your &bLevelledMobs&7 version is &boutdated&7! Please update to &bv%latestVersion%&7 as soon as possible. &8(&7You''re running &bv%currentVersion%&8)'
    send-in-console: true
    send-on-join: true

  mob-head-drop-name: '%mob_name%''s head'
  no-drop-in-chunk: '%prefix% &7Your levelled mob kill count has reached the maximum for this area. You will no longer receive levelled drops from these mobs. Please come back after a while.'
  create-debug:
    - '&b&nCreate a Debugging ZIP'
    - '&7You should only run this command if a LevelledMobs developer has asked you to. It is used to assist users who are experiencing issues with the plugin.'
    - ''
    - '&7This command will generate a ZIP file containing the following required data:'
    - '&8 &m->&b Plugins list'
    - '&8 &m->&b Server version'
    - '&8 &m->&b Current and maximum online player count'
    - '&8 &m->&b The latest.log file&7 &8(/logs/latest.log)'
    - ''
    - '&7LevelledMobs developers will not redistribute or retain the data beyond the purpose of resolving any issue you may be experiencing. You may also verify the contents prior to sending the file.'
    - '&7To proceed in creating the ZIP file, please run:'
    - '&b/lm debug create-zip confirm&7'
```

</details>

LevelledMobs' `messages.yml` file allows you to customise all of the chat messages that are sent from the plugin. You can visit the Official Translations to fine easy to swap translations of this file in Español (Spanish), Deutsch (German), and Français (French) \[COMING SOON]!

#### Warnings:

> **Most placeholders only work in certain messages.**\
> Usually, if a placeholder is not included in a message by default, it will not be processed in it.\
> \
> For this reason, you may find it useful to reference the default messages.yml file if you are unsure which placeholders are supported in one or more messages in the file.\
> \
> For example, you will not be able to use the `%supportedVersions%` placeholder in the 'no permission' message.

<details>

<summary>Click to view a list of all options within Section 1 - Common Messages</summary>

```yaml
common:
  prefix: '&b&lLevelledMobs:&7'
  no-permission:
    - '%prefix% You don''t have access to that.'
  players-only:
    - '%prefix% Only players have access to that.'
  player-offline:
    - '%prefix% Player ''&r%player%&7'' is offline.'
  invalid-command:
    - '%prefix% Invalid command.'
```

</details>

<details>

<summary>Click to view a list of all options within Section 2 - Default Command Messages</summary>

```yaml
#
#   ---------------  -  ------------------------------
#        Section 02  |  Default Command Messages
#   ---------------  -  ------------------------------
#
command:
  levelledmobs:
    main-usage:
      - '%prefix% Available commands:'
      - '&8 &m->&b /%label% debug &8- &7various commands relating to debugging'
      - '&8 &m->&b /%label% egg &8- &7create spawner eggs'
      - '&8 &m->&b /%label% help &8- &7show URL to the wiki'
      - '&8 &m->&b /%label% info &8- &7view info about the plugin'
      - '&8 &m->&b /%label% kill &8- &7mass kill levelled mobs'
      - '&8 &m->&b /%label% reload &8- &7reload the configuration files'
      - '&8 &m->&b /%label% rules &8- &7printout of the rules system'
      - '&8 &m->&b /%label% summon &8- &7summon specific levelled mobs'
```

</details>

<details>

<summary>Click to view a list of all options within Section 3 - Summon Command Messages</summary>

```yaml
#
#   ---------------  -  ------------------------------
#        Section 03  |  Summon Command Messages
#   ---------------  -  ------------------------------
#
    summon:
      invalid-amount:
        - '%prefix% Invalid amount ''&b%amount%&7''.'
      invalid-entity-type:
        - '%prefix% Invalid entity type ''&b%entityType%&7''.'
      invalid-level:
        - '%prefix% Invalid level ''&b%level%&7''.'
      invalid-summon-type:
        - '%prefix% Invalid summon type ''&b%summonType%&7''.'
      invalid-summon-type-console:
        - '%prefix% Only players may use summon type ''&bhere''&7, you must use ''&batPlayer&7'' or ''&batLocation&7'' instead.'
      invalid-location:
        - '%prefix% Invalid location.'
      here:
        usage:
          - '%prefix% Usage: &b/%label% summon <amount> <entity> <level> here'
        success:
          - '%prefix% Spawned &b%amount%&7 of &fLvl.%level% &b%entity%(s)&7 at your location.'
      atLocation:
        usage:
          - '%prefix% Usage: &b/%label% summon <amount> <entity> <level> atLocation <x> <y> <z> [world]'
        success:
          - '%prefix% Spawned &b%amount%&7 of &fLvl.%level% &b%entity%(s)&7 at &8(&b%x%&7, &b%y%&7, &b%z%&7 in world ''&b%world%&7''&8)&7.'
        usage-console:
          - '%prefix% Usage (console): &b/%label% summon <amount> <entity> <level> atLocation <x> <y> <z> <world>'
        invalid-world:
          - '%prefix% Invalid world ''&b%world%&7''.'
        invalid-location:
          - '%prefix% Invalid location.'
      atPlayer:
        usage:
          - '%prefix% Usage: &b/%label% summon <amount> <entityType> <level> atPlayer <player>'
        success:
          - '%prefix% Spawned &b%amount%&7 of &fLvl.%level% &b%entity%(s)&7 at &r%targetDisplayname%&7''s location.'
      usage:
        - '%prefix% Summon command syntax:'
        - '&8 &m->&b /%label% summon <amount> <entity> <level> here'
        - '&8 &m->&b /%label% summon <amount> <entity> <level> atPlayer <player>'
        - '&8 &m->&b /%label% summon <amount> <entity> <level> atLocation <x> <y> <z> [world]'
      amount-limited:
        min:
          - '%prefix% Summon amount limited to a minimum of &b1&7 mob.'
        max:
          - '%prefix% Summon amount limited to a maximum of &b%maxAmount%&7 mobs.'
      level-limited:
        min:
          - '%prefix% Level limited to a minimum of &bLvl.%minLevel%&7.'
        max:
          - '%prefix% Level limited to a maximum of &bLvl.%maxLevel%&7.'
      not-levellable:
        - '%prefix% &b%entity%&7 is not levellable.'
ix% Usage (console): /%label% kill all <world/*>'
      near:
        invalid-radius:
          - '%prefix% Invalid radius ''&b%radius%&7''.'
        invalid-radius-min:
          - '%prefix% Specified radius has been adjusted to the minimum radius &8(&b%minRadius%&8)&7.'
        invalid-radius-max:
          - '%prefix% Specified radius has been adjusted to the maximum radius &8(&b%maxRadius%&8)&7.'
        success:
          - '%prefix% Killed &b%killed%&7 levelled mobs within a radius of &b%radius%&7 block(s) &8(&b%skipped%&7 mobs were skipped&8)&7.'
        usage:
          - '%prefix% Usage: &b/%label% kill near <radius>'
```

</details>

<details>

<summary>Click to view a list of all options within Section 4 - Kill Command Messages</summary>

```yaml
#
#   ---------------  -  ------------------------------
#        Section 04  |  Kill Command Messages
#   ---------------  -  ------------------------------
#
    kill:
      usage:
        - '%prefix% Usage: &b/%label% kill <all/near>'
      all:
        invalid-world:
          - '%prefix% Invalid world ''&b%world%&7''.'
        success:
          - '%prefix% Killed &b%killed%&7 levelled mobs in &b%worlds%&7 world(s) &8(&b%skipped%&7 mobs were skipped&8)&7.'
        usage:
          - '%prefix% Usage: &b/%label% kill all [world/*]'
        usage-console:
          - '%prefix% Usage (console): /%label% kill all <world/*>'
      near:
        invalid-radius:
          - '%prefix% Invalid radius ''&b%radius%&7''.'
        invalid-radius-min:
          - '%prefix% Specified radius has been adjusted to the minimum radius &8(&b%minRadius%&8)&7.'
        invalid-radius-max:
          - '%prefix% Specified radius has been adjusted to the maximum radius &8(&b%maxRadius%&8)&7.'
        success:
          - '%prefix% Killed &b%killed%&7 levelled mobs within a radius of &b%radius%&7 block(s) &8(&b%skipped%&7 mobs were skipped&8)&7.'
        usage:
          - '%prefix% Usage: &b/%label% kill near <radius>'
```

</details>

<details>

<summary>Click to view a list of all options within Section 5 - Spawner Command Messages</summary>

```yaml
#
#   ---------------  -  ------------------------------
#        Section 05  |  Spawner Command Messages
#   ---------------  -  ------------------------------
#
    spawner:
      usage:
        - '%prefix% Spawner command syntax:'
        - '&8 &m->&b /%label% spawner create'
        - '&8 &m->&b /%label% spawner copy'
        - '&8 &m->&b /%label% spawner info'
        - ' '
        - '&fSample syntax:'
        - '&8 &m->&b /%label% spawner create &3/minlevel&b 1 &3/maxlevel&b 10 &3/name&b "My customized LM spawner" &3/customDropId&b Id1'
      no-value:
        - '%prefix% No value was specified for key ''&b%keyname%&7''.'
      no-player:
        - '%prefix% Command can only be run by a player unless the &b/giveplayer&7 parameter is specified.'
      invalid-value:
        - '%prefix% Invalid value for &b%keyname%&7, must be a number.'
      no-level-specified:
        - '%prefix% You must specify minLevel and/or maxLevel.'
      inventory-full:
        - '%prefix% Your inventory is full.'
      spawner-give-message:
        - '%prefix% Gave you a LM spawner.'
      spawner-give-message-console:
        - '%prefix% Gave &r%playername%&7 a LM spawner. &8|&7 minLevel: &b%minlevel%&7, maxLevel: &b%maxlevel%&7'
      permission-denied:
        - '%prefix% You don''t have permission to update or convert a LM spawner.'
      spawner-converted:
        - '%prefix% Converted vanilla spawner into a LM spawner with name "%spawnername%".'
      spawner-updated:
        - '%prefix% Updated LM spawner from spawn egg. Spawner name: "%spawnername%"'
      info:
        status-enabled:
          - '%prefix% Spawner info is &aenabled&f.'
        status-not-enabled:
          - '%prefix% Spawner info is &cnot enabled&f.'
        enabled:
          - '%prefix% Spawner info is &aenabled&f. Right-Click any Spawner for details!'
        disabled:
          - '%prefix% Spawner info has been &cdisabled&f.'
      copy:
        vanilla-spawner:
          - '%prefix% Spawner copy only works with LM spawners.'
        status-enabled:
          - '%prefix% Spawner copy is &aenabled&f.'
        status-not-enabled:
          - '%prefix% Spawner copy is &cnot enabled&f.'
        enabled:
          - '%prefix% Spawner copy is &aenabled&f. Right-Click a LM Spawner to make a copy.'
          - 'Your hand must be empty.'
        disabled:
          - '%prefix% Spawner copy has been &cdisabled&f.'
```

</details>

<details>

<summary>Click to view a list of all options within Section 6 - Spawn Egg Command Messages</summary>

```yaml
#
#   ---------------  -  ------------------------------
#        Section 06  |  Spawn Egg Command Messages
#   ---------------  -  ------------------------------
#
    spawn_egg:
      usage:
        - '%prefix% egg command syntax:'
        - '&8 &m->&b /%label% egg /minlevel <level> /maxlevel <level> /entity <entity type>'
        - '&7&o Sample Spawn Egg'
        - '&7/%label% egg &b/minlevel&7 1 &b/maxlevel&7 10 &b/name&7 "My customized LM spawn egg" &b/customDropId&7 Id1'
      no-paper:
        - '%prefix% This feature is only available on servers running Paper or forks of Paper'
      no-value:
        - '%prefix% No value was specified for: &b%keyname%&7'
      no-player:
        - '%prefix% Command can only be run by a player unless /giveplayer is specified'
      no-player-specified:
        - '%prefix% No player was specified'
      invalid-value:
        - '%prefix% Invalid value for &b%keyname%&7, must be a number'
      no-level-specified:
        - '%prefix% You must specify minLevel, maxLevel and entity'
      inventory-full:
        - '%prefix% &4Your inventory is full!'
      give-message:
        - '%prefix% Gave you a LM spawn egg'
      give-message-console:
        - '%prefix% Gave &r%playername%&7 a LM spawn egg. &8|&7 minLevel: &b%minlevel%&7, maxLevel: &b%maxlevel%&7, entity: &b%entitytype%&7'
```

</details>

<details>

<summary>Click to view a list of all options within Section 7 - Rules Command Messages</summary>

```yaml
#
#   ---------------  -  ------------------------------
#        Section 07  |  Rules Command Messages
#   ---------------  -  ------------------------------
#
    rules:
      incomplete-command:
        - '%prefix% Incomplete command'
      console-rules:
        - '%prefix% Rules have been printed on the console'
      discord-invite:
        - '%prefix% Click for Discord invite'
      wiki-link:
        - '%prefix% Click to open the wiki'
      rules-reprocessed:
        - '%prefix% Rules Reprocessed for &b%entitycount%&7 mobs in &b%worldcount%&7 world(s)'
      reset:
        - '%prefix% Running this command will reset your rules to one of 4 defaults.'
        - 'You must select if you want vanilla/basic/average/advanced/extreme difficulty.'
        - 'A backup will be made and your rules.yml reset to default.'
      resetting:
        - '%prefix% Resetting rules to %difficulty%'
      reset-syntax:
        - '%prefix% To reset your rules to %difficulty% difficulty, type in the following command:'
        - '%label% rules reset %difficulty% confirm'
      reset-complete:
        - '%prefix% rules.yml updated successfully'
      invalid-difficulty:
        - '%prefix% Invalid difficulty: %difficulty%'
      rule-name-missing:
        - '%prefix% Must specify a rule name.'
      rule-name-invalid:
        - '%prefix% No rule was found with name %rulename%'
      showing-rules:
        - 'Showing all values for rule: &b%rulename%&r'
      no-entities-visible:
        - '%prefix% Must be looking at a nearby entity'
      no-entities-near:
        - '%prefix% No entities were found within a 10 block radius'
      effective-rules:
        - '%prefix% Showing effective rules for: %entitytype% (lvl %level% %mobname%) in %world%, %location%'
      no-effective-rules:
        - '%prefix% No effective rules were found'
```

</details>

<details>

<summary>Click to view a list of all options within Section 8 - System Command Messages</summary>

```yaml
#
#   ---------------  -  ------------------------------
#        Section 08  |  System Command Messages
#   ---------------  -  ------------------------------
#
    reload:
      started:
        - '%prefix% Reloading configuration files...'
      finished:
        - '%prefix% Reload complete.'
      usage:
        - '%prefix% Usage: &b/%label% reload'
    info:
      about:
        - ' '
        - '&b&lLevelledMobs&b v%version%'
        - '&7&o%description%'
        - ' '
        - '&7Maintainers: &f%maintainers%'
        - '&7Contributors: &f%contributors%'
        - '&7Support for: &fMC &f%supportedVersions%'
        - ' '
      listSeparator: '&7, &f'
      usage:
        - '%prefix% Usage: &b/%label% info'
    compatibility:
      notice:
        - '%prefix% Compatibility checks have been printed to your logs. Please check the console :)'
      usage:
        - '%prefix% Usage: &b/%label% compatibility'
```

</details>

<details>

<summary>Click to view a list of all options within Section 9 - Other Messages</summary>

```yaml
#
#
#   ---------------  -  ------------------------------
#        Section 09  |  Other Messages
#   ---------------  -  ------------------------------
#
other:
  compatibility-notice:
    enabled: true
    messages:
      - '%prefix% LevelledMobs compatibility notice:'
      - '&8 &m->&r &b%incompatibilities% &7possible incompatibilities were found. Please run ''&b/levelledmobs compatibility&7'' to check them.'
      - '&8 &m->&7 This message is sent as you have the permission &blevelledmobs.compatibility-notice&7. You can disable this message in &bmessages.yml&7.'
      - '&8 &m->&7 Please ensure you have followed all instructions on the plugin''s Wiki page.'
  update-notice:
    messages:
      - '&b&nLevelledMobs Update Checker Notice:'
      - '&7Your &bLevelledMobs&7 version is &boutdated&7! Please update to &bv%latestVersion%&7 as soon as possible. &8(&7You''re running &bv%currentVersion%&8)'
    send-in-console: true
    send-on-join: true

  mob-head-drop-name: '%mob_name%''s head'
  no-drop-in-chunk: '%prefix% &7Your levelled mob kill count has reached the maximum for this area. You will no longer receive levelled drops from these mobs. Please come back after a while.'
  create-debug:
    - '&b&nCreate a Debugging ZIP'
    - '&7You should only run this command if a LevelledMobs developer has asked you to. It is used to assist users who are experiencing issues with the plugin.'
    - ''
    - '&7This command will generate a ZIP file containing the following required data:'
    - '&8 &m->&b Plugins list'
    - '&8 &m->&b Server version'
    - '&8 &m->&b Current and maximum online player count'
    - '&8 &m->&b The latest.log file&7 &8(/logs/latest.log)'
    - ''
    - '&7LevelledMobs developers will not redistribute or retain the data beyond the purpose of resolving any issue you may be experiencing. You may also verify the contents prior to sending the file.'
    - '&7To proceed in creating the ZIP file, please run:'
    - '&b/lm debug create-zip confirm&7'
```

</details>

***

<table><thead><tr><th width="223" align="center">Config Line Option</th><th>Description</th></tr></thead><tbody><tr><td align="center"><code>%prefix%</code></td><td>The prefix LevelledMobs uses before any messages sent via the plugin.</td></tr><tr><td align="center"><code>%player%</code></td><td>The name of the player who the event is directed towards.</td></tr><tr><td align="center"><code>%label%</code></td><td>The main command alias used when running LM's commands.<strong>Example:</strong> <code>/lm</code> or <code>/levelledmobs</code></td></tr><tr><td align="center"><code>%amount%</code></td><td>The input value of the event.</td></tr><tr><td align="center"><code>%entityType%</code></td><td>The <code>EntityType</code> value of the event.</td></tr><tr><td align="center"><code>%level%</code></td><td>The level of the entity from the event being processed.</td></tr><tr><td align="center"><code>%summonType%</code></td><td>The input value of the summon <code>EntityType</code></td></tr><tr><td align="center"><code>%entity%</code></td><td>The nametag, <code>CustomName</code>, or default name value of the entity being processed.</td></tr><tr><td align="center"><code>%x%</code> <code>%y%</code> <code>%z%</code></td><td>These three tags report back the <strong>X</strong>, <strong>Y</strong>, and <strong>Z</strong> coordinates of the event.</td></tr><tr><td align="center"><code>%world%</code></td><td>The value of the world name where the event took place.</td></tr><tr><td align="center"><code>%targetUsername%</code></td><td>The username of the target of the event.</td></tr><tr><td align="center"><code>%targetDisplayname%</code></td><td>The displayname of the target of the event.</td></tr><tr><td align="center"><code>%maxAmount%</code></td><td>Returns the value of the <em><strong>Summon Command Limiter</strong></em> from <code>settings.yml</code>.</td></tr><tr><td align="center"><code>%minLevel%</code> <code>%%maxLevel%</code></td><td>Returns the <code>minLevel</code> and <code>maxLevel</code> value present during the processed event.</td></tr><tr><td align="center"><code>%killed%</code></td><td>Returns the number of entities which were killed during the processed event.</td></tr><tr><td align="center"><code>%skipped%</code></td><td>Returns the number of entities which were skipped during a LM kill event.</td></tr><tr><td align="center"><code>%radius%</code></td><td>The input value of the radius used in LM's summon command.</td></tr><tr><td align="center"><code>%minRadius%</code> <code>%maxRadius%</code></td><td>Returns the minimum and maximum radius value.</td></tr><tr><td align="center"><code>%version%</code></td><td>Returns the current version of LM, formatted <code>LM X.Y.Z b000</code>, where <code>X.Y.Z</code> represents the release version and <code>b000</code> represents the actual build number.</td></tr><tr><td align="center"><code>%description%</code></td><td>Returns the internal LM description text.</td></tr><tr><td align="center"><code>%supportedVersions%</code></td><td>Returns the internal LM supported version text.</td></tr><tr><td align="center"><code>%contributors%</code></td><td>Returns the internal LM contributors list text.</td></tr><tr><td align="center"><code>%incompatibilities%</code></td><td>Returns the internal LM incompatibilities text.</td></tr></tbody></table>
