---
title: CheckBox 元素
description: 表示核取方塊控制項。
ms.assetid: ebb44d6d-91fb-4a59-9b62-4a694fea8a4d
keywords:
- CheckBox 元素視窗功能區
topic_type:
- apiref
api_name:
- CheckBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0af090058e0475f1997c681750009a12f4e5e7cd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104092524"
---
# <a name="checkbox-element"></a>CheckBox 元素

表示 [核取方塊](windowsribbon-controls-checkbox.md) 控制項。

## <a name="usage"></a>使用方式

``` syntax
<CheckBox
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
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
<td><strong>S. IsChecked</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>只有當 <strong>CheckBox</strong> 元素是 <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a>的子系時，這個屬性才有效。 <br/> 限制為下列其中一個值：<br/>
<blockquote>
[!Note]<br />
此 <strong>核取方塊</strong> 不支援第三個或不定的狀態。
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 預設值。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>No<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [**Group**](windowsribbon-element-group.md)<br/>                                                                   |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                                                           |
| [**QuickAccessToolbar. s**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>備註

選擇性或必要，視父元素而定。

可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)、s、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。

## <a name="examples"></a>範例

下列範例示範 **CheckBox** 元素的基本標記。

這一節的程式碼會顯示 **核取方塊** 命令聲明。


```XML
<Command Name="cmdCheckBoxGroup"
         Symbol="cmdCheckBoxGroup"
         Comment="CheckBox Group"
         LabelTitle="CheckBoxGroup"/>
<Command Name="cmdCheckBox"
         Symbol="cmdCheckBox"
         Comment="CheckBox"
         LabelTitle="CheckBox"/>
```



這段程式碼會顯示 **CheckBox** 控制項宣告。


```XML
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
```



## <a name="element-information"></a>項目資訊



|                                     |           |
|-------------------------------------|-----------|
| 最低支援系統<br/> | Windows 7 |
| 可以是空的                        | Yes       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[核取方塊控制項](windowsribbon-controls-checkbox.md)
</dt> </dl>

 

 





