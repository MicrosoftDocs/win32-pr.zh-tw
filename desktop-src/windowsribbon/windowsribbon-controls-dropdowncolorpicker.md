---
title: Drop-Down 色彩選擇器
description: Windows 功能區架構提供特製化的 Drop-Down 色彩選擇器控制項，可透過分割按鈕和可自訂的下拉式色彩選取器來公開各種色彩設定。
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8104ba92d0be9d56607083508d7f30728a7f3a141839d74314561d392fb942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707656"
---
# <a name="drop-down-color-picker"></a>Drop-Down 色彩選擇器

Windows 功能區架構提供特製化的 Drop-Down 色彩選擇器控制項，可透過分割按鈕和可自訂的下拉式色彩選取器來公開各種色彩設定。

-   [簡介](#introduction)
-   [標記](#markup)
-   [程式碼](#code)
    -   [屬性](#properties)
    -   [命令處理常式](#command-handlers)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

藉由模擬 Microsoft Office 色彩選擇器的外觀和功能，功能區架構可讓您在各種應用程式之間獲益，並參與一致性和熟悉。

## <a name="markup"></a>標記

就像所有功能區控制項一樣，Drop-Down 色彩選擇器可以透過標記輕鬆地執行和自訂。 架構會為 Drop-Down 色彩選擇器提供數個元素屬性，以公開各種層級的功能。 下表列出 Drop-Down 色彩選擇器屬性。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ColorTemplate</td>
<td>指定 Drop-Down 色彩選擇器類型的版面配置範本。<br/> 有三個範本，每個範本都會為相關聯的屬性和屬性索引鍵指定控制項配置和預設值。 <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td>ChipSize</td>
<td>每個色晶片 (或樣本) 的大小。<br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td>資料行</td>
<td>色板 (或樣本) 資料行的數目。<br/></td>
</tr>
<tr class="even">
<td>CommandName</td>
<td>相關命令宣告的名稱。 <br/></td>
</tr>
<tr class="odd">
<td>IsAutomaticColorButtonVisible</td>
<td>顯示 (或隱藏) [ <strong>自動</strong> ] 按鈕。<br/> 只有當 <em>ColorTemplate</em> 的值為或時，才有效 <code>ThemeColors</code> <code>StandardColors</code> 。<br/></td>
</tr>
<tr class="even">
<td>IsNoColorButtonVisible</td>
<td>顯示 (或隱藏) [ <strong>無色彩</strong> ] 按鈕。<br/> 對所有 <em>ColorTemplate</em> 值都有效。<br/></td>
</tr>
<tr class="odd">
<td>RecentColorGridRows</td>
<td>[ <strong>最近使用的色彩</strong> ] 區域中的色晶片 (或樣本) 資料列數目。<br/> 只有當 <em>ColorTemplate</em> 的值是時才有效 <code>ThemeColors</code> 。<br/></td>
</tr>
<tr class="even">
<td>StandardColorGridRows</td>
<td><strong>標準色彩</strong>區域中的色晶片 (或樣本) 資料列數目。<br/></td>
</tr>
<tr class="odd">
<td>ThemeColorGridRows</td>
<td><strong>主題色彩</strong>區域中的色晶片 (或樣本) 資料列數目。<br/> 只有當 <em>ColorTemplate</em> 的值是時才有效 <code>ThemeColors</code> 。<br/></td>
</tr>
</tbody>
</table>



 

下列螢幕擷取畫面說明三個色彩範本的預設 Drop-Down 色彩選擇器版面配置。



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`： \[ \] ![ colortemplate 屬性設定為 ' themecolors ' 的 dropdowncolorpicker 元素的行出螢幕擷取畫面。 ](images/markup/colortemplate.themedcolors.1.png) \[除\] | `standardcolors`： \[ \] ![ colortemplate 屬性設定為 ' standardcolors ' 的 dropdowncolorpicker 元素的行出螢幕擷取畫面。 ](images/markup/colortemplate.standardcolors.3.png) \[除\] | `highlightcolors`： \[ \] ![ colortemplate 屬性設定為 ' highlightcolors ' 的 dropdowncolorpicker 元素的行出螢幕擷取畫面。](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

下列範例示範每個 Drop-Down 色彩選擇器類型所需的基本標記：

> [!Note]  
> Drop-Down 色彩選擇器是 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)範本中有效的 [按鈕](windowsribbon-controls-button.md)控制項。

 


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


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a>程式碼

作為支援自訂的特殊控制項，任何利用這些功能的 Drop-Down 色彩選擇器實作此實作都需要特殊的應用程式程式碼，才能管理屬性及處理控制項發出的任何命令。

### <a name="properties"></a>屬性

功能區架構會針對 Drop-Down 色彩選擇器控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

一般來說，在功能區 UI 中會更新 Drop-Down 色彩選擇器屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與 Drop-Down 色彩選擇器控制項相關聯的屬性索引鍵。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性索引鍵</th>
<th>描述</th>
<th>附註</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></td>
<td>定義 <strong>自動</strong> 色彩按鈕的標籤。<br/> 只有當 <em>ColorTemplate</em> 的值為或時，才有效 <code>ThemeColors</code> <code>StandardColors</code> 。<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></td>
<td>將選取的色彩值定義為 <a href="/windows/win32/gdi/colorref">COLORREF</a>。<br/> 只有在 <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> 的值為時才有效 <code>UI_SWATCHCOLORTYPE_RGB</code> 。<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></td>
<td>定義選取的色彩類型。<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>定義控制項回應使用者互動的能力。<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>

<td>只能透過失效進行更新。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>定義控制項標籤的字元字串。<br/></td>
<td>只能透過失效進行更新。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>定義要為控制項顯示的大型高對比影像。<br/></td>
<td>只能透過失效進行更新。<br/> 如需影像格式的詳細資訊，請參閱 <a href="windowsribbon-imageformats.md">指定功能區影像資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>定義要為控制項顯示的大型影像。<br/></td>
<td>只能透過失效進行更新。<br/> 如需影像格式的詳細資訊，請參閱 <a href="windowsribbon-imageformats.md">指定功能區影像資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></td>
<td>定義 [ <strong>其他色彩</strong> ] 的標籤 ... 按鈕。<br/> 只有當 <em>ColorTemplate</em> 的值為或時，才有效 <code>ThemeColors</code> <code>StandardColors</code> 。<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></td>
<td>定義 [ <strong>無色彩</strong> ] 按鈕的標籤。<br/> 對所有 <em>ColorTemplate</em> 值都有效。<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></td>
<td>定義 [ <strong>最近使用的色彩</strong> ] 分類的標籤。<br/> 只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。 這是唯一包含標記類別的範本。<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>定義要為控制項顯示的小型高對比影像。<br/></td>
<td>只能透過失效進行更新。<br/> 如需影像格式的詳細資訊，請參閱 <a href="windowsribbon-imageformats.md">指定功能區影像資源</a>。<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>定義要為控制項顯示的小型影像。<br/></td>
<td>只能透過失效進行更新。<br/> 如需影像格式的詳細資訊，請參閱 <a href="windowsribbon-imageformats.md">指定功能區影像資源</a>。<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></td>
<td>針對 Drop-Down 色彩選擇器的樣本，定義 <a href="/windows/win32/gdi/colorref">COLORREF</a> 值的陣列。<br/> 每個 Drop-Down 色彩選擇器 <em>ColorTemplate</em> 都包含一個 <code>StandardColors</code> 方格。 <br/>
<blockquote>
[!Note]<br />
陣列的初始<em>StandardColorGridRows</em> x 資料<em>行</em>中的<a href="/windows/win32/gdi/colorref">COLORREF</a>值隨即顯示。 如果陣列定義的色彩比標記中宣告的 <code>StandardColors</code> 樣本數目少，則會顯示遺漏晶片的空白空間。
</blockquote>
<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></td>
<td>定義 <strong>標準色彩</strong> 分類的標籤。<br/> 只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。 這是唯一包含標記類別的範本。<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></td>
<td>為方格定義色彩樣本工具提示的字串陣列 <code>StandardColors</code> 。<br/> 每個 Drop-Down 色彩選擇器 <em>ColorTemplate</em> 都包含一個 <code>StandardColors</code> 方格。 <br/>
<blockquote>
[!Note]<br />
只會使用標示方格中所顯示之色彩色板的工具提示 <code>StandardColors</code> 。 如果提供的標籤數目少於方格中的樣本數目 <code>StandardColors</code> ，就會提供 remainining 樣本的預設值。
</blockquote>
<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></td>
<td>針對 Drop-Down 色彩選擇器的樣本，定義 <a href="/windows/win32/gdi/colorref">COLORREF</a> 值的陣列。<br/> 只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。 <br/>
<blockquote>
[!Note]<br />
陣列的初始<em>ThemeColorGridRows</em> x 資料<em>行</em>中的<a href="/windows/win32/gdi/colorref">COLORREF</a>值隨即顯示。 如果陣列定義的色彩比標記中宣告的 <code>ThemeColors</code> 樣本數目少，則會顯示遺漏晶片的空白空間。
</blockquote>
<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></td>
<td>為方格定義色彩樣本工具提示的字串陣列 <code>ThemeColors</code> 。<br/> 只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。 <br/>
<blockquote>
[!Note]<br />
只會使用標示方格中所顯示之色彩色板的工具提示 <code>ThemeColors</code> 。 如果提供的標籤數目少於方格中的樣本數目 <code>ThemeColors</code> ，就會提供 remainining 樣本的預設值。
</blockquote>
<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></td>
<td>定義 <strong>主題色彩</strong> 分類的標籤。<br/> 只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。 這是唯一包含標記類別的範本。<br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>為與 <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>相關聯的工具提示描述定義字元字串。<br/></td>
<td>只能透過失效進行更新。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>定義命令工具提示的字元字串。<br/></td>
<td>只能透過失效進行更新。</td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a>命令處理常式

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)方法是用來透過上方所列的屬性索引鍵來自訂 Drop-Down 色彩選擇器。 下列範例示範如何根據自訂樣式喜好設定或在標記中宣告的自訂樣本方格，設定 Drop-Down 色彩選擇器的色彩樣本。


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



下列範例示範 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 方法的執行，此方法會向功能區應用程式公開 Drop-Down 色彩選擇器色板色彩。


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**DropDownColorPicker 標記元素**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[色彩選擇器屬性](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[透過大小定義和調整原則自訂功能區](windowsribbon-templates.md)
</dt> <dt>

[DropDownColorPicker 範例](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

