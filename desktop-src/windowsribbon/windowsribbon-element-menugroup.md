---
title: MenuGroup 元素
description: 表示要在圖庫、功能表或工具列中顯示的控制項容器。
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- MenuGroup 元素 Windows 功能區
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dad52aebe4a90d132827f01400fc7a1f2bbf1fde
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624714"
---
# <a name="menugroup-element"></a>MenuGroup 元素

表示要在圖庫、功能表或工具列中顯示的控制項容器。

## <a name="usage"></a>使用方式

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
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
<td><strong>類別</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>指定功能表 UI 中元素的大小和配置樣式。<br/> 您可以使用 <a href="windowsribbon-element-command-largeimages.md"><strong>LargeImages</strong></a> 和 <a href="windowsribbon-element-command-smallimages.md"><strong>SmallImages</strong></a> 屬性專案，以兩種大小提供影像資源 (大型和小型) ，並與標記中的元素相關聯。 如果只提供一個影像，則架構會視需要調整其大小。<br/> 限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (StandardItems) <br/> </dt> <dd> 預設值。 <br/> 樣式：小型影像和反白的文字。<br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <dt><span></span><span></span><strong></strong> (MajorItems) <br/> </dt> <dd> 樣式：大型影像和粗體文字。<br/>
<blockquote>
[!Note]<br />
如果 <strong>MenuGroup</strong> 是 <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>的子系，則會忽略 <em>類別</em> 屬性，而 <code>MajorItems</code> 架構會強制執行的樣式。
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>否<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素



| 元素                                                                             | 描述                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Button**](windowsribbon-element-button.md)<br/>                           | 可能會發生一次或多次<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                       | 可能會發生一次或多次<br/> <br/> |
| [**ComboBox**](windowsribbon-element-combobox.md)<br/>                       | 可能會發生一次或多次<br/> <br/> |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>           | 可能會發生一次或多次<br/> <br/> |
| [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)<br/> | 可能會發生一次或多次<br/> <br/> |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>         | 可能會發生一次或多次<br/> <br/> |
| [**FontControl**](windowsribbon-element-fontcontrol.md)<br/>                 | 最多可能發生一次<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                 | 可能會發生一次或多次<br/> <br/> |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/>   | 可能會發生一次或多次<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>               | 可能會發生一次或多次<br/> <br/> |



## <a name="parent-elements"></a>父元素



| 元素                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/>                             |
| [**ContextMenu**](windowsribbon-element-contextmenu.md)<br/>                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [**浮動工具列**](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [**SplitButton. MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a>備註

必要。

每個 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)、 [**CoNtextMenu**](windowsribbon-element-contextmenu.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery-menugroups.md)、MenuGroups、 [**InRibbonGallery**](windowsribbon-element-inribbongallery-menugroups.md) [**、MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)、SplitButton、 [**MenuGroups**](windowsribbon-element-minitoolbar.md)或 [**浮動工具列**](windowsribbon-element-splitbuttongallery-menugroups.md) 元素都必須至少發生一次。

如果 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) 是父元素，則 **MenuGroup** 會限制為下列子項目： [**Button**](windowsribbon-element-button.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)。

如果 [**CoNtextMenu**](windowsribbon-element-contextmenu.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery、MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)、 [**InRibbonGallery**](windowsribbon-element-inribbongallery-menugroups.md)、 [**MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)、SplitButton 或 [**MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) 是父元素，則 **SplitButtonGallery** 會限制為下列子項目： [**Button**](windowsribbon-element-button.md)、 [**CheckBox**](windowsribbon-element-checkbox.md)、 **MenuGroups**、 [**MenuGroup**](windowsribbon-element-dropdowncolorpicker.md)、 [**DropDownButton**](windowsribbon-element-dropdowngallery.md)、 [**DropDownColorPicker**](windowsribbon-element-splitbutton.md)、 [**DropDownGallery**](windowsribbon-element-splitbuttongallery.md)或 [**切換按鈕**](windowsribbon-element-togglebutton.md)。

如果 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 是父元素，則 **MenuGroup** 會限制為下列子項目： [**Button**](windowsribbon-element-button.md)、 [**CheckBox**](windowsribbon-element-checkbox.md)、 [**ComboBox**](windowsribbon-element-combobox.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**FontControl**](windowsribbon-element-fontcontrol.md)、 [**微調**](windowsribbon-element-spinner.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)、 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)或 [**切換按鈕**](windowsribbon-element-togglebutton.md)。

當 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) 是父元素時，不需要類別屬性。 架構會強制執行類別屬性的 MajorItems 值。

當 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) 是父元素時，不需要類別屬性。

## <a name="examples"></a>範例

下列範例示範具有 **MenuGroup** 元素之 [**SplitButton**](windowsribbon-element-splitbutton.md)的基本標記。

這段程式碼會顯示具有大型和小型影像資源的 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 **MenuGroup** 命令宣告。 也會宣告作為 **SplitButton** 專案父容器的相關聯 [**群組**](windowsribbon-element-group.md)。


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



這段程式碼會以和來顯示 [**SplitButton**](windowsribbon-element-splitbutton.md) 和 **MenuGroup** 控制項 `StandardItems` 宣告 `MajorItems` 。


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a>項目資訊

* **最低支援系統**： Windows 7
* **可以是空** 的：否



## <a name="see-also"></a>另請參閱

<dl> <dt>

[指定功能區影像資源](windowsribbon-imageformats.md)
</dt> <dt>

[功能表群組](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





