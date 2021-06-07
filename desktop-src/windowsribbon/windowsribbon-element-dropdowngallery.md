---
title: DropDownGallery 元素
description: 表示具有資源庫型功能表的 Drop-Down 資源庫控制項。
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- DropDownGallery 元素視窗功能區
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befe0624dfef5910625a0aa067f3ad8cd9882ca2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443419"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="3d5fe-104">DropDownGallery 元素</span><span class="sxs-lookup"><span data-stu-id="3d5fe-104">DropDownGallery element</span></span>

<span data-ttu-id="3d5fe-105">表示含有以圖庫為基礎之功能表的 [下拉式清單庫](windowsribbon-controls-dropdowngallery.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="3d5fe-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="3d5fe-106">Usage</span></span>

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
```

## <a name="attributes"></a><span data-ttu-id="3d5fe-107">屬性</span><span class="sxs-lookup"><span data-stu-id="3d5fe-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d5fe-108">屬性</span><span class="sxs-lookup"><span data-stu-id="3d5fe-108">Attribute</span></span></th>
<th><span data-ttu-id="3d5fe-109">類型</span><span class="sxs-lookup"><span data-stu-id="3d5fe-109">Type</span></span></th>
<th><span data-ttu-id="3d5fe-110">必要</span><span class="sxs-lookup"><span data-stu-id="3d5fe-110">Required</span></span></th>
<th><span data-ttu-id="3d5fe-111">描述</span><span class="sxs-lookup"><span data-stu-id="3d5fe-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d5fe-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="3d5fe-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="3d5fe-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="3d5fe-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="3d5fe-114">否</span><span class="sxs-lookup"><span data-stu-id="3d5fe-114">No</span></span><br/></td>
<td><span data-ttu-id="3d5fe-115">只有在 <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> 是父元素時才有效。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="3d5fe-116">
<dt><span></span><span></span><strong></strong> (xs： string) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3d5fe-117">字串，其中包含0到31之間的整數清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="3d5fe-118">空白字元是有效的，而且會被忽略。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="3d5fe-119">最大長度：250個字元。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d5fe-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="3d5fe-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="3d5fe-121">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="3d5fe-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="3d5fe-122">否</span><span class="sxs-lookup"><span data-stu-id="3d5fe-122">No</span></span><br/></td>
<td><span data-ttu-id="3d5fe-123">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="3d5fe-124">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3d5fe-125">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="3d5fe-126">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="3d5fe-127">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d5fe-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="3d5fe-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="3d5fe-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="3d5fe-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="3d5fe-130">否</span><span class="sxs-lookup"><span data-stu-id="3d5fe-130">No</span></span><br/></td>
<td><span data-ttu-id="3d5fe-131">決定是否要在資源庫控制項中顯示命令的大型或小型影像資源。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3d5fe-132">僅適用于 <em>Type</em> 屬性值等於的資源庫 <code>Command</code> 。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="3d5fe-133">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="3d5fe-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="3d5fe-134">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="3d5fe-135">預設值。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-135">Default.</span></span> <br/> </dd> <span data-ttu-id="3d5fe-136"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d5fe-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="3d5fe-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="3d5fe-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3d5fe-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3d5fe-139">否</span><span class="sxs-lookup"><span data-stu-id="3d5fe-139">No</span></span><br/></td>
<td><span data-ttu-id="3d5fe-140"><dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3d5fe-141">預設值為 -1。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d5fe-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="3d5fe-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="3d5fe-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3d5fe-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="3d5fe-144">否</span><span class="sxs-lookup"><span data-stu-id="3d5fe-144">No</span></span><br/></td>
<td><span data-ttu-id="3d5fe-145"><dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="3d5fe-146">預設值為 -1。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d5fe-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="3d5fe-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="3d5fe-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="3d5fe-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="3d5fe-149">否</span><span class="sxs-lookup"><span data-stu-id="3d5fe-149">No</span></span><br/></td>
<td><span data-ttu-id="3d5fe-150">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="3d5fe-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3d5fe-151">
<dt><span></span><span></span><strong></strong> (底部) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3d5fe-152"><dt><span></span><span></span><strong></strong> (隱藏) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3d5fe-153"><dt><span></span><span></span><strong></strong> (左) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3d5fe-154"><dt><span></span><span></span><strong></strong> (重迭) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3d5fe-155"><dt><span></span><span></span><strong></strong> (右) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3d5fe-156"><dt><span></span><span></span><strong></strong> (Top) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d5fe-157"><strong>類型</strong></span><span class="sxs-lookup"><span data-stu-id="3d5fe-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="3d5fe-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="3d5fe-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="3d5fe-159">否</span><span class="sxs-lookup"><span data-stu-id="3d5fe-159">No</span></span><br/></td>
<td><span data-ttu-id="3d5fe-160">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="3d5fe-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="3d5fe-161">
<dt><span></span><span></span><strong></strong> (專案) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3d5fe-162"><dt><span></span><span></span><strong></strong> (命令) </span><span class="sxs-lookup"><span data-stu-id="3d5fe-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3d5fe-163">子元素</span><span class="sxs-lookup"><span data-stu-id="3d5fe-163">Child elements</span></span>



| <span data-ttu-id="3d5fe-164">元素</span><span class="sxs-lookup"><span data-stu-id="3d5fe-164">Element</span></span>                                                                                           | <span data-ttu-id="3d5fe-165">描述</span><span class="sxs-lookup"><span data-stu-id="3d5fe-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="3d5fe-166">**Button**</span><span class="sxs-lookup"><span data-stu-id="3d5fe-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="3d5fe-167">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3d5fe-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3d5fe-168">**相應**</span><span class="sxs-lookup"><span data-stu-id="3d5fe-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="3d5fe-169">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3d5fe-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3d5fe-170">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="3d5fe-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="3d5fe-171">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="3d5fe-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="3d5fe-172">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="3d5fe-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="3d5fe-173">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="3d5fe-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="3d5fe-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="3d5fe-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="3d5fe-175">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3d5fe-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="3d5fe-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="3d5fe-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="3d5fe-177">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="3d5fe-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3d5fe-178">父元素</span><span class="sxs-lookup"><span data-stu-id="3d5fe-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d5fe-179">元素</span><span class="sxs-lookup"><span data-stu-id="3d5fe-179">Element</span></span></th>
<th><span data-ttu-id="3d5fe-180">描述</span><span class="sxs-lookup"><span data-stu-id="3d5fe-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d5fe-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d5fe-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3d5fe-182"><a href="windowsribbon-element-group.md"><strong>群組</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d5fe-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3d5fe-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d5fe-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="3d5fe-184">包含在 <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>中的。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="3d5fe-185">只有第一個層級才支援這個元素，而且必須沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d5fe-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d5fe-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="3d5fe-187">Windows 8 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d5fe-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="3d5fe-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="3d5fe-189">備註</span><span class="sxs-lookup"><span data-stu-id="3d5fe-189">Remarks</span></span>

<span data-ttu-id="3d5fe-190">選擇性。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-190">Optional.</span></span>

<span data-ttu-id="3d5fe-191">可能會針對每個 [**ControlGroup**](windowsribbon-element-controlgroup.md)、 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)、 [**Group**](windowsribbon-element-group.md)、 [**MenuGroup**](windowsribbon-element-menugroup.md)或 [**SplitButton**](windowsribbon-element-splitbutton.md) 元素執行一次或多次。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="3d5fe-192">**DropDownGallery** 支援 [應用程式模式](ribbon-applicationmodes.md)。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="3d5fe-193">下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中的功能區 [下拉式圖庫](windowsribbon-controls-dropdowngallery.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![適用于 windows 7 的 microsoft 油漆中，下拉式圖庫控制項的螢幕擷取畫面。](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="3d5fe-195">範例</span><span class="sxs-lookup"><span data-stu-id="3d5fe-195">Examples</span></span>

<span data-ttu-id="3d5fe-196">下列範例示範 **DropDownGallery** 的基本標記。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="3d5fe-197">這段程式碼會顯示 **DropDownGallery** 命令宣告，以及可做為 **DropDownGallery** 元素之父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



<span data-ttu-id="3d5fe-198">這段程式碼會顯示 **DropDownGallery** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="3d5fe-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="3d5fe-199">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3d5fe-199">Element information</span></span>

* <span data-ttu-id="3d5fe-200">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d5fe-200">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="3d5fe-201">**可以是空** 的：否</span><span class="sxs-lookup"><span data-stu-id="3d5fe-201">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="3d5fe-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d5fe-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5fe-203">**下拉式圖庫控制項**</span><span class="sxs-lookup"><span data-stu-id="3d5fe-203">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="3d5fe-204">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="3d5fe-204">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="3d5fe-205">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="3d5fe-205">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="3d5fe-206">資源庫範例</span><span class="sxs-lookup"><span data-stu-id="3d5fe-206">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

