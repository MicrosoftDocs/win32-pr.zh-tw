---
title: Group 元素
description: 代表做為元素群組之容器的群組控制項。
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- 群組元素視窗功能區
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375965"
---
# <a name="group-element"></a>Group 元素

代表做為元素群組之容器的 [群組](windowsribbon-controls-group.md) 控制項。

## <a name="usage"></a>使用方式

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 字串，其中包含0到31之間的整數清單（以逗號分隔）。<br/> 空白字元是有效的，而且會被忽略。<br/> 最大長度：250個字元。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>No<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>SizeDefinition</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>當指定時， <em>SizeDefinition</em> 的值會限制為功能區架構所定義的其中一個 <a href="windowsribbon-templates.md">版面配置範本</a> 。 <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： string) <br/> </dt> <dd> 任何零或多個字元的序列。<br/> 長度上限為未系結。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                                             | 描述                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | 可能會發生一次或多次<br/> <br/> |
| [**相應**](windowsribbon-element-checkbox.md)<br/>                       | 可能會發生一次或多次<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | 可能會發生一次或多次<br/> <br/> |
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>               | 可能會發生一次或多次<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | 可能會發生一次或多次<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | 可能會發生一次或多次<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | 可能會發生一次或多次<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | 最多可能發生一次<br/> <br/>      |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/>         | 可能會發生一次或多次<br/> <br/> |
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/>           | 最多可能發生一次<br/> <br/>      |
| [**Spinner**](windowsribbon-element-spinner.md)<br/>                         | 可能會發生一次或多次<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | 可能會發生一次或多次<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | 可能會發生一次或多次<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | 可能會發生一次或多次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                             |
|-----------------------------------------------------|
| [**索引標籤**](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

每個索引標籤元素可能會 [**發生一次**](windowsribbon-element-tab.md) 或多次。

[**Tab**](windowsribbon-element-tab.md) 支援 [應用程式模式](ribbon-applicationmodes.md)。

只有當 **群組** 的子項目對應到針對 *SizeDefinition* 指定的範本時，功能區標記才有效。

## <a name="examples"></a>範例

下列程式碼範例說明如何在 **群組** 中使用自訂範本。


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a>項目資訊



|                                     |           |
|-------------------------------------|-----------|
| 最低支援系統<br/> | Windows 7 |
| 可以是空的                        | 否        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)
</dt> <dt>

[群組控制項](windowsribbon-controls-group.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

