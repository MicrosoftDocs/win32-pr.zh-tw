---
title: RecentItems 元素
description: 代表 [應用程式] 功能表中的 [最近的專案] 控制項。
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- RecentItems 元素視窗功能區
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a433e2f04eae8607b0c14c5494c734ad0f0dd83a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444109"
---
# <a name="recentitems-element"></a>RecentItems 元素

代表 [[應用程式] 功能表](windowsribbon-controls-applicationmenu.md)中的 [[最近的專案](windowsribbon-controls-recentitems.md)] 控制項。

## <a name="usage"></a>使用方式

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a>屬性



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<tr class="even">
<td><strong>EnablePinning</strong><br/></td>
<td>Boolean<br/></td>
<td>否<br/></td>
<td>限制為下列其中一個值 (0 和1不是有效的) ：<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 預設值。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxCount</strong><br/></td>
<td>xs:nonNegativeInteger<br/></td>
<td>否<br/></td>
<td>要顯示的最近專案數目。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： nonNegativeInteger) <br/> </dt> <dd> 0或大於零的整數值。<br/> 預設值為 <strong>10</strong>。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a>備註

必要。

必須針對每個 [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) 元素剛好出現一次。

[ [最近](windowsribbon-controls-recentitems.md) 使用的專案] 控制項會顯示功能區應用程式最近使用的 (MRU) Items 清單。

## <a name="examples"></a>範例

下列範例將示範 [ [最近使用的專案](windowsribbon-controls-recentitems.md) ] 控制項的基本標記。

下列範例顯示 **RecentItems** 命令聲明。


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



下列範例顯示相關聯的 **RecentItems** 控制項宣告。


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a>項目資訊

* **最低支援系統**： Windows 7
* **可以是空** 的：是


## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式功能表控制項](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[最近的專案控制項](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





