---
title: VerticalMenuLayout 元素
description: 代表資源庫中專案的垂直版面配置。
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- VerticalMenuLayout 元素 Windows 功能區
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 732fff993e4ac4e1caf8637c1f83804636bf6882
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623294"
---
# <a name="verticalmenulayout-element"></a>VerticalMenuLayout 元素

代表資源庫中專案的垂直版面配置。

## <a name="usage"></a>使用方式

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
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
<td><strong>片 梭</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>附加至圖庫下拉式清單的調整大小控點。 <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> 限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (無) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (垂直) <br/> </dt> <dd> 預設值。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsMultipleHighlightingEnabled</strong><br/></td>
<td>xs:boolean<br/></td>
<td>否<br/></td>
<td><strong>Windows 8 和更新版本</strong><br/> 將清單中的所有專案反白顯示，並包含目前的滑鼠懸停專案 (而不是僅) 滑鼠停用的專案。 通常用於多個 <strong>復原</strong> 和 <strong>重做</strong> 功能。<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd> 預設值。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>資料列</strong><br/></td>
<td>xs:integer<br/></td>
<td>否<br/></td>
<td>指定要顯示但不需要滾動的專案資料列數目。 <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd> 任何正整數或負整數。 <br/> 預設值為 <strong>-1</strong> ，指定盡可能顯示最多的專案資料列。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a>備註

必要。

**VerticalMenuLayout** 或 [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)元素必須針對每個 [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)、 [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery-menulayout.md)專案進行一次。

## <a name="examples"></a>範例

下列範例示範 **VerticalMenuLayout** 元素的基本標記。

這段程式碼會顯示 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 控制項宣告。


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a>項目資訊


- **最低支援系統**： Windows 7 
- **可以是空** 的：是



 

 





