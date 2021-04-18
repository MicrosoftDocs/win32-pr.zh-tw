---
title: FlowMenuLayout 元素
description: 代表包含資源庫中專案之分行符號的水準配置。
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- FlowMenuLayout 元素視窗功能區
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965407"
---
# <a name="flowmenulayout-element"></a>FlowMenuLayout 元素

代表包含資源庫中專案之分行符號的水準配置。

## <a name="usage"></a>使用方式

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
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
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>資料行</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>指定要在單一資料列中顯示的專案數。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： integer) <br/> </dt> <dd> 任何正整數或負整數。 <br/> 預設值為 <strong>2</strong>。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>片 梭</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>附加至圖庫下拉式清單的調整大小控點。 <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> 限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (無) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (垂直) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (角落) <br/> </dt> <dd> 預設值。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>資料列</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
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

[**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)或 **FlowMenuLayout** 元素必須針對每個 [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)、 [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery-menulayout.md)專案進行一次。

專案會根據資料 *列* 和資料 *行* 屬性固有的行分隔屬性來排列。 當內容超過單行的長度時，功能表會中斷線條、換行，並適當地對齊內容。

## <a name="examples"></a>範例

下列範例示範 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)的基本標記。

這一段程式碼會顯示具有 **FlowMenuLayout** 規格的 [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)控制項宣告。


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a>項目資訊



|                                     |           |
|-------------------------------------|-----------|
| 最低支援系統<br/> | Windows 7 |
| 可以是空的                        | 是       |



 

 





