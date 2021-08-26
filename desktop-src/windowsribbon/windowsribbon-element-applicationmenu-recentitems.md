---
title: ApplicationMenu. RecentItems 屬性
description: 代表 [應用程式] 功能表中 [最近的專案] 控制項的容器。
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- ApplicationMenu. RecentItems 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cfb5152cd1d9cc4d27abfa3432666f06880d8e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630373"
---
# <a name="applicationmenurecentitems-property"></a>ApplicationMenu. RecentItems 屬性

代表 [[應用程式] 功能表](windowsribbon-controls-applicationmenu.md)中 [[最近的專案](windowsribbon-controls-recentitems.md)] 控制項的容器。

## <a name="usage"></a>使用方式

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>類型</th>
<th>必要</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>否<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                             | 描述                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [**RecentItems**](windowsribbon-element-recentitems.md)<br/> | 必須剛好發生一次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                     |
|-----------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) 元素最多可能會發生一次。

[ [最近](windowsribbon-controls-recentitems.md) 使用的專案] 控制項會顯示功能區應用程式最近使用的 (MRU) Items 清單。

## <a name="examples"></a>範例

下列範例將示範 [ [最近使用的專案](windowsribbon-controls-recentitems.md) ] 控制項的基本標記。

下列範例顯示 [**RecentItems**](windowsribbon-element-recentitems.md) 命令聲明。


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



下列範例顯示相關聯的 **ApplicationMenu RecentItems** 和 [**RecentItems**](windowsribbon-element-recentitems.md) 控制項宣告。


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式功能表控制項](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[最近的專案控制項](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





