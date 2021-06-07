---
title: SplitButtonGallery 元素
description: 表示含有以圖庫為基礎之下拉式功能表的分割按鈕資源庫控制項。
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- SplitButtonGallery 元素視窗功能區
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5f8767135b9472acba333b1cdfa6ab102e9b7f4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444829"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="b82f1-104">SplitButtonGallery 元素</span><span class="sxs-lookup"><span data-stu-id="b82f1-104">SplitButtonGallery element</span></span>

<span data-ttu-id="b82f1-105">表示含有以圖庫為基礎之下拉式功能表的 [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="b82f1-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="b82f1-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="b82f1-106">Usage</span></span>

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
```

## <a name="attributes"></a><span data-ttu-id="b82f1-107">屬性</span><span class="sxs-lookup"><span data-stu-id="b82f1-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b82f1-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b82f1-108">Attribute</span></span></th>
<th><span data-ttu-id="b82f1-109">類型</span><span class="sxs-lookup"><span data-stu-id="b82f1-109">Type</span></span></th>
<th><span data-ttu-id="b82f1-110">必要</span><span class="sxs-lookup"><span data-stu-id="b82f1-110">Required</span></span></th>
<th><span data-ttu-id="b82f1-111">描述</span><span class="sxs-lookup"><span data-stu-id="b82f1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b82f1-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="b82f1-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="b82f1-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="b82f1-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="b82f1-114">否</span><span class="sxs-lookup"><span data-stu-id="b82f1-114">No</span></span><br/></td>
<td><span data-ttu-id="b82f1-115">只有在 <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> 是父元素時才有效。</span><span class="sxs-lookup"><span data-stu-id="b82f1-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="b82f1-116">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="b82f1-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b82f1-117">字串，其中包含0到31之間的整數清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="b82f1-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="b82f1-118">空白字元是有效的，而且會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b82f1-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="b82f1-119">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="b82f1-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b82f1-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="b82f1-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="b82f1-121">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="b82f1-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="b82f1-122">否</span><span class="sxs-lookup"><span data-stu-id="b82f1-122">No</span></span><br/></td>
<td><span data-ttu-id="b82f1-123">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b82f1-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="b82f1-124">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="b82f1-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="b82f1-125">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="b82f1-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="b82f1-126">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b82f1-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="b82f1-127">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="b82f1-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b82f1-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="b82f1-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="b82f1-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="b82f1-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="b82f1-130">否</span><span class="sxs-lookup"><span data-stu-id="b82f1-130">No</span></span><br/></td>
<td><span data-ttu-id="b82f1-131">決定是否要在資源庫控制項中顯示命令的大型或小型影像資源。</span><span class="sxs-lookup"><span data-stu-id="b82f1-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b82f1-132">僅適用于 <em>Type</em> 屬性值等於的資源庫 <code>Command</code> 。</span><span class="sxs-lookup"><span data-stu-id="b82f1-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="b82f1-133">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="b82f1-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="b82f1-134">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="b82f1-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="b82f1-135">預設值。</span><span class="sxs-lookup"><span data-stu-id="b82f1-135">Default.</span></span> <br/> </dd> <span data-ttu-id="b82f1-136"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="b82f1-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b82f1-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="b82f1-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="b82f1-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b82f1-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="b82f1-139">否</span><span class="sxs-lookup"><span data-stu-id="b82f1-139">No</span></span><br/></td>
<td><span data-ttu-id="b82f1-140"><dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="b82f1-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="b82f1-141">預設值為 -1。</span><span class="sxs-lookup"><span data-stu-id="b82f1-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b82f1-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="b82f1-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="b82f1-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b82f1-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="b82f1-144">否</span><span class="sxs-lookup"><span data-stu-id="b82f1-144">No</span></span><br/></td>
<td><span data-ttu-id="b82f1-145"><dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="b82f1-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="b82f1-146">預設值為 -1。</span><span class="sxs-lookup"><span data-stu-id="b82f1-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b82f1-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="b82f1-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="b82f1-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="b82f1-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="b82f1-149">否</span><span class="sxs-lookup"><span data-stu-id="b82f1-149">No</span></span><br/></td>
<td><span data-ttu-id="b82f1-150">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="b82f1-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="b82f1-151">
<dt><span></span><span></span><strong></strong> (底部) </span><span class="sxs-lookup"><span data-stu-id="b82f1-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b82f1-152"><dt><span></span><span></span><strong></strong> (隱藏) </span><span class="sxs-lookup"><span data-stu-id="b82f1-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b82f1-153"><dt><span></span><span></span><strong></strong> (左) </span><span class="sxs-lookup"><span data-stu-id="b82f1-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b82f1-154"><dt><span></span><span></span><strong></strong> (重迭) </span><span class="sxs-lookup"><span data-stu-id="b82f1-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b82f1-155"><dt><span></span><span></span><strong></strong> (右) </span><span class="sxs-lookup"><span data-stu-id="b82f1-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b82f1-156"><dt><span></span><span></span><strong></strong> (Top) </span><span class="sxs-lookup"><span data-stu-id="b82f1-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b82f1-157"><strong>類型</strong></span><span class="sxs-lookup"><span data-stu-id="b82f1-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="b82f1-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="b82f1-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="b82f1-159">否</span><span class="sxs-lookup"><span data-stu-id="b82f1-159">No</span></span><br/></td>
<td><span data-ttu-id="b82f1-160">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="b82f1-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="b82f1-161">
<dt><span></span><span></span><strong></strong> (專案) </span><span class="sxs-lookup"><span data-stu-id="b82f1-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="b82f1-162"><dt><span></span><span></span><strong></strong> (命令) </span><span class="sxs-lookup"><span data-stu-id="b82f1-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="b82f1-163">子元素</span><span class="sxs-lookup"><span data-stu-id="b82f1-163">Child elements</span></span>



| <span data-ttu-id="b82f1-164">元素</span><span class="sxs-lookup"><span data-stu-id="b82f1-164">Element</span></span>                                                                                                 | <span data-ttu-id="b82f1-165">描述</span><span class="sxs-lookup"><span data-stu-id="b82f1-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="b82f1-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="b82f1-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="b82f1-167">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="b82f1-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="b82f1-168">**相應**</span><span class="sxs-lookup"><span data-stu-id="b82f1-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="b82f1-169">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="b82f1-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="b82f1-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="b82f1-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="b82f1-171">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="b82f1-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="b82f1-172">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="b82f1-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="b82f1-173">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="b82f1-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="b82f1-174">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="b82f1-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="b82f1-175">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="b82f1-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="b82f1-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="b82f1-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="b82f1-177">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="b82f1-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="b82f1-178">父元素</span><span class="sxs-lookup"><span data-stu-id="b82f1-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b82f1-179">元素</span><span class="sxs-lookup"><span data-stu-id="b82f1-179">Element</span></span></th>
<th><span data-ttu-id="b82f1-180">描述</span><span class="sxs-lookup"><span data-stu-id="b82f1-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b82f1-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="b82f1-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b82f1-182"><a href="windowsribbon-element-group.md"><strong>群組</strong></a></span><span class="sxs-lookup"><span data-stu-id="b82f1-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b82f1-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="b82f1-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="b82f1-184">包含在 <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>中的。</span><span class="sxs-lookup"><span data-stu-id="b82f1-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="b82f1-185">只有第一個層級才支援這個元素，而且必須沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="b82f1-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b82f1-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a></span><span class="sxs-lookup"><span data-stu-id="b82f1-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="b82f1-187">Windows 8 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="b82f1-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b82f1-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="b82f1-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="b82f1-189">備註</span><span class="sxs-lookup"><span data-stu-id="b82f1-189">Remarks</span></span>

<span data-ttu-id="b82f1-190">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b82f1-190">Optional.</span></span>

<span data-ttu-id="b82f1-191">每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)或 [**SplitButton**](windowsribbon-element-splitbutton.md) 元素可能會發生一次或多次。</span><span class="sxs-lookup"><span data-stu-id="b82f1-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="b82f1-192">**SplitButtonGallery** 支援 [應用程式模式](ribbon-applicationmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="b82f1-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="b82f1-193">[UI \_PKEY \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) 是由應用程式用來查詢 **SplitButtonGallery** 按鈕控制項的切換狀態。</span><span class="sxs-lookup"><span data-stu-id="b82f1-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="b82f1-194">下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中的功能區 [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="b82f1-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![適用于 windows 7 的 microsoft 油漆中分割按鈕圖庫控制項的螢幕擷取畫面。](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="b82f1-196">範例</span><span class="sxs-lookup"><span data-stu-id="b82f1-196">Examples</span></span>

<span data-ttu-id="b82f1-197">下列範例示範 [分割按鈕圖庫](windowsribbon-controls-splitbuttongallery.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="b82f1-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="b82f1-198">這段程式碼會顯示 **SplitButtonGallery** 命令宣告，以及可作為 **SplitButtonGallery** 元素之父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="b82f1-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



<span data-ttu-id="b82f1-199">這段程式碼會顯示 **SplitButtonGallery** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="b82f1-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="b82f1-200">項目資訊</span><span class="sxs-lookup"><span data-stu-id="b82f1-200">Element information</span></span>


- <span data-ttu-id="b82f1-201">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="b82f1-201">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="b82f1-202">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="b82f1-202">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="b82f1-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b82f1-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b82f1-204">分割按鈕資源庫控制項</span><span class="sxs-lookup"><span data-stu-id="b82f1-204">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="b82f1-205">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="b82f1-205">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="b82f1-206">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="b82f1-206">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="b82f1-207">資源庫範例</span><span class="sxs-lookup"><span data-stu-id="b82f1-207">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

