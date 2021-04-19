---
title: ApplicationMenu 屬性
description: 表示應用程式功能表。 |ApplicationMenu 屬性
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- ApplicationMenu 屬性視窗功能區
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986068"
---
# <a name="ribbonapplicationmenu-property"></a>ApplicationMenu 屬性

表示應用程式功能表。

## <a name="usage"></a>使用方式

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素



| 元素                                                                     | 描述                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/> | 必須剛好發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                   |
|-----------------------------------------------------------|
| [**功能區**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>備註

必要。

每個 [**功能區**](windowsribbon-element-ribbon.md)最多可能會發生一次。

## <a name="examples"></a>範例

下列範例示範 **ApplicationMenu** 元素的基本標記。

這段程式碼會顯示 **ApplicationMenu** 控制項宣告。


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/> |



 

 





