# 管理导航栏

In Menu management page, you can

This article instructs how to create and manage navigation panel. You also can synchronize the menu to IAM for Authorization purpose.

# Manage navigation panel
系统管理员可以新建或编辑平台产品模块的菜单信息，同步菜单信息（顺序、ID）到IAM并进行注册。同步完成后，组织的管理员用户可以通过**IAM>策略管理**，创建策略并选择需要被授权的菜单。

OU owner can create and edit the navigation panel of the EnOS console based on the service module.

添加菜单时，需要选择菜单的父节点（分类、一级菜单）。若无，需要先添加父节点。平台支持最多两级菜单。

## 修改导航栏布局/修改分类

1. 点击“添加分类”，填写分类信息，包括键值ID，中文名，英文名。其中，键值ID最大长度为64个字符，全局唯一。
2. 选中“已有分类”，点击“编辑”，可以修改分类信息。

## 菜单管理

### 添加一级菜单

当父节点为分类时，添加一级菜单的方式如下：

1. 选择目标**分类**，
2. 点击**添加菜单**，填写详细信息：

  - 键值ID：最大长度64个字符，全局唯一，格式platform-{modulename}
  - 父节点：所选”分类“，或下拉选择其它分类或一级菜单
  - 图标：下拉并在系统提供的图标库中选择
  - 中文名：最大长度64个字符，全局唯一
  - 英文名：最大长度64个字符，全局唯一
  - 是否默认显示在常用菜单中：选择“否”，则默认在左侧导航中的”全部“一栏；选择”是“，则默认在左侧导航栏中的”常用“一栏

  - 是否默认显示在顶部导航中：默认选择”否“

  - 赋权：赋权方式，支持“通过IAM赋权”，“所有人可见”，“仅平台管理员可见”三种方式

  - 点击“保存”，完成一级菜单创建

  - 同步菜单信息（顺序、ID）到IAM并进行注册

当父节点为“一级菜单”时，添加二级菜单的方式如下：

- 选择目标“一级菜单”

- 点击“添加菜单”，填写菜单信息：

  + 键值ID：最大长度64个字符，全局唯一，格式platform-{modulename}-{pagename}

  + 父节点：所选“一级菜单”，或下拉选择其他分类或一级菜单

  + URL：菜单的URL

  + 是否在新Tab页打开：默认为否

  + 图标：下拉并在系统提供的图标库中选择

  + 中文名：最大长度64个字符，全局唯一

  + 英文名：最大长度64个字符，全局唯一

- 点击“保存“，完成二级菜单创建

- 同步菜单信息（顺序、ID）到IAM并进行注册