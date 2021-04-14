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
# <a name="fontcontrol-element"></a><span data-ttu-id="14a1e-104">FontControl 元素</span><span class="sxs-lookup"><span data-stu-id="14a1e-104">FontControl element</span></span>

<span data-ttu-id="14a1e-105">表示 [字型控制項](windowsribbon-controls-fontcontrol.md)，這是專供字型操作之個別控制項的特殊容器。</span><span class="sxs-lookup"><span data-stu-id="14a1e-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="14a1e-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="14a1e-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="14a1e-107">屬性</span><span class="sxs-lookup"><span data-stu-id="14a1e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14a1e-108">屬性</span><span class="sxs-lookup"><span data-stu-id="14a1e-108">Attribute</span></span></th>
<th><span data-ttu-id="14a1e-109">類型</span><span class="sxs-lookup"><span data-stu-id="14a1e-109">Type</span></span></th>
<th><span data-ttu-id="14a1e-110">必要</span><span class="sxs-lookup"><span data-stu-id="14a1e-110">Required</span></span></th>
<th><span data-ttu-id="14a1e-111">描述</span><span class="sxs-lookup"><span data-stu-id="14a1e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="14a1e-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="14a1e-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="14a1e-114">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-114">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-115">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="14a1e-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="14a1e-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="14a1e-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-117">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="14a1e-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="14a1e-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="14a1e-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="14a1e-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="14a1e-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14a1e-120"><strong>FontType</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="14a1e-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="14a1e-122">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-122">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-123">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="14a1e-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="14a1e-124">
<dt><span></span><span></span><strong></strong> (FontOnly) </span><span class="sxs-lookup"><span data-stu-id="14a1e-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-125">預設值。</span><span class="sxs-lookup"><span data-stu-id="14a1e-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="14a1e-126">將 <em>FontType</em> 屬性設定為可 <code>FontOnly</code> 啟用下列功能：</span><span class="sxs-lookup"><span data-stu-id="14a1e-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="14a1e-127">[<strong>字型家族</strong>] 下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="14a1e-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="14a1e-128"><strong>字型大小</strong> 下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="14a1e-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="14a1e-129"><strong>粗體</strong>、 <strong>斜體</strong>、 <strong>底線</strong>和 <strong>刪除線</strong> 切換按鈕。</span><span class="sxs-lookup"><span data-stu-id="14a1e-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="14a1e-130">預設會顯示 <strong>刪除線</strong> 和 <strong>底線切換按鈕，但</strong> 可以藉由將 <em>IsStrikethroughButtonVisible</em> 和 <em>IsUnderlineButtonVisible</em> 屬性設定為來隱藏 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="14a1e-131"><dt><span></span><span></span><strong></strong> (FontWithColor) </span><span class="sxs-lookup"><span data-stu-id="14a1e-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="14a1e-132">將 <em>FontType</em> 屬性設定為可 <code>FontWithColor</code> 啟用下列功能：</span><span class="sxs-lookup"><span data-stu-id="14a1e-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="14a1e-133">[<strong>字型家族</strong>] 下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="14a1e-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="14a1e-134"><strong>字型大小</strong> 下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="14a1e-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="14a1e-135"><strong>放大字型</strong> 和 <strong>壓縮字型</strong> 大小的遞增和遞減按鈕。</span><span class="sxs-lookup"><span data-stu-id="14a1e-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="14a1e-136"><strong>粗體</strong>、 <strong>斜體</strong>、 <strong>底線</strong>和 <strong>刪除線</strong> 切換按鈕。</span><span class="sxs-lookup"><span data-stu-id="14a1e-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="14a1e-137">預設會顯示 <strong>刪除線</strong> 和 <strong>底線切換按鈕，但</strong> 可以藉由將 <em>IsStrikethroughButtonVisible</em> 和 <em>IsUnderlineButtonVisible</em> 屬性設定為來隱藏 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="14a1e-138"><strong>文字色彩</strong> 色彩選擇器。</span><span class="sxs-lookup"><span data-stu-id="14a1e-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="14a1e-139"><strong>文字反白顯示色彩</strong> 色彩選擇器。</span><span class="sxs-lookup"><span data-stu-id="14a1e-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="14a1e-140">預設會隱藏此控制項，但可以藉由將 <em>IsHighlightButtonVisible</em> 屬性設定為來顯示 <code>true</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="14a1e-141"><dt><span></span><span></span><strong></strong> (RichFont) </span><span class="sxs-lookup"><span data-stu-id="14a1e-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="14a1e-142">將 <em>FontType</em> 屬性設定為可 <code>RichFont</code> 啟用下列功能：</span><span class="sxs-lookup"><span data-stu-id="14a1e-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="14a1e-143">[<strong>字型家族</strong>] 下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="14a1e-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="14a1e-144"><strong>字型大小</strong> 下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="14a1e-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="14a1e-145"><strong>放大字型</strong> 和 <strong>壓縮字型</strong> 大小的遞增和遞減按鈕。</span><span class="sxs-lookup"><span data-stu-id="14a1e-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="14a1e-146"><strong>粗體</strong>、 <strong>斜體</strong>、 <strong>底線</strong>和 <strong>刪除線</strong> 切換按鈕。</span><span class="sxs-lookup"><span data-stu-id="14a1e-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="14a1e-147">預設會顯示 <strong>刪除線</strong> 和 <strong>底線切換按鈕，而且</strong> 無法藉由將 <em>IsStrikethroughButtonVisible</em> 和 <em>IsUnderlineButtonVisible</em> 屬性設定為來隱藏 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="14a1e-148"><strong>文字色彩</strong> 色彩選擇器。</span><span class="sxs-lookup"><span data-stu-id="14a1e-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="14a1e-149"><strong>文字反白顯示色彩</strong> 色彩選擇器。</span><span class="sxs-lookup"><span data-stu-id="14a1e-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="14a1e-150">預設會顯示此控制項，將 <em>IsHighlightButtonVisible</em> 屬性設定為，就無法隱藏這個控制項 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="14a1e-151">注<strong>標</strong>和<strong>上標</strong>切換按鈕。</span><span class="sxs-lookup"><span data-stu-id="14a1e-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14a1e-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="14a1e-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="14a1e-154">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-154">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-155"><strong>Windows 8 和更新版本</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="14a1e-156">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="14a1e-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="14a1e-157">[成長/縮小] 按鈕永遠不會顯示在 <a href="windowsribbon-element-minitoolbar.md"><strong>浮動工具列</strong></a>中。</span><span class="sxs-lookup"><span data-stu-id="14a1e-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="14a1e-158">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="14a1e-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-159"><em>FontType</em>的值等於或時的預設值 <code>FontWithColor</code> <code>RichFont</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="14a1e-160"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="14a1e-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-161"><em>FontType</em>的值等於時的預設值 <code>FontOnly</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14a1e-162"><strong>IsHighlightButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="14a1e-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="14a1e-164">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-164">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-165">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="14a1e-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="14a1e-166">只有當<em>FontType</em>屬性的值等於或時，才可以從<strong>FontControl</strong>中使用色彩反白顯示 <code>FontWithColor</code> <code>RichFont</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="14a1e-167">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="14a1e-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-168"><em>FontType</em>的值等於或時的預設值 <code>FontWithColor</code> <code>RichFont</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="14a1e-169">只有當 <em>FontType</em> 的值等於或時才會有效 <code>FontWithColor</code> <code>RichFont</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="14a1e-170"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="14a1e-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-171"><em>FontType</em>的值等於時的預設值 <code>FontOnly</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="14a1e-172">只有當 <em>FontType</em> 的值等於或時才會有效 <code>FontOnly</code> <code>FontWithColor</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14a1e-173"><strong>IsStrikethroughButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="14a1e-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="14a1e-175">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-175">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-176">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="14a1e-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="14a1e-177">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="14a1e-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-178">預設值。</span><span class="sxs-lookup"><span data-stu-id="14a1e-178">Default.</span></span> <br/> </dd> <span data-ttu-id="14a1e-179"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="14a1e-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-180">只有當 <em>FontType</em> 的值等於或時才會有效 <code>FontOnly</code> <code>FontWithColor</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14a1e-181"><strong>IsUnderlineButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-182">Boolean</span><span class="sxs-lookup"><span data-stu-id="14a1e-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="14a1e-183">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-183">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-184">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="14a1e-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="14a1e-185">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="14a1e-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-186">預設值。</span><span class="sxs-lookup"><span data-stu-id="14a1e-186">Default.</span></span> <br/> </dd> <span data-ttu-id="14a1e-187"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="14a1e-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-188">只有當 <em>FontType</em> 的值等於或時才會有效 <code>FontOnly</code> <code>FontWithColor</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14a1e-189"><strong>MaximumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="14a1e-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="14a1e-191">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-191">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-192">要顯示的最大點大小。</span><span class="sxs-lookup"><span data-stu-id="14a1e-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="14a1e-193">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) </span><span class="sxs-lookup"><span data-stu-id="14a1e-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-194">介於1到9999（含）之間的整數值。</span><span class="sxs-lookup"><span data-stu-id="14a1e-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="14a1e-195">預設值為 <strong>9999</strong>。</span><span class="sxs-lookup"><span data-stu-id="14a1e-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14a1e-196"><strong>MinimumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="14a1e-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="14a1e-198">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-198">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-199">要顯示的最小點大小。</span><span class="sxs-lookup"><span data-stu-id="14a1e-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="14a1e-200">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger) </span><span class="sxs-lookup"><span data-stu-id="14a1e-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-201">介於1到9999（含）之間的整數值。</span><span class="sxs-lookup"><span data-stu-id="14a1e-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="14a1e-202">預設值為 <strong>1</strong>。</span><span class="sxs-lookup"><span data-stu-id="14a1e-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14a1e-203"><strong>ShowTrueTypeOnly</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-204">Boolean</span><span class="sxs-lookup"><span data-stu-id="14a1e-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="14a1e-205">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-205">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-206">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="14a1e-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="14a1e-207">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="14a1e-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-208">只顯示 TrueType 和 OpenType 字型。</span><span class="sxs-lookup"><span data-stu-id="14a1e-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="14a1e-209"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="14a1e-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-210">預設值。</span><span class="sxs-lookup"><span data-stu-id="14a1e-210">Default.</span></span> <span data-ttu-id="14a1e-211">所顯示的字型類型沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="14a1e-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14a1e-212"><strong>ShowVerticalFonts</strong></span><span class="sxs-lookup"><span data-stu-id="14a1e-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="14a1e-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="14a1e-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="14a1e-214">No</span><span class="sxs-lookup"><span data-stu-id="14a1e-214">No</span></span><br/></td>
<td><span data-ttu-id="14a1e-215">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="14a1e-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="14a1e-216">在 <strong>字型系列</strong> 清單中，垂直字型前面會加上 @ 符號。</span><span class="sxs-lookup"><span data-stu-id="14a1e-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="14a1e-217">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="14a1e-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-218">預設值。</span><span class="sxs-lookup"><span data-stu-id="14a1e-218">Default.</span></span> <span data-ttu-id="14a1e-219">顯示設定為<strong>在 [字型</strong>] 控制台中<strong>顯示</strong>的垂直字型。</span><span class="sxs-lookup"><span data-stu-id="14a1e-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="14a1e-220"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="14a1e-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="14a1e-221">允許不支援垂直文字的應用程式隱藏所有設定為 <strong>顯示</strong> 在 <strong>字型 [控制台] 中的垂直</strong> 字型。</span><span class="sxs-lookup"><span data-stu-id="14a1e-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="14a1e-222">在 Windows Vista 中， <strong>[字型</strong> ] 控制台不提供 <strong>顯示</strong> 或 <strong>隱藏</strong> 功能。</span><span class="sxs-lookup"><span data-stu-id="14a1e-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="14a1e-223">在此情況下， <em>ShowVerticalFonts</em> 屬性必須設定為 <code>False</code> 。</span><span class="sxs-lookup"><span data-stu-id="14a1e-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="14a1e-224">子元素</span><span class="sxs-lookup"><span data-stu-id="14a1e-224">Child elements</span></span>

