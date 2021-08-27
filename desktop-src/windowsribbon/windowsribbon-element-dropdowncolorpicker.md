---
title: DropDownColorPicker 元素
description: 表示按一下以顯示色板的 Drop-Down 色彩 Pickercontrol。
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- DropDownColorPicker 元素 Windows 功能區
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31525ee1b7233f0bf49668856d917ef14bc034b6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622884"
---
# <a name="dropdowncolorpicker-element"></a>DropDownColorPicker 元素

表示當按一下以顯示色板時的 [下拉式色彩選擇器](windowsribbon-controls-dropdowncolorpicker.md)控制項。

## <a name="usage"></a>使用方式

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
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
<td><strong>ChipSize</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>每個色晶片或樣本的大小。 <br/> 限制為下列其中一個值：<br/> <br/>
<dt><span></span><span></span><strong></strong> (Small) <br/> </dt> <dd> 每個色晶片都是11x11 圖元正方形。 <br/> </dd> <dt><span></span><span></span><strong></strong> (中) <br/> </dt> <dd> 每個色晶片都是16x16 圖元正方形。 <br/> </dd> <dt><span></span><span></span><strong></strong> (大型) <br/> </dt> <dd> 每個色晶片都是24x24 圖元正方形。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ColorTemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>否<br/></td>
<td>指定 <a href="windowsribbon-controls-dropdowncolorpicker.md">下拉式色彩選擇器</a>類型的版面配置範本。 <br/> 限制為下列其中一個值 (如果未宣告與 <em>ColorTemplate</em> 相關的選擇性屬性，則會顯示) 的預設視圖：<br/> <br/>
<dt><span></span><span></span><strong></strong> (ThemeColors) <br/> </dt> <dd> 預設值。 <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> 將 <em>ColorTemplate</em> 屬性設定為可 <code>ThemeColors</code> 啟用下列功能：<br/>
<ul>
<li>SplitButton 錨點。</li>
<li>預設會顯示 [<strong>自動</strong>色彩] 按鈕。</li>
<li>Windows<strong>主題色彩</strong>] 色板方格。</li>
<li><strong>標準色彩</strong> 樣本方格。</li>
<li>[<strong>最近使用的色彩</strong>] 樣本方格是選擇性的。</li>
<li>[<strong>其他色彩</strong>] 對話方塊啟動器。</li>
<li>預設不會顯示<strong>色彩</strong>色彩按鈕。</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (StandardColors) <br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> 將 <em>ColorTemplate</em> 屬性設定為可 <code>StandardColors</code> 啟用下列功能：<br/>
<ul>
<li>SplitButton 錨點。</li>
<li>預設會顯示 [<strong>自動</strong>色彩] 按鈕。</li>
<li><strong>標準色彩</strong> 樣本方格。</li>
<li>[<strong>其他色彩</strong>] 對話方塊啟動器。</li>
<li>預設不會顯示<strong>色彩</strong>色彩按鈕。</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (HighlightColors) <br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> 將 <em>ColorTemplate</em> 屬性設定為可 <code>HighlightColors</code> 啟用下列功能：<br/>
<ul>
<li>SplitButton 錨點。</li>
<li>沒有標頭的<strong>標準色彩</strong>樣本方格。</li>
<li>預設不會顯示<strong>色彩</strong>色彩按鈕。</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>資料行</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>否<br/></td>
<td>色板 (或樣本) 資料行的數目。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) <br/> </dt> <dd> 介於1和256之間的任何正整數值（含）。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs： positiveInteger 或 xs： string<br/></td>
<td>否<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsAutomaticColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>否<br/></td>
<td>顯示 (或隱藏) [ <strong>自動</strong> 色彩] 按鈕。 <br/> 只有在 <code>StandardColors</code> <code>ThemeColors</code> 為 <em>ColorTemplate</em> 屬性指定或時有效。 <br/> 限制為下列其中一個值 (0 和1不是有效的) ：<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsNoColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>否<br/></td>
<td>顯示 (或隱藏) [ <strong>無色彩</strong> ] 按鈕。 <br/> 對所有 <em>ColorTemplate</em> 值都有效。<br/> 限制為下列其中一個值 (0 和1不是有效的) ：<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>RecentColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>否<br/></td>
<td>[ <strong>最近使用的色彩</strong> ] 區域中的色晶片 (或樣本) 資料列數目。 <br/> 只有在 <code>ThemeColors</code> 為 <em>ColorTemplate</em> 屬性指定時才有效。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) <br/> </dt> <dd> 介於1和256之間的任何正整數值（含）。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>StandardColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>否<br/></td>
<td><strong>標準色彩</strong>區域中的色晶片 (或樣本) 資料列數目。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) <br/> </dt> <dd> 介於1和256之間的任何正整數值（含）。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ThemeColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>否<br/></td>
<td><strong>主題色彩</strong>區域中的色晶片 (或樣本) 資料列數目。<br/> 只有在 <code>ThemeColors</code> 為 <em>ColorTemplate</em> 屬性指定時才有效。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) <br/> </dt> <dd> 介於1和256之間的任何正整數值（含）。<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>         |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Group**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>備註

選擇性。

可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。

## <a name="examples"></a>範例

下列範例示範所有三種類型的 [下拉式色彩選擇器](windowsribbon-controls-dropdowncolorpicker.md)的基本標記。

這段程式碼會顯示三個 **DropDownColorPicker** 元素的命令宣告。


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



這段程式碼會顯示三種類型的 **DropDownColorPicker** 控制項宣告。


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a>項目資訊

* **最低支援系統**： Windows 7
* **可以是空** 的：是



## <a name="see-also"></a>另請參閱

<dl> <dt>

[下拉式色彩選擇器控制項](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[DropDownColorPicker 範例](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





