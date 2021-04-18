---
title: FlowMenuLayout 元素
description: 代表包含資源庫中專案之分行符號的水準配置。
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- FlowMenuLayout 元素視窗功能區
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965407"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="594cf-104">FlowMenuLayout 元素</span><span class="sxs-lookup"><span data-stu-id="594cf-104">FlowMenuLayout element</span></span>

<span data-ttu-id="594cf-105">代表包含資源庫中專案之分行符號的水準配置。</span><span class="sxs-lookup"><span data-stu-id="594cf-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="594cf-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="594cf-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="594cf-107">屬性</span><span class="sxs-lookup"><span data-stu-id="594cf-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="594cf-108">屬性</span><span class="sxs-lookup"><span data-stu-id="594cf-108">Attribute</span></span></th>
<th><span data-ttu-id="594cf-109">類型</span><span class="sxs-lookup"><span data-stu-id="594cf-109">Type</span></span></th>
<th><span data-ttu-id="594cf-110">必要</span><span class="sxs-lookup"><span data-stu-id="594cf-110">Required</span></span></th>
<th><span data-ttu-id="594cf-111">說明</span><span class="sxs-lookup"><span data-stu-id="594cf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="594cf-112"><strong>資料行</strong></span><span class="sxs-lookup"><span data-stu-id="594cf-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="594cf-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="594cf-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="594cf-114">No</span><span class="sxs-lookup"><span data-stu-id="594cf-114">No</span></span><br/></td>
<td><span data-ttu-id="594cf-115">指定要在單一資料列中顯示的專案數。</span><span class="sxs-lookup"><span data-stu-id="594cf-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="594cf-116">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="594cf-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="594cf-117">任何正整數或負整數。</span><span class="sxs-lookup"><span data-stu-id="594cf-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="594cf-118">預設值為 <strong>2</strong>。</span><span class="sxs-lookup"><span data-stu-id="594cf-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="594cf-119"><strong>片 梭</strong></span><span class="sxs-lookup"><span data-stu-id="594cf-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="594cf-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="594cf-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="594cf-121">No</span><span class="sxs-lookup"><span data-stu-id="594cf-121">No</span></span><br/></td>
<td><span data-ttu-id="594cf-122">附加至圖庫下拉式清單的調整大小控點。</span><span class="sxs-lookup"><span data-stu-id="594cf-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="594cf-123">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="594cf-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="594cf-124">
<dt><span></span><span></span><strong></strong> (無) </span><span class="sxs-lookup"><span data-stu-id="594cf-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="594cf-125"><dt><span></span><span></span><strong></strong> (垂直) </span><span class="sxs-lookup"><span data-stu-id="594cf-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="594cf-126"><dt><span></span><span></span><strong></strong> (角落) </span><span class="sxs-lookup"><span data-stu-id="594cf-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="594cf-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="594cf-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="594cf-128"><strong>資料列</strong></span><span class="sxs-lookup"><span data-stu-id="594cf-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="594cf-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="594cf-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="594cf-130">No</span><span class="sxs-lookup"><span data-stu-id="594cf-130">No</span></span><br/></td>
<td><span data-ttu-id="594cf-131">指定要顯示但不需要滾動的專案資料列數目。</span><span class="sxs-lookup"><span data-stu-id="594cf-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="594cf-132">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="594cf-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="594cf-133">任何正整數或負整數。</span><span class="sxs-lookup"><span data-stu-id="594cf-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="594cf-134">預設值為 <strong>-1</strong> ，指定盡可能顯示最多的專案資料列。</span><span class="sxs-lookup"><span data-stu-id="594cf-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="594cf-135">子元素</span><span class="sxs-lookup"><span data-stu-id="594cf-135">Child elements</span></span>

<span data-ttu-id="594cf-136">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="594cf-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="594cf-137">父元素</span><span class="sxs-lookup"><span data-stu-id="594cf-137">Parent elements</span></span>



| <span data-ttu-id="594cf-138">元素</span><span class="sxs-lookup"><span data-stu-id="594cf-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="594cf-139">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="594cf-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="594cf-140">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="594cf-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="594cf-141">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="594cf-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="594cf-142">備註</span><span class="sxs-lookup"><span data-stu-id="594cf-142">Remarks</span></span>

<span data-ttu-id="594cf-143">必要。</span><span class="sxs-lookup"><span data-stu-id="594cf-143">Required.</span></span>

<span data-ttu-id="594cf-144">[**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)或 **FlowMenuLayout** 元素必須針對每個 [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)、 [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery-menulayout.md)專案進行一次。</span><span class="sxs-lookup"><span data-stu-id="594cf-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="594cf-145">專案會根據資料 *列* 和資料 *行* 屬性固有的行分隔屬性來排列。</span><span class="sxs-lookup"><span data-stu-id="594cf-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="594cf-146">當內容超過單行的長度時，功能表會中斷線條、換行，並適當地對齊內容。</span><span class="sxs-lookup"><span data-stu-id="594cf-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="594cf-147">範例</span><span class="sxs-lookup"><span data-stu-id="594cf-147">Examples</span></span>

<span data-ttu-id="594cf-148">下列範例示範 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="594cf-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="594cf-149">這一段程式碼會顯示具有 **FlowMenuLayout** 規格的 [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="594cf-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="594cf-150">項目資訊</span><span class="sxs-lookup"><span data-stu-id="594cf-150">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="594cf-151">最低支援系統</span><span class="sxs-lookup"><span data-stu-id="594cf-151">Minimum supported system</span></span><br/> | <span data-ttu-id="594cf-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="594cf-152">Windows 7</span></span> |
| <span data-ttu-id="594cf-153">可以是空的</span><span class="sxs-lookup"><span data-stu-id="594cf-153">Can be empty</span></span>                        | <span data-ttu-id="594cf-154">是</span><span class="sxs-lookup"><span data-stu-id="594cf-154">Yes</span></span>       |



 

 