<span data-ttu-id="14a1e-225">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="14a1e-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="14a1e-226">父元素</span><span class="sxs-lookup"><span data-stu-id="14a1e-226">Parent elements</span></span>



| <span data-ttu-id="14a1e-227">元素</span><span class="sxs-lookup"><span data-stu-id="14a1e-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="14a1e-228">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="14a1e-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="14a1e-229">**Group**</span><span class="sxs-lookup"><span data-stu-id="14a1e-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="14a1e-230">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="14a1e-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="14a1e-231">備註</span><span class="sxs-lookup"><span data-stu-id="14a1e-231">Remarks</span></span>

<span data-ttu-id="14a1e-232">選擇性。</span><span class="sxs-lookup"><span data-stu-id="14a1e-232">Optional.</span></span>

<span data-ttu-id="14a1e-233">每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**Group**](windowsribbon-element-group.md)或 [**MenuGroup**](windowsribbon-element-menugroup.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="14a1e-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="14a1e-234">標記中宣告的任何 **FontControl** 命令屬性（例如 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 或 [**TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)）都會由組成 **FontControl** 之個別控制項的屬性覆寫。</span><span class="sxs-lookup"><span data-stu-id="14a1e-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="14a1e-235">如果沒有與控制項相關聯的命令處理常式，嘗試從 [字型控制項](windowsribbon-controls-fontcontrol.md) 的色彩選擇器選取色彩樣本，可能會造成存取違規。</span><span class="sxs-lookup"><span data-stu-id="14a1e-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="14a1e-236">範例</span><span class="sxs-lookup"><span data-stu-id="14a1e-236">Examples</span></span>

<span data-ttu-id="14a1e-237">下列範例示範三種 [字型控制項](windowsribbon-controls-fontcontrol.md)類型的基本標記。</span><span class="sxs-lookup"><span data-stu-id="14a1e-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="14a1e-238">這段程式碼會顯示 **FontControl** 命令宣告，每個宣告都有 [**群組**](windowsribbon-element-group.md) 容器宣告。</span><span class="sxs-lookup"><span data-stu-id="14a1e-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


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



<span data-ttu-id="14a1e-239">這段程式碼會顯示 **FontControl** 控制項宣告，其中每個 **FontControl** 和 [**群組**](windowsribbon-element-group.md) 都在單一索引標籤中宣告。</span><span class="sxs-lookup"><span data-stu-id="14a1e-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="14a1e-240">項目資訊</span><span class="sxs-lookup"><span data-stu-id="14a1e-240">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="14a1e-241">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="14a1e-241">Minimum supported system</span></span><br/> | <span data-ttu-id="14a1e-242">Windows 7</span><span class="sxs-lookup"><span data-stu-id="14a1e-242">Windows 7</span></span> |
| <span data-ttu-id="14a1e-243">可以是空的</span><span class="sxs-lookup"><span data-stu-id="14a1e-243">Can be empty</span></span>                        | <span data-ttu-id="14a1e-244">Yes</span><span class="sxs-lookup"><span data-stu-id="14a1e-244">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="14a1e-245">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14a1e-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a1e-246">字型控制項控制項</span><span class="sxs-lookup"><span data-stu-id="14a1e-246">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="14a1e-247">字型控制項屬性</span><span class="sxs-lookup"><span data-stu-id="14a1e-247">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="14a1e-248">FontControl 範例</span><span class="sxs-lookup"><span data-stu-id="14a1e-248">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





