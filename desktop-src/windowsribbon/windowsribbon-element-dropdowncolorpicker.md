---
title: DropDownColorPicker 元素
description: 表示按一下以顯示色板的 Drop-Down 色彩 Pickercontrol。
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- DropDownColorPicker 元素視窗功能區
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442899"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="07549-104">DropDownColorPicker 元素</span><span class="sxs-lookup"><span data-stu-id="07549-104">DropDownColorPicker element</span></span>

<span data-ttu-id="07549-105">表示當按一下以顯示色板時的 [下拉式色彩選擇器](windowsribbon-controls-dropdowncolorpicker.md)控制項。</span><span class="sxs-lookup"><span data-stu-id="07549-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="07549-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="07549-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="07549-107">屬性</span><span class="sxs-lookup"><span data-stu-id="07549-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07549-108">屬性</span><span class="sxs-lookup"><span data-stu-id="07549-108">Attribute</span></span></th>
<th><span data-ttu-id="07549-109">類型</span><span class="sxs-lookup"><span data-stu-id="07549-109">Type</span></span></th>
<th><span data-ttu-id="07549-110">必要</span><span class="sxs-lookup"><span data-stu-id="07549-110">Required</span></span></th>
<th><span data-ttu-id="07549-111">描述</span><span class="sxs-lookup"><span data-stu-id="07549-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07549-112"><strong>ChipSize</strong></span><span class="sxs-lookup"><span data-stu-id="07549-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="07549-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="07549-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="07549-114">否</span><span class="sxs-lookup"><span data-stu-id="07549-114">No</span></span><br/></td>
<td><span data-ttu-id="07549-115">每個色晶片或樣本的大小。</span><span class="sxs-lookup"><span data-stu-id="07549-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="07549-116">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="07549-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="07549-117">
<dt><span></span><span></span><strong></strong> (Small) </span><span class="sxs-lookup"><span data-stu-id="07549-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="07549-118">每個色晶片都是11x11 圖元正方形。</span><span class="sxs-lookup"><span data-stu-id="07549-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="07549-119"><dt><span></span><span></span><strong></strong> (中) </span><span class="sxs-lookup"><span data-stu-id="07549-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="07549-120">每個色晶片都是16x16 圖元正方形。</span><span class="sxs-lookup"><span data-stu-id="07549-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="07549-121"><dt><span></span><span></span><strong></strong> (大型) </span><span class="sxs-lookup"><span data-stu-id="07549-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="07549-122">每個色晶片都是24x24 圖元正方形。</span><span class="sxs-lookup"><span data-stu-id="07549-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07549-123"><strong>ColorTemplate</strong></span><span class="sxs-lookup"><span data-stu-id="07549-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="07549-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="07549-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="07549-125">否</span><span class="sxs-lookup"><span data-stu-id="07549-125">No</span></span><br/></td>
<td><span data-ttu-id="07549-126">指定 <a href="windowsribbon-controls-dropdowncolorpicker.md">下拉式色彩選擇器</a>類型的版面配置範本。</span><span class="sxs-lookup"><span data-stu-id="07549-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="07549-127">限制為下列其中一個值 (如果未宣告與 <em>ColorTemplate</em> 相關的選擇性屬性，則會顯示) 的預設視圖：</span><span class="sxs-lookup"><span data-stu-id="07549-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="07549-128">
<dt><span></span><span></span><strong></strong> (ThemeColors) </span><span class="sxs-lookup"><span data-stu-id="07549-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="07549-129">預設值。</span><span class="sxs-lookup"><span data-stu-id="07549-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="07549-130">將 <em>ColorTemplate</em> 屬性設定為可 <code>ThemeColors</code> 啟用下列功能：</span><span class="sxs-lookup"><span data-stu-id="07549-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="07549-131">SplitButton 錨點。</span><span class="sxs-lookup"><span data-stu-id="07549-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="07549-132">預設會顯示 [<strong>自動</strong>色彩] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="07549-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="07549-133">Windows <strong>主題色彩</strong> 色板方格。</span><span class="sxs-lookup"><span data-stu-id="07549-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="07549-134"><strong>標準色彩</strong> 樣本方格。</span><span class="sxs-lookup"><span data-stu-id="07549-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="07549-135">[<strong>最近使用的色彩</strong>] 樣本方格是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="07549-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="07549-136">[<strong>其他色彩</strong>] 對話方塊啟動器。</span><span class="sxs-lookup"><span data-stu-id="07549-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="07549-137">預設不會顯示<strong>色彩</strong>色彩按鈕。</span><span class="sxs-lookup"><span data-stu-id="07549-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="07549-138"><dt><span></span><span></span><strong></strong> (StandardColors) </span><span class="sxs-lookup"><span data-stu-id="07549-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="07549-139">將 <em>ColorTemplate</em> 屬性設定為可 <code>StandardColors</code> 啟用下列功能：</span><span class="sxs-lookup"><span data-stu-id="07549-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="07549-140">SplitButton 錨點。</span><span class="sxs-lookup"><span data-stu-id="07549-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="07549-141">預設會顯示 [<strong>自動</strong>色彩] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="07549-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="07549-142"><strong>標準色彩</strong> 樣本方格。</span><span class="sxs-lookup"><span data-stu-id="07549-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="07549-143">[<strong>其他色彩</strong>] 對話方塊啟動器。</span><span class="sxs-lookup"><span data-stu-id="07549-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="07549-144">預設不會顯示<strong>色彩</strong>色彩按鈕。</span><span class="sxs-lookup"><span data-stu-id="07549-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="07549-145"><dt><span></span><span></span><strong></strong> (HighlightColors) </span><span class="sxs-lookup"><span data-stu-id="07549-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="07549-146">將 <em>ColorTemplate</em> 屬性設定為可 <code>HighlightColors</code> 啟用下列功能：</span><span class="sxs-lookup"><span data-stu-id="07549-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="07549-147">SplitButton 錨點。</span><span class="sxs-lookup"><span data-stu-id="07549-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="07549-148">沒有標頭的<strong>標準色彩</strong>樣本方格。</span><span class="sxs-lookup"><span data-stu-id="07549-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="07549-149">預設不會顯示<strong>色彩</strong>色彩按鈕。</span><span class="sxs-lookup"><span data-stu-id="07549-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07549-150"><strong>資料行</strong></span><span class="sxs-lookup"><span data-stu-id="07549-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="07549-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="07549-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="07549-152">否</span><span class="sxs-lookup"><span data-stu-id="07549-152">No</span></span><br/></td>
<td><span data-ttu-id="07549-153">色板 (或樣本) 資料行的數目。</span><span class="sxs-lookup"><span data-stu-id="07549-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="07549-154">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) </span><span class="sxs-lookup"><span data-stu-id="07549-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="07549-155">介於1和256之間的任何正整數值（含）。</span><span class="sxs-lookup"><span data-stu-id="07549-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07549-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="07549-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="07549-157">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="07549-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="07549-158">否</span><span class="sxs-lookup"><span data-stu-id="07549-158">No</span></span><br/></td>
<td><span data-ttu-id="07549-159">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="07549-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="07549-160">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="07549-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="07549-161">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="07549-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="07549-162">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="07549-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="07549-163">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="07549-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07549-164"><strong>IsAutomaticColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="07549-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="07549-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="07549-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="07549-166">否</span><span class="sxs-lookup"><span data-stu-id="07549-166">No</span></span><br/></td>
<td><span data-ttu-id="07549-167">顯示 (或隱藏) [ <strong>自動</strong> 色彩] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="07549-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="07549-168">只有在 <code>StandardColors</code> <code>ThemeColors</code> 為 <em>ColorTemplate</em> 屬性指定或時有效。</span><span class="sxs-lookup"><span data-stu-id="07549-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="07549-169">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="07549-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="07549-170">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="07549-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="07549-171"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="07549-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07549-172"><strong>IsNoColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="07549-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="07549-173">Boolean</span><span class="sxs-lookup"><span data-stu-id="07549-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="07549-174">否</span><span class="sxs-lookup"><span data-stu-id="07549-174">No</span></span><br/></td>
<td><span data-ttu-id="07549-175">顯示 (或隱藏) [ <strong>無色彩</strong> ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="07549-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="07549-176">對所有 <em>ColorTemplate</em> 值都有效。</span><span class="sxs-lookup"><span data-stu-id="07549-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="07549-177">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="07549-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="07549-178">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="07549-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="07549-179"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="07549-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07549-180"><strong>RecentColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="07549-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="07549-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="07549-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="07549-182">否</span><span class="sxs-lookup"><span data-stu-id="07549-182">No</span></span><br/></td>
<td><span data-ttu-id="07549-183">[ <strong>最近使用的色彩</strong> ] 區域中的色晶片 (或樣本) 資料列數目。</span><span class="sxs-lookup"><span data-stu-id="07549-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="07549-184">只有在 <code>ThemeColors</code> 為 <em>ColorTemplate</em> 屬性指定時才有效。</span><span class="sxs-lookup"><span data-stu-id="07549-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="07549-185">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) </span><span class="sxs-lookup"><span data-stu-id="07549-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="07549-186">介於1和256之間的任何正整數值（含）。</span><span class="sxs-lookup"><span data-stu-id="07549-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07549-187"><strong>StandardColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="07549-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="07549-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="07549-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="07549-189">否</span><span class="sxs-lookup"><span data-stu-id="07549-189">No</span></span><br/></td>
<td><span data-ttu-id="07549-190"><strong>標準色彩</strong>區域中的色晶片 (或樣本) 資料列數目。</span><span class="sxs-lookup"><span data-stu-id="07549-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="07549-191">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) </span><span class="sxs-lookup"><span data-stu-id="07549-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="07549-192">介於1和256之間的任何正整數值（含）。</span><span class="sxs-lookup"><span data-stu-id="07549-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07549-193"><strong>ThemeColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="07549-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="07549-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="07549-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="07549-195">否</span><span class="sxs-lookup"><span data-stu-id="07549-195">No</span></span><br/></td>
<td><span data-ttu-id="07549-196"><strong>主題色彩</strong>區域中的色晶片 (或樣本) 資料列數目。</span><span class="sxs-lookup"><span data-stu-id="07549-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="07549-197">只有在 <code>ThemeColors</code> 為 <em>ColorTemplate</em> 屬性指定時才有效。</span><span class="sxs-lookup"><span data-stu-id="07549-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="07549-198">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) </span><span class="sxs-lookup"><span data-stu-id="07549-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="07549-199">介於1和256之間的任何正整數值（含）。</span><span class="sxs-lookup"><span data-stu-id="07549-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="07549-200">子元素</span><span class="sxs-lookup"><span data-stu-id="07549-200">Child elements</span></span>

