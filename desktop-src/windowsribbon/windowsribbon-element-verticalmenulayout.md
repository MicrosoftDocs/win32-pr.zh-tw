---
title: VerticalMenuLayout 元素
description: 代表資源庫中專案的垂直版面配置。
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- VerticalMenuLayout 元素視窗功能區
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e6f3e4a691c9691b9bc6c8c6d760bb10635d8d8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444049"
---
# <a name="verticalmenulayout-element"></a><span data-ttu-id="efb39-104">VerticalMenuLayout 元素</span><span class="sxs-lookup"><span data-stu-id="efb39-104">VerticalMenuLayout element</span></span>

<span data-ttu-id="efb39-105">代表資源庫中專案的垂直版面配置。</span><span class="sxs-lookup"><span data-stu-id="efb39-105">Represents a vertical layout for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="efb39-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="efb39-106">Usage</span></span>

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="efb39-107">屬性</span><span class="sxs-lookup"><span data-stu-id="efb39-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="efb39-108">屬性</span><span class="sxs-lookup"><span data-stu-id="efb39-108">Attribute</span></span></th>
<th><span data-ttu-id="efb39-109">類型</span><span class="sxs-lookup"><span data-stu-id="efb39-109">Type</span></span></th>
<th><span data-ttu-id="efb39-110">必要</span><span class="sxs-lookup"><span data-stu-id="efb39-110">Required</span></span></th>
<th><span data-ttu-id="efb39-111">描述</span><span class="sxs-lookup"><span data-stu-id="efb39-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="efb39-112"><strong>片 梭</strong></span><span class="sxs-lookup"><span data-stu-id="efb39-112"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="efb39-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="efb39-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="efb39-114">否</span><span class="sxs-lookup"><span data-stu-id="efb39-114">No</span></span><br/></td>
<td><span data-ttu-id="efb39-115">附加至圖庫下拉式清單的調整大小控點。</span><span class="sxs-lookup"><span data-stu-id="efb39-115">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="efb39-116">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="efb39-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="efb39-117">
<dt><span></span><span></span><strong></strong> (無) </span><span class="sxs-lookup"><span data-stu-id="efb39-117">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="efb39-118"><dt><span></span><span></span><strong></strong> (垂直) </span><span class="sxs-lookup"><span data-stu-id="efb39-118"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd> <span data-ttu-id="efb39-119">預設值。</span><span class="sxs-lookup"><span data-stu-id="efb39-119">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efb39-120"><strong>IsMultipleHighlightingEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="efb39-120"><strong>IsMultipleHighlightingEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="efb39-121">xs:boolean</span><span class="sxs-lookup"><span data-stu-id="efb39-121">xs:boolean</span></span><br/></td>
<td><span data-ttu-id="efb39-122">否</span><span class="sxs-lookup"><span data-stu-id="efb39-122">No</span></span><br/></td>
<td><span data-ttu-id="efb39-123"><strong>Windows 8 和更新版本</strong></span><span class="sxs-lookup"><span data-stu-id="efb39-123"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="efb39-124">將清單中的所有專案反白顯示，並包含目前的滑鼠懸停專案 (而不是僅) 滑鼠停用的專案。</span><span class="sxs-lookup"><span data-stu-id="efb39-124">Highlights all items in the list up to, and including, the current mouseover item (instead of the mouseover item only).</span></span> <span data-ttu-id="efb39-125">通常用於多個 <strong>復原</strong> 和 <strong>重做</strong> 功能。</span><span class="sxs-lookup"><span data-stu-id="efb39-125">Typically used for multiple <strong>Undo</strong> and <strong>Redo</strong> functionality.</span></span><br/> <br/><span data-ttu-id="efb39-126">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="efb39-126">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="efb39-127"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="efb39-127"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="efb39-128">預設值。</span><span class="sxs-lookup"><span data-stu-id="efb39-128">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efb39-129"><strong>資料列</strong></span><span class="sxs-lookup"><span data-stu-id="efb39-129"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="efb39-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="efb39-130">xs:integer</span></span><br/></td>
<td><span data-ttu-id="efb39-131">否</span><span class="sxs-lookup"><span data-stu-id="efb39-131">No</span></span><br/></td>
<td><span data-ttu-id="efb39-132">指定要顯示但不需要滾動的專案資料列數目。</span><span class="sxs-lookup"><span data-stu-id="efb39-132">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="efb39-133">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="efb39-133">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="efb39-134">任何正整數或負整數。</span><span class="sxs-lookup"><span data-stu-id="efb39-134">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="efb39-135">預設值為 <strong>-1</strong> ，指定盡可能顯示最多的專案資料列。</span><span class="sxs-lookup"><span data-stu-id="efb39-135">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="efb39-136">子元素</span><span class="sxs-lookup"><span data-stu-id="efb39-136">Child elements</span></span>

<span data-ttu-id="efb39-137">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="efb39-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="efb39-138">父元素</span><span class="sxs-lookup"><span data-stu-id="efb39-138">Parent elements</span></span>



| <span data-ttu-id="efb39-139">元素</span><span class="sxs-lookup"><span data-stu-id="efb39-139">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efb39-140">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="efb39-140">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="efb39-141">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="efb39-141">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="efb39-142">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="efb39-142">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="efb39-143">備註</span><span class="sxs-lookup"><span data-stu-id="efb39-143">Remarks</span></span>

<span data-ttu-id="efb39-144">必要。</span><span class="sxs-lookup"><span data-stu-id="efb39-144">Required.</span></span>

<span data-ttu-id="efb39-145">**VerticalMenuLayout** 或 [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)元素必須針對每個 [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)、 [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery-menulayout.md)專案進行一次。</span><span class="sxs-lookup"><span data-stu-id="efb39-145">Either the **VerticalMenuLayout** or the [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="efb39-146">範例</span><span class="sxs-lookup"><span data-stu-id="efb39-146">Examples</span></span>

<span data-ttu-id="efb39-147">下列範例示範 **VerticalMenuLayout** 元素的基本標記。</span><span class="sxs-lookup"><span data-stu-id="efb39-147">The following example demonstrates the basic markup for an **VerticalMenuLayout** element.</span></span>

<span data-ttu-id="efb39-148">這段程式碼會顯示 [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="efb39-148">This section of code shows the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="efb39-149">項目資訊</span><span class="sxs-lookup"><span data-stu-id="efb39-149">Element information</span></span>


- <span data-ttu-id="efb39-150">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="efb39-150">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="efb39-151">**可以是空** 的：是</span><span class="sxs-lookup"><span data-stu-id="efb39-151">**Can be empty**: Yes</span></span>



 

 





