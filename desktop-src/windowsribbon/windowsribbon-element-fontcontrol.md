---
title: FontControl 元素
description: 表示字型控制項，這是專供字型操作之個別控制項的特殊容器。
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- FontControl 元素視窗功能區
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa080b58e3a9d53fa044e7dbbb6598d5b7be7c49
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2020
ms.locfileid: "104374913"
---
# <a name="fontcontrol-element"></a>FontControl 元素

表示 [字型控制項](windowsribbon-controls-fontcontrol.md)，這是專供字型操作之個別控制項的特殊容器。

## <a name="usage"></a>使用方式

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
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
<td>No<br/></td>
<td>將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) <br/> </dt> <dd> 字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。 <br/> 值在功能區 XML 檔中必須是唯一的。 <br/> 最大長度：100個字元。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>FontType</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>限制為下列其中一個值： <br/> <br/>
<dt><span></span><span></span><strong></strong> (FontOnly) <br/> </dt> <dd> 預設值。 <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> 將 <em>FontType</em> 屬性設定為可 <code>FontOnly</code> 啟用下列功能：<br/>
<ul>
<li>[<strong>字型家族</strong>] 下拉式方塊。</li>
<li><strong>字型大小</strong> 下拉式方塊。</li>
<li><p><strong>粗體</strong>、 <strong>斜體</strong>、 <strong>底線</strong>和 <strong>刪除線</strong> 切換按鈕。</p>
<blockquote>
[!Note]<br />
預設會顯示 <strong>刪除線</strong> 和 <strong>底線切換按鈕，但</strong> 可以藉由將 <em>IsStrikethroughButtonVisible</em> 和 <em>IsUnderlineButtonVisible</em> 屬性設定為來隱藏 <code>false</code> 。
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (FontWithColor) <br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> 將 <em>FontType</em> 屬性設定為可 <code>FontWithColor</code> 啟用下列功能：<br/>
<ul>
<li>[<strong>字型家族</strong>] 下拉式方塊。</li>
<li><strong>字型大小</strong> 下拉式方塊。</li>
<li><strong>放大字型</strong> 和 <strong>壓縮字型</strong> 大小的遞增和遞減按鈕。</li>
<li><p><strong>粗體</strong>、 <strong>斜體</strong>、 <strong>底線</strong>和 <strong>刪除線</strong> 切換按鈕。</p>
<blockquote>
[!Note]<br />
預設會顯示 <strong>刪除線</strong> 和 <strong>底線切換按鈕，但</strong> 可以藉由將 <em>IsStrikethroughButtonVisible</em> 和 <em>IsUnderlineButtonVisible</em> 屬性設定為來隱藏 <code>false</code> 。
</blockquote>
<p><br/></p></li>
<li><strong>文字色彩</strong> 色彩選擇器。</li>
<li><p><strong>文字反白顯示色彩</strong> 色彩選擇器。</p>
<blockquote>
[!Note]<br />
預設會隱藏此控制項，但可以藉由將 <em>IsHighlightButtonVisible</em> 屬性設定為來顯示 <code>true</code> 。
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (RichFont) <br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> 將 <em>FontType</em> 屬性設定為可 <code>RichFont</code> 啟用下列功能：<br/>
<ul>
<li>[<strong>字型家族</strong>] 下拉式方塊。</li>
<li><strong>字型大小</strong> 下拉式方塊。</li>
<li><strong>放大字型</strong> 和 <strong>壓縮字型</strong> 大小的遞增和遞減按鈕。</li>
<li><p><strong>粗體</strong>、 <strong>斜體</strong>、 <strong>底線</strong>和 <strong>刪除線</strong> 切換按鈕。</p>
<blockquote>
[!Note]<br />
預設會顯示 <strong>刪除線</strong> 和 <strong>底線切換按鈕，而且</strong> 無法藉由將 <em>IsStrikethroughButtonVisible</em> 和 <em>IsUnderlineButtonVisible</em> 屬性設定為來隱藏 <code>false</code> 。
</blockquote>
<p><br/></p></li>
<li><strong>文字色彩</strong> 色彩選擇器。</li>
<li><p><strong>文字反白顯示色彩</strong> 色彩選擇器。</p>
<blockquote>
[!Note]<br />
預設會顯示此控制項，將 <em>IsHighlightButtonVisible</em> 屬性設定為，就無法隱藏這個控制項 <code>false</code> 。
</blockquote>
<p><br/></p></li>
<li>注<strong>標</strong>和<strong>上標</strong>切換按鈕。</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsGrowShrinkButtonGroupVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td><strong>Windows 8 和更新版本</strong><br/> 限制為下列其中一個值： <br/>
<blockquote>
[!Note]<br />
[成長/縮小] 按鈕永遠不會顯示在 <a href="windowsribbon-element-minitoolbar.md"><strong>浮動工具列</strong></a>中。
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> <em>FontType</em>的值等於或時的預設值 <code>FontWithColor</code> <code>RichFont</code> 。<br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd> <em>FontType</em>的值等於時的預設值 <code>FontOnly</code> 。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsHighlightButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>限制為下列其中一個值 (0 和1不是有效的) ： <br/>
<blockquote>
[!Note]<br />
只有當<em>FontType</em>屬性的值等於或時，才可以從<strong>FontControl</strong>中使用色彩反白顯示 <code>FontWithColor</code> <code>RichFont</code> 。
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> <em>FontType</em>的值等於或時的預設值 <code>FontWithColor</code> <code>RichFont</code> 。<br/> 只有當 <em>FontType</em> 的值等於或時才會有效 <code>FontWithColor</code> <code>RichFont</code> 。<br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd> <em>FontType</em>的值等於時的預設值 <code>FontOnly</code> 。<br/> 只有當 <em>FontType</em> 的值等於或時才會有效 <code>FontOnly</code> <code>FontWithColor</code> 。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsStrikethroughButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>限制為下列其中一個值 (0 和1不是有效的) ： <br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 預設值。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd> 只有當 <em>FontType</em> 的值等於或時才會有效 <code>FontOnly</code> <code>FontWithColor</code> 。 <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsUnderlineButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>限制為下列其中一個值 (0 和1不是有效的) ： <br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 預設值。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd> 只有當 <em>FontType</em> 的值等於或時才會有效 <code>FontOnly</code> <code>FontWithColor</code> 。 <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaximumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>要顯示的最大點大小。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) <br/> </dt> <dd> 介於1到9999（含）之間的整數值。<br/> 預設值為 <strong>9999</strong>。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinimumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>要顯示的最小點大小。<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) <br/> </dt> <dd> 介於1到9999（含）之間的整數值。<br/> 預設值為 <strong>1</strong>。<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ShowTrueTypeOnly</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>限制為下列其中一個值 (0 和1不是有效的) ：<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 只顯示 TrueType 和 OpenType 字型。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd> 預設值。 所顯示的字型類型沒有任何限制。<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ShowVerticalFonts</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>限制為下列其中一個值 (0 和1不是有效的) ：<br/>
<blockquote>
[!Note]<br />
在 <strong>字型系列</strong> 清單中，垂直字型前面會加上 @ 符號。
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true) <br/> </dt> <dd> 預設值。 顯示設定為<strong>在 [字型</strong>] 控制台中<strong>顯示</strong>的垂直字型。 <br/> </dd> <dt><span></span><span></span><strong></strong> (false) <br/> </dt> <dd> 允許不支援垂直文字的應用程式隱藏所有設定為 <strong>顯示</strong> 在 <strong>字型 [控制台] 中的垂直</strong> 字型。<br/>
<blockquote>
[!Note]<br />
在 Windows Vista 中， <strong>[字型</strong> ] 控制台不提供 <strong>顯示</strong> 或 <strong>隱藏</strong> 功能。 在此情況下， <em>ShowVerticalFonts</em> 屬性必須設定為 <code>False</code> 。
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                                                               |
|-----------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/> |
| [**Group**](windowsribbon-element-group.md)<br/>               |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a>備註

選擇性。

每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**Group**](windowsribbon-element-group.md)或 [**MenuGroup**](windowsribbon-element-menugroup.md) 元素最多可能會發生一次。

標記中宣告的任何 **FontControl** 命令屬性（例如 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 或 [**TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)）都會由組成 **FontControl** 之個別控制項的屬性覆寫。

如果沒有與控制項相關聯的命令處理常式，嘗試從 [字型控制項](windowsribbon-controls-fontcontrol.md) 的色彩選擇器選取色彩樣本，可能會造成存取違規。

## <a name="examples"></a>範例

下列範例示範三種 [字型控制項](windowsribbon-controls-fontcontrol.md)類型的基本標記。

這段程式碼會顯示 **FontControl** 命令宣告，每個宣告都有 [**群組**](windowsribbon-element-group.md) 容器宣告。


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



這段程式碼會顯示 **FontControl** 控制項宣告，其中每個 **FontControl** 和 [**群組**](windowsribbon-element-group.md) 都在單一索引標籤中宣告。


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a>項目資訊



|                                     |           |
|-------------------------------------|-----------|
| 最低支援系統<br/> | Windows 7 |
| 可以是空的                        | Yes       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[字型控制項控制項](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[字型控制項屬性](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[FontControl 範例](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





