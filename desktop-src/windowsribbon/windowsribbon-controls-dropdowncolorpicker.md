---
title: Drop-Down 色彩選擇器
description: Windows 功能區架構提供特製化的 Drop-Down 色彩選擇器控制項，可透過分割按鈕和可自訂的下拉式色彩選取器來公開各種色彩設定。
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366cc7eadaca23271d5b2afa43ec66235839694a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443659"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="fa1c6-103">Drop-Down 色彩選擇器</span><span class="sxs-lookup"><span data-stu-id="fa1c6-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="fa1c6-104">Windows 功能區架構提供特製化的 Drop-Down 色彩選擇器控制項，可透過分割按鈕和可自訂的下拉式色彩選取器來公開各種色彩設定。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="fa1c6-105">簡介</span><span class="sxs-lookup"><span data-stu-id="fa1c6-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="fa1c6-106">標記</span><span class="sxs-lookup"><span data-stu-id="fa1c6-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="fa1c6-107">程式碼</span><span class="sxs-lookup"><span data-stu-id="fa1c6-107">Code</span></span>](#code)
    -   [<span data-ttu-id="fa1c6-108">屬性</span><span class="sxs-lookup"><span data-stu-id="fa1c6-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="fa1c6-109">命令處理常式</span><span class="sxs-lookup"><span data-stu-id="fa1c6-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="fa1c6-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa1c6-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="fa1c6-111">簡介</span><span class="sxs-lookup"><span data-stu-id="fa1c6-111">Introduction</span></span>

<span data-ttu-id="fa1c6-112">藉由模擬 Microsoft Office 色彩選擇器的外觀和功能，功能區架構可讓您在各種應用程式之間獲益，並參與一致性和熟悉。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="fa1c6-113">標記</span><span class="sxs-lookup"><span data-stu-id="fa1c6-113">Markup</span></span>

<span data-ttu-id="fa1c6-114">就像所有功能區控制項一樣，Drop-Down 色彩選擇器可以透過標記輕鬆地執行和自訂。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="fa1c6-115">架構會為 Drop-Down 色彩選擇器提供數個元素屬性，以公開各種層級的功能。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="fa1c6-116">下表列出 Drop-Down 色彩選擇器屬性。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa1c6-117">屬性</span><span class="sxs-lookup"><span data-stu-id="fa1c6-117">Attribute</span></span></th>
<th><span data-ttu-id="fa1c6-118">描述</span><span class="sxs-lookup"><span data-stu-id="fa1c6-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa1c6-119">ColorTemplate</span><span class="sxs-lookup"><span data-stu-id="fa1c6-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="fa1c6-120">指定 Drop-Down 色彩選擇器類型的版面配置範本。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="fa1c6-121">有三個範本，每個範本都會為相關聯的屬性和屬性索引鍵指定控制項配置和預設值。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-122">ChipSize</span><span class="sxs-lookup"><span data-stu-id="fa1c6-122">ChipSize</span></span></td>
<td><span data-ttu-id="fa1c6-123">每個色晶片 (或樣本) 的大小。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-124">資料行</span><span class="sxs-lookup"><span data-stu-id="fa1c6-124">Columns</span></span></td>
<td><span data-ttu-id="fa1c6-125">色板 (或樣本) 資料行的數目。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="fa1c6-126">CommandName</span></span></td>
<td><span data-ttu-id="fa1c6-127">相關命令宣告的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-128">IsAutomaticColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="fa1c6-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="fa1c6-129">顯示 (或隱藏) [ <strong>自動</strong> ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="fa1c6-130">只有當 <em>ColorTemplate</em> 的值為或時，才有效 <code>ThemeColors</code> <code>StandardColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-131">IsNoColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="fa1c6-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="fa1c6-132">顯示 (或隱藏) [ <strong>無色彩</strong> ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="fa1c6-133">對所有 <em>ColorTemplate</em> 值都有效。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-134">RecentColorGridRows</span><span class="sxs-lookup"><span data-stu-id="fa1c6-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="fa1c6-135">[ <strong>最近使用的色彩</strong> ] 區域中的色晶片 (或樣本) 資料列數目。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="fa1c6-136">只有當 <em>ColorTemplate</em> 的值是時才有效 <code>ThemeColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-137">StandardColorGridRows</span><span class="sxs-lookup"><span data-stu-id="fa1c6-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="fa1c6-138"><strong>標準色彩</strong>區域中的色晶片 (或樣本) 資料列數目。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-139">ThemeColorGridRows</span><span class="sxs-lookup"><span data-stu-id="fa1c6-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="fa1c6-140"><strong>主題色彩</strong>區域中的色晶片 (或樣本) 資料列數目。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="fa1c6-141">只有當 <em>ColorTemplate</em> 的值是時才有效 <code>ThemeColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fa1c6-142">下列螢幕擷取畫面說明三個色彩範本的預設 Drop-Down 色彩選擇器版面配置。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa1c6-143">`ThemeColors`： \[ \] ![ colortemplate 屬性設定為 ' themecolors ' 的 dropdowncolorpicker 元素的行出螢幕擷取畫面。 ](images/markup/colortemplate.themedcolors.1.png) \[除\]</span><span class="sxs-lookup"><span data-stu-id="fa1c6-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="fa1c6-144">`standardcolors`： \[ \] ![ colortemplate 屬性設定為 ' standardcolors ' 的 dropdowncolorpicker 元素的行出螢幕擷取畫面。 ](images/markup/colortemplate.standardcolors.3.png) \[除\]</span><span class="sxs-lookup"><span data-stu-id="fa1c6-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="fa1c6-145">`highlightcolors`： \[ \] ![ colortemplate 屬性設定為 ' highlightcolors ' 的 dropdowncolorpicker 元素的行出螢幕擷取畫面。](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="fa1c6-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="fa1c6-146">下列範例示範每個 Drop-Down 色彩選擇器類型所需的基本標記：</span><span class="sxs-lookup"><span data-stu-id="fa1c6-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="fa1c6-147">Drop-Down 色彩選擇器是 [**SizeDefinition**](windowsribbon-element-sizedefinition.md)範本中有效的 [按鈕](windowsribbon-controls-button.md)控制項。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


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





## <a name="code"></a><span data-ttu-id="fa1c6-148">程式碼</span><span class="sxs-lookup"><span data-stu-id="fa1c6-148">Code</span></span>

<span data-ttu-id="fa1c6-149">作為支援自訂的特殊控制項，任何利用這些功能的 Drop-Down 色彩選擇器實作此實作都需要特殊的應用程式程式碼，才能管理屬性及處理控制項發出的任何命令。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="fa1c6-150">屬性</span><span class="sxs-lookup"><span data-stu-id="fa1c6-150">Properties</span></span>

<span data-ttu-id="fa1c6-151">功能區架構會針對 Drop-Down 色彩選擇器控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="fa1c6-152">一般來說，在功能區 UI 中會更新 Drop-Down 色彩選擇器屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="fa1c6-153">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="fa1c6-154">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="fa1c6-155">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="fa1c6-156">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="fa1c6-157">下表列出與 Drop-Down 色彩選擇器控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa1c6-158">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="fa1c6-158">Property Key</span></span></th>
<th><span data-ttu-id="fa1c6-159">描述</span><span class="sxs-lookup"><span data-stu-id="fa1c6-159">Description</span></span></th>
<th><span data-ttu-id="fa1c6-160">注意</span><span class="sxs-lookup"><span data-stu-id="fa1c6-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa1c6-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="fa1c6-162">定義 <strong>自動</strong> 色彩按鈕的標籤。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="fa1c6-163">只有當 <em>ColorTemplate</em> 的值為或時，才有效 <code>ThemeColors</code> <code>StandardColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-164">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="fa1c6-166">將選取的色彩值定義為 <a href="/windows/win32/gdi/colorref">COLORREF</a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="fa1c6-167">只有在 <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> 的值為時才有效 <code>UI_SWATCHCOLORTYPE_RGB</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-168">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="fa1c6-170">定義選取的色彩類型。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-171">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="fa1c6-173">定義控制項回應使用者互動的能力。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-174">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="fa1c6-176">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="fa1c6-178">定義控制項標籤的字元字串。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-179">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="fa1c6-181">定義要為控制項顯示的大型高對比影像。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-182">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="fa1c6-183">如需影像格式的詳細資訊，請參閱 <a href="windowsribbon-imageformats.md">指定功能區影像資源</a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="fa1c6-185">定義要為控制項顯示的大型影像。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-186">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="fa1c6-187">如需影像格式的詳細資訊，請參閱 <a href="windowsribbon-imageformats.md">指定功能區影像資源</a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="fa1c6-189">定義 [ <strong>其他色彩</strong> ] 的標籤 ... 按鈕。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="fa1c6-190">只有當 <em>ColorTemplate</em> 的值為或時，才有效 <code>ThemeColors</code> <code>StandardColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-191">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="fa1c6-193">定義 [ <strong>無色彩</strong> ] 按鈕的標籤。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="fa1c6-194">對所有 <em>ColorTemplate</em> 值都有效。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-195">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="fa1c6-197">定義 [ <strong>最近使用的色彩</strong> ] 分類的標籤。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="fa1c6-198">只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="fa1c6-199">這是唯一包含標記類別的範本。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-200">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="fa1c6-202">定義要為控制項顯示的小型高對比影像。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-203">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="fa1c6-204">如需影像格式的詳細資訊，請參閱 <a href="windowsribbon-imageformats.md">指定功能區影像資源</a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="fa1c6-206">定義要為控制項顯示的小型影像。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-207">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="fa1c6-208">如需影像格式的詳細資訊，請參閱 <a href="windowsribbon-imageformats.md">指定功能區影像資源</a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="fa1c6-210">針對 Drop-Down 色彩選擇器的樣本，定義 <a href="/windows/win32/gdi/colorref">COLORREF</a> 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="fa1c6-211">每個 Drop-Down 色彩選擇器 <em>ColorTemplate</em> 都包含一個 <code>StandardColors</code> 方格。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fa1c6-212">陣列的初始<em>StandardColorGridRows</em> x 資料<em>行</em>中的<a href="/windows/win32/gdi/colorref">COLORREF</a>值隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="fa1c6-213">如果陣列定義的色彩比標記中宣告的 <code>StandardColors</code> 樣本數目少，則會顯示遺漏晶片的空白空間。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="fa1c6-214">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="fa1c6-216">定義 <strong>標準色彩</strong> 分類的標籤。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="fa1c6-217">只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="fa1c6-218">這是唯一包含標記類別的範本。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-219">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="fa1c6-221">為方格定義色彩樣本工具提示的字串陣列 <code>StandardColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="fa1c6-222">每個 Drop-Down 色彩選擇器 <em>ColorTemplate</em> 都包含一個 <code>StandardColors</code> 方格。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fa1c6-223">只會使用標示方格中所顯示之色彩色板的工具提示 <code>StandardColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="fa1c6-224">如果提供的標籤數目少於方格中的樣本數目 <code>StandardColors</code> ，就會提供 remainining 樣本的預設值。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="fa1c6-225">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="fa1c6-227">針對 Drop-Down 色彩選擇器的樣本，定義 <a href="/windows/win32/gdi/colorref">COLORREF</a> 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="fa1c6-228">只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fa1c6-229">陣列的初始<em>ThemeColorGridRows</em> x 資料<em>行</em>中的<a href="/windows/win32/gdi/colorref">COLORREF</a>值隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="fa1c6-230">如果陣列定義的色彩比標記中宣告的 <code>ThemeColors</code> 樣本數目少，則會顯示遺漏晶片的空白空間。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="fa1c6-231">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="fa1c6-233">為方格定義色彩樣本工具提示的字串陣列 <code>ThemeColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="fa1c6-234">只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fa1c6-235">只會使用標示方格中所顯示之色彩色板的工具提示 <code>ThemeColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="fa1c6-236">如果提供的標籤數目少於方格中的樣本數目 <code>ThemeColors</code> ，就會提供 remainining 樣本的預設值。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="fa1c6-237">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="fa1c6-239">定義 <strong>主題色彩</strong> 分類的標籤。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="fa1c6-240">只有當 <em>ColorTemplate</em> 的值為時才有效 <code>ThemeColors</code> 。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="fa1c6-241">這是唯一包含標記類別的範本。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-242">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa1c6-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="fa1c6-244">為與 <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>相關聯的工具提示描述定義字元字串。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-245">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa1c6-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="fa1c6-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="fa1c6-247">定義命令工具提示的字元字串。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="fa1c6-248">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="fa1c6-249">命令處理常式</span><span class="sxs-lookup"><span data-stu-id="fa1c6-249">Command handlers</span></span>

<span data-ttu-id="fa1c6-250">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)方法是用來透過上方所列的屬性索引鍵來自訂 Drop-Down 色彩選擇器。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="fa1c6-251">下列範例示範如何根據自訂樣式喜好設定或在標記中宣告的自訂樣本方格，設定 Drop-Down 色彩選擇器的色彩樣本。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


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



<span data-ttu-id="fa1c6-252">下列範例示範 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 方法的執行，此方法會向功能區應用程式公開 Drop-Down 色彩選擇器色板色彩。</span><span class="sxs-lookup"><span data-stu-id="fa1c6-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fa1c6-253">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa1c6-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa1c6-254">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="fa1c6-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="fa1c6-255">**DropDownColorPicker 標記元素**</span><span class="sxs-lookup"><span data-stu-id="fa1c6-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="fa1c6-256">色彩選擇器屬性</span><span class="sxs-lookup"><span data-stu-id="fa1c6-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="fa1c6-257">透過大小定義和調整原則自訂功能區</span><span class="sxs-lookup"><span data-stu-id="fa1c6-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="fa1c6-258">DropDownColorPicker 範例</span><span class="sxs-lookup"><span data-stu-id="fa1c6-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

