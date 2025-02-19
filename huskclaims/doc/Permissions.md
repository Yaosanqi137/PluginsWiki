---
sidebar_position: 2
---

# 权限

<table align="right">
    <thead>
        <tr><th colspan="2">Key</th></tr>
    </thead>
    <tbody>
        <tr><td>✅</td><td>默认情况下所有玩家均可访问</td></tr>
        <tr><td>❌</td><td>默认情况下仅服务器管理员可访问</td></tr>
    </tbody>
</table>

HuskClaims 提供了用于限制对命令和功能访问的权限。

这些权限的详细信息如下。

## 命令
请参阅 [[Commands]] 页面以获取完整的命令列表及其权限。

## 检查
这些权限限制了检查领地的能力。

| 权限                          | 描述                                                                                   | 默认 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|---------|
| `huskclaims.inspect`                | 使用检查工具检查领地。                                                      | ✅       |
| `huskclaims.inspect.nearby`         | 通过按住 SNEAK 并使用检查工具检查附近的所有领地。                     | ✅       |
| `huskclaims.inspect.view_last_seen` | 在检查时，用户是否可以查看领地所有者上次登录的天数。 | ❌       |

## 领地
这些权限限制了创建某些类型领地的能力。有关领地的更多详细信息，请参阅 [[Claims]]。还可以在插件配置中禁用创建管理员/子领地。

| 权限               | 描述                                                     | 默认 |
|--------------------------|-----------------------------------------------------------------|:-------:|
| `huskclaims.claim`       | 创建常规用户拥有的领地。                               |    ✅    |
| `huskclaims.admin_claim` | 创建管理员领地，**并管理所有其他管理员领地。**     |    ❌    |
| `huskclaims.child_claim` | 创建子领地；在父领地内划分土地。 |    ✅    |

## 信任标签
这些权限限制了在向其他玩家授予信任时使用某些信任标签的能力。有关信任标签的更多详细信息，请参阅 [[Trust]]。

| 权限                   | 描述                                                                                                    | 默认 |
|------------------------------|----------------------------------------------------------------------------------------------------------------|:-------:|
| `huskclaims.trust.public`    | 在领地中使用 `#public` 信任标签以授予公共访问权限。                                                  |    ✅    |
| `huskclaims.trust.luckperms` | 在领地中使用 `#role/(name)` 信任标签以授予基于 LuckPerms 角色的访问权限。需要 LuckPerms 钩子。 |    ❌    |

您可以在 [[config]] 钩子设置中关闭在领地中使用 LuckPerms 组的权限要求。