<span data-ttu-id="07549-201">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="07549-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="07549-202">父元素</span><span class="sxs-lookup"><span data-stu-id="07549-202">Parent elements</span></span>



| <span data-ttu-id="07549-203">元素</span><span class="sxs-lookup"><span data-stu-id="07549-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="07549-204">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="07549-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="07549-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="07549-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="07549-206">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="07549-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="07549-207">**群組**</span><span class="sxs-lookup"><span data-stu-id="07549-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="07549-208">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="07549-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="07549-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="07549-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="07549-210">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="07549-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="07549-211">備註</span><span class="sxs-lookup"><span data-stu-id="07549-211">Remarks</span></span>

<span data-ttu-id="07549-212">選擇性。</span><span class="sxs-lookup"><span data-stu-id="07549-212">Optional.</span></span>

<span data-ttu-id="07549-213">可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) 元素執行一次或多次。</span><span class="sxs-lookup"><span data-stu-id="07549-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="07549-214">範例</span><span class="sxs-lookup"><span data-stu-id="07549-214">Examples</span></span>

<span data-ttu-id="07549-215">下列範例示範所有三種類型的 [下拉式色彩選擇器](windowsribbon-controls-dropdowncolorpicker.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="07549-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="07549-216">這段程式碼會顯示三個 **DropDownColorPicker** 元素的命令宣告。</span><span class="sxs-lookup"><span data-stu-id="07549-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


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



<span data-ttu-id="07549-217">這段程式碼會顯示三種類型的 **DropDownColorPicker** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="07549-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="07549-218">項目資訊</span><span class="sxs-lookup"><span data-stu-id="07549-218">Element information</span></span>

* <span data-ttu-id="07549-219">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="07549-219">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="07549-220">**可以是空** 的：是</span><span class="sxs-lookup"><span data-stu-id="07549-220">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="07549-221">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07549-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07549-222">下拉式色彩選擇器控制項</span><span class="sxs-lookup"><span data-stu-id="07549-222">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="07549-223">DropDownColorPicker 範例</span><span class="sxs-lookup"><span data-stu-id="07549-223">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





