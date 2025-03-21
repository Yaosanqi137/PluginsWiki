---
sidebar_position: 2
---

# 城镇

城镇是HuskTowns的社会和经济核心，允许用户建立一个社会，[创建领地](claims)，[管理关系](Relations)，如果启用，甚至可以[发动战争](Wars)。玩家可以创建一个新的城镇，或者接受其他玩家的邀请加入一个城镇。你一次只能加入一个城镇，每个城镇有一个市长。

## 1. 创建城镇
要创建一个城镇，输入`/town create <名称>`。这将创建一个等级为1的新城镇，并赋予它指定的名称。

如果你的服务器启用了`towns.require_first_level_collateral`设置，那么创建城镇将花费在[`levels.yml`](config-files)中定义的“等级1”的价格。名称不能包含任何空白字符。

### 1.1 自定义
你可以更改城镇的颜色、简介、欢迎和告别消息。每个更改都会影响其他玩家对你的城镇的看法。
* **城镇颜色**—在领地地图上显示的颜色。使用`/town color <#rgb>`更改
* **城镇简介**—在`/town info <名称>`页面和`/town list`中悬停时显示的城镇简介。使用`/town bio <消息>`更改
* **城镇欢迎消息**—当玩家进入你的领地时显示的消息。使用`/town greeting <消息>`更改
* **城镇告别消息**—当玩家离开你的领地时显示的消息。使用`/town farewell <消息>`更改

如果你改变了主意，也可以使用`/town rename <名称>`重命名城镇。

### 1.2 城镇信息页面
所有城镇都有一个城镇信息页面，显示每个城镇的一些重要信息，如等级、人口数量、领地数量、市长、银行余额、出生点位置等。

如果你是城镇的成员，单独运行`/town`命令将显示你的城镇信息页面。如果你想查看其他城镇的信息页面，使用`/town about <名称>`。

### 1.3 城镇列表
你可以使用`/town list`命令查看城镇列表。如果创建了很多城镇，你可以使用分页和过滤按钮来更改列表排序。点击列表中的城镇名称将显示其城镇信息页面。

### 1.4 城镇聊天
你可以使用`/town chat <消息>`向城镇成员发送私密消息。

## 2. 添加成员
你可以使用`/town invite <玩家>`邀请成员加入你的城镇。注意你只能邀请当前不是任何城镇成员的玩家。

### 2.1 管理权限
你可以根据服务器设置的城镇角色层次结构提升或降级成员。要提升成员，使用`/town promote <成员>`。同样，要降级用户，使用`/town demote <成员>`。注意你不能提升或降级与你角色相同或更高的成员。

### 2.2 权限
层次结构中的每个角色都有相关的权限，包括从较低层次角色继承的权限。例如，默认情况下，只有市长可以重命名城镇，只有受托人可以邀请其他成员。

<details>
<summary>默认角色层次结构</summary>

| 角色权重 | 角色名称 | 权限                                                                                                                                                                                   |
|:-----------:|:---------:|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|      3      |   市长   | `set_bio`, `evict`, `promote`, `demote`, `withdraw`, `level_up`, `set_rules`, `rename`, `set_color`, `declare_war`                                                                           |
|      2      |  受托人  | `set_farm`, `set_plot`, `manage_plot_members`, `trusted_access`, `unclaim`, `claim`, `set_greeting`, `set_farewell`, `invite`, `set_spawn`, `manage_relations`, `spawn_privacy`, `view_logs` |
|      1      | 居民  | `deposit`, `chat`, `claim_plot`, `spawn`                                                                                                                                                     |

</details>

有关角色自定义的更多信息，请参见[[角色]]。

### 2.3 城镇人口普查 / 成员列表
要查看任何给定城镇的成员列表，按角色分组，使用`/town census [名称]`命令。

### 2.4 驱逐成员
如果你有权限，可以使用`/town evict <成员>`驱逐成员。注意你不能驱逐与你角色相同或更高的成员。

### 2.5 离开城镇
如果你想离开你的城镇，可以使用`/town leave`。市长不能离开自己的城镇；他们必须先转移所有权或删除它。

### 2.6 转移和删除
城镇的市长可以使用`/town transfer <成员>`将所有权转移给城镇的另一个成员。如果他们愿意，也可以选择使用`/town delete`删除城镇，这将同时移除所有城镇的领地。

## 3. 提升城镇等级
城镇有一个银行余额（“金库”）和等级，等级从1开始。通过提升城镇等级，你可以增加城镇的最大领地和成员数量，以及在城镇的农场区块中获得作物生长速度和怪物生成器生成速度的提升。

要提升城镇等级，你必须使用`/town deposit <金额>`将钱存入城镇金库。当你的城镇达到升级门槛时，你可以使用`/town levelup`从城镇金库中花费金钱将城镇等级提升1级。有权限的成员也可以随时使用`/town withdraw <金额>`从城镇金库中取款。

### 3.1 等级要求
如果你是管理员，可以通过修改`levels.yml`文件来编辑这些要求。

<details>
<summary>默认等级要求</summary>

| 等级 | 升级成本  | 领地 | 成员 |
|:-----:|---------------|:------:|:-------:|
|   1   | 2,000         |   6    |    5    |
|   2   | 4,000         |   12   |   10    |
|   3   | 8,000         |   18   |   15    |
|   4   | 16,000        |   24   |   20    |
|   5   | 32,000        |   30   |   25    |
|   6   | 64,000        |   36   |   30    |
|   7   | 128,000       |   42   |   35    |
|   8   | 256,000       |   48   |   40    |
|   9   | 512,000       |   54   |   45    |
|  10   | 1,024,000     |   60   |   50    |
|  11   | 2,048,000     |   66   |   55    |
|  12   | 4,096,000     |   72   |   60    |
|  13   | 8,192,000     |   78   |   65    |
|  14   | 16,384,000    |   84   |   70    |
|  15   | 32,768,000    |   90   |   75    |
|  16   | 65,536,000    |   96   |   80    |
|  17   | 131,072,000   |  102   |   85    |
|  18   | 262,144,000   |  108   |   90    |
|  19   | 524,288,000   |  114   |   95    |
|  20   | 1,048,576,000 |  120   |   100   |

</details>

## 4. 城镇出生点
你的城镇有一个可以传送到的出生点，它必须位于你的城镇[[领地]]之一。要设置城镇出生点，使用`/town setspawn`。城镇成员可以使用`/town spawn`返回出生点。

### 4.1 出生点隐私
如果你希望允许城镇外的成员传送到你的城镇出生点，使用`/town privacy public`将出生点设为公开。任何人都可以使用`/town spawn <名称>`进行访问。

## 5. 城镇关系
如果你启用了[[关系]]，你可以使用`/town relations`命令设置与服务器上其他城镇的关系。