---
title: InRibbonGallery 元素
description: 代表 In-Ribbon 資源庫，此為資源庫型控制項，可直接在功能區中公開專案的預設子集。 按一下下拉式功能表按鈕時，會顯示任何剩餘的專案。
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- InRibbonGallery 元素視窗功能區
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 24ecf9a34c74d8b66f838e0e49c815f00c80b89c
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2020
ms.locfileid: "104023203"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="2b92d-105">InRibbonGallery 元素</span><span class="sxs-lookup"><span data-stu-id="2b92d-105">InRibbonGallery element</span></span>

<span data-ttu-id="2b92d-106">代表 [功能區元件庫](windowsribbon-controls-inribbongallery.md)，此為資源庫型控制項，可直接在功能區中公開專案的預設子集。</span><span class="sxs-lookup"><span data-stu-id="2b92d-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="2b92d-107">按一下下拉式功能表按鈕時，會顯示任何剩餘的專案。</span><span class="sxs-lookup"><span data-stu-id="2b92d-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="2b92d-108">使用方式</span><span class="sxs-lookup"><span data-stu-id="2b92d-108">Usage</span></span>

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
```

## <a name="attributes"></a><span data-ttu-id="2b92d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2b92d-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b92d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2b92d-110">Attribute</span></span></th>
<th><span data-ttu-id="2b92d-111">類型</span><span class="sxs-lookup"><span data-stu-id="2b92d-111">Type</span></span></th>
<th><span data-ttu-id="2b92d-112">必要</span><span class="sxs-lookup"><span data-stu-id="2b92d-112">Required</span></span></th>
<th><span data-ttu-id="2b92d-113">描述</span><span class="sxs-lookup"><span data-stu-id="2b92d-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b92d-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-115">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="2b92d-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2b92d-116">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-116">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-117">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="2b92d-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2b92d-118">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="2b92d-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2b92d-119">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="2b92d-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2b92d-120">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2b92d-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2b92d-121">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="2b92d-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b92d-122"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="2b92d-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="2b92d-124">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-124">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-125">決定是否要在資源庫控制項中顯示命令的大型或小型影像資源。</span><span class="sxs-lookup"><span data-stu-id="2b92d-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2b92d-126">僅適用于 <em>Type</em> 屬性值等於的資源庫 <code>Command</code> 。</span><span class="sxs-lookup"><span data-stu-id="2b92d-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="2b92d-127">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="2b92d-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="2b92d-128">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="2b92d-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="2b92d-129">預設值。</span><span class="sxs-lookup"><span data-stu-id="2b92d-129">Default.</span></span> <br/> </dd> <span data-ttu-id="2b92d-130"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="2b92d-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b92d-131"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2b92d-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2b92d-133">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-133">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-134">搭配 <em>ItemWidth</em>，可決定在資源庫控制項中顯示之專案影像的大小。</span><span class="sxs-lookup"><span data-stu-id="2b92d-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2b92d-135">只適用于 <em>類型</em> 屬性值等於的資源庫</span><span class="sxs-lookup"><span data-stu-id="2b92d-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="2b92d-136">.</span><span class="sxs-lookup"><span data-stu-id="2b92d-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="2b92d-137">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="2b92d-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="2b92d-138">預設值為 -1。</span><span class="sxs-lookup"><span data-stu-id="2b92d-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b92d-139"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2b92d-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2b92d-141">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-141">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-142">搭配 <em>ItemHeight</em>，可決定在資源庫控制項中顯示之專案影像的大小。</span><span class="sxs-lookup"><span data-stu-id="2b92d-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2b92d-143">只適用于 <em>類型</em> 屬性值等於的資源庫</span><span class="sxs-lookup"><span data-stu-id="2b92d-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="2b92d-144">.</span><span class="sxs-lookup"><span data-stu-id="2b92d-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="2b92d-145">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="2b92d-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="2b92d-146">預設值為 -1。</span><span class="sxs-lookup"><span data-stu-id="2b92d-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b92d-147"><strong>MaxColumns</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2b92d-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2b92d-149">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-149">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-150">指定 <strong>InRibbonGallery</strong> 所顯示的最大資料行數目，例如，在 [ <em>大型</em> 群組版面配置] 下拉式清單中。</span><span class="sxs-lookup"><span data-stu-id="2b92d-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="2b92d-151">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="2b92d-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b92d-152"><strong>MaxColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2b92d-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2b92d-154">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-154">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-155">指定在切換至<em>大型</em>版面配置之前， <strong>InRibbonGallery</strong>顯示在<em>中等</em>群組配置中的最大資料行數目。</span><span class="sxs-lookup"><span data-stu-id="2b92d-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="2b92d-156">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="2b92d-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b92d-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2b92d-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2b92d-159">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-159">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-160">指定 <strong>InRibbonGallery</strong> 專案版面配置的最大資料列數。</span><span class="sxs-lookup"><span data-stu-id="2b92d-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="2b92d-161">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="2b92d-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="2b92d-162">預設值是 1。</span><span class="sxs-lookup"><span data-stu-id="2b92d-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b92d-163"><strong>MinColumnsLarge</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2b92d-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2b92d-165">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-165">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-166">在切換至<em>媒體</em>之前，指定<strong>InRibbonGallery</strong>在<em>大型</em>群組配置中顯示的最小資料行數目。</span><span class="sxs-lookup"><span data-stu-id="2b92d-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="2b92d-167">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="2b92d-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b92d-168"><strong>MinColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2b92d-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="2b92d-170">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-170">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-171">指定 <strong>InRibbonGallery</strong> 在 <em>中等</em> 群組配置中顯示的最小資料行數目，然後切換為 <em>小型</em>。</span><span class="sxs-lookup"><span data-stu-id="2b92d-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="2b92d-172">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="2b92d-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b92d-173"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-174">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="2b92d-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="2b92d-175">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-175">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-176">指定專案標籤顯示的位置（相對於影像）。</span><span class="sxs-lookup"><span data-stu-id="2b92d-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="2b92d-177">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="2b92d-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="2b92d-178">
<dt><span></span><span></span><strong></strong> (底部) </span><span class="sxs-lookup"><span data-stu-id="2b92d-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2b92d-179"><dt><span></span><span></span><strong></strong> (隱藏) </span><span class="sxs-lookup"><span data-stu-id="2b92d-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2b92d-180"><dt><span></span><span></span><strong></strong> (左) </span><span class="sxs-lookup"><span data-stu-id="2b92d-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2b92d-181"><dt><span></span><span></span><strong></strong> (重迭) </span><span class="sxs-lookup"><span data-stu-id="2b92d-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2b92d-182"><dt><span></span><span></span><strong></strong> (右) </span><span class="sxs-lookup"><span data-stu-id="2b92d-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2b92d-183"><dt><span></span><span></span><strong></strong> (Top) </span><span class="sxs-lookup"><span data-stu-id="2b92d-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b92d-184"><strong>型別</strong></span><span class="sxs-lookup"><span data-stu-id="2b92d-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="2b92d-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="2b92d-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="2b92d-186">No</span><span class="sxs-lookup"><span data-stu-id="2b92d-186">No</span></span><br/></td>
<td><span data-ttu-id="2b92d-187">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="2b92d-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="2b92d-188">
<dt><span></span><span></span><strong></strong> (專案) </span><span class="sxs-lookup"><span data-stu-id="2b92d-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="2b92d-189"><dt><span></span><span></span><strong></strong> (命令) </span><span class="sxs-lookup"><span data-stu-id="2b92d-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2b92d-190">子元素</span><span class="sxs-lookup"><span data-stu-id="2b92d-190">Child elements</span></span>



| <span data-ttu-id="2b92d-191">元素</span><span class="sxs-lookup"><span data-stu-id="2b92d-191">Element</span></span>                                                                                           | <span data-ttu-id="2b92d-192">描述</span><span class="sxs-lookup"><span data-stu-id="2b92d-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="2b92d-193">**相應**</span><span class="sxs-lookup"><span data-stu-id="2b92d-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="2b92d-194">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2b92d-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2b92d-195">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="2b92d-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="2b92d-196">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="2b92d-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="2b92d-197">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="2b92d-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="2b92d-198">最多可能發生一次</span><span class="sxs-lookup"><span data-stu-id="2b92d-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="2b92d-199">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="2b92d-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="2b92d-200">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2b92d-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2b92d-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="2b92d-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="2b92d-202">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2b92d-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="2b92d-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="2b92d-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="2b92d-204">可能會發生一次或多次</span><span class="sxs-lookup"><span data-stu-id="2b92d-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2b92d-205">父元素</span><span class="sxs-lookup"><span data-stu-id="2b92d-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b92d-206">元素</span><span class="sxs-lookup"><span data-stu-id="2b92d-206">Element</span></span></th>
<th><span data-ttu-id="2b92d-207">描述</span><span class="sxs-lookup"><span data-stu-id="2b92d-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b92d-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b92d-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="2b92d-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b92d-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2b92d-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar. s</strong></a></span><span class="sxs-lookup"><span data-stu-id="2b92d-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="2b92d-211">Windows 8 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="2b92d-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="2b92d-212">備註</span><span class="sxs-lookup"><span data-stu-id="2b92d-212">Remarks</span></span>

<span data-ttu-id="2b92d-213">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2b92d-213">Optional.</span></span>

<span data-ttu-id="2b92d-214">每個 [**ControlGroup**](windowsribbon-element-controlgroup.md) 或 [**群組**](windowsribbon-element-group.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="2b92d-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="2b92d-215">下列螢幕擷取畫面說明 Windows 7 Microsoft 小畫家中功能區元件 [庫](windowsribbon-controls-inribbongallery.md) 控制項的功能區。</span><span class="sxs-lookup"><span data-stu-id="2b92d-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![microsoft 油漆功能區中功能區資源庫控制項的螢幕擷取畫面。](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="2b92d-217">範例</span><span class="sxs-lookup"><span data-stu-id="2b92d-217">Examples</span></span>

<span data-ttu-id="2b92d-218">下列範例會示範 [功能區元件庫](windowsribbon-controls-inribbongallery.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="2b92d-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="2b92d-219">這段程式碼會顯示 **InRibbonGallery** 命令宣告，以及可做為 **InRibbonGallery** 元素之父容器的相關聯 [**群組**](windowsribbon-element-group.md)。</span><span class="sxs-lookup"><span data-stu-id="2b92d-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



<span data-ttu-id="2b92d-220">這段程式碼會顯示 **InRibbonGallery** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="2b92d-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="2b92d-221">項目資訊</span><span class="sxs-lookup"><span data-stu-id="2b92d-221">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2b92d-222">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="2b92d-222">Minimum supported system</span></span><br/> | <span data-ttu-id="2b92d-223">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b92d-223">Windows 7</span></span> |
| <span data-ttu-id="2b92d-224">可以是空的</span><span class="sxs-lookup"><span data-stu-id="2b92d-224">Can be empty</span></span>                        | <span data-ttu-id="2b92d-225">否</span><span class="sxs-lookup"><span data-stu-id="2b92d-225">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="2b92d-226">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b92d-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b92d-227">功能區資源庫控制項</span><span class="sxs-lookup"><span data-stu-id="2b92d-227">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="2b92d-228">使用資源庫</span><span class="sxs-lookup"><span data-stu-id="2b92d-228">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="2b92d-229">資源庫範例</span><span class="sxs-lookup"><span data-stu-id="2b92d-229">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





