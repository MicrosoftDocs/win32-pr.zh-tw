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
ms.openlocfilehash: 31a040fb51ad46feb30147fea97c19210cc16094
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442879"
---
# <a name="flowmenulayout-element"></a><span data-ttu-id="03552-104">FlowMenuLayout 元素</span><span class="sxs-lookup"><span data-stu-id="03552-104">FlowMenuLayout element</span></span>

<span data-ttu-id="03552-105">代表包含資源庫中專案之分行符號的水準配置。</span><span class="sxs-lookup"><span data-stu-id="03552-105">Represents a horizontal layout with line breaks for items in a gallery.</span></span>

## <a name="usage"></a><span data-ttu-id="03552-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="03552-106">Usage</span></span>

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="03552-107">屬性</span><span class="sxs-lookup"><span data-stu-id="03552-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03552-108">屬性</span><span class="sxs-lookup"><span data-stu-id="03552-108">Attribute</span></span></th>
<th><span data-ttu-id="03552-109">類型</span><span class="sxs-lookup"><span data-stu-id="03552-109">Type</span></span></th>
<th><span data-ttu-id="03552-110">必要</span><span class="sxs-lookup"><span data-stu-id="03552-110">Required</span></span></th>
<th><span data-ttu-id="03552-111">說明</span><span class="sxs-lookup"><span data-stu-id="03552-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03552-112"><strong>資料行</strong></span><span class="sxs-lookup"><span data-stu-id="03552-112"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="03552-113">xs:integer</span><span class="sxs-lookup"><span data-stu-id="03552-113">xs:integer</span></span><br/></td>
<td><span data-ttu-id="03552-114">否</span><span class="sxs-lookup"><span data-stu-id="03552-114">No</span></span><br/></td>
<td><span data-ttu-id="03552-115">指定要在單一資料列中顯示的專案數。</span><span class="sxs-lookup"><span data-stu-id="03552-115">Specifies the number of items to display in a single row.</span></span><br/> <br/><span data-ttu-id="03552-116">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="03552-116">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="03552-117">任何正整數或負整數。</span><span class="sxs-lookup"><span data-stu-id="03552-117">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="03552-118">預設值為 <strong>2</strong>。</span><span class="sxs-lookup"><span data-stu-id="03552-118">The default is <strong>2</strong>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03552-119"><strong>片 梭</strong></span><span class="sxs-lookup"><span data-stu-id="03552-119"><strong>Gripper</strong></span></span><br/></td>
<td><span data-ttu-id="03552-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="03552-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="03552-121">否</span><span class="sxs-lookup"><span data-stu-id="03552-121">No</span></span><br/></td>
<td><span data-ttu-id="03552-122">附加至圖庫下拉式清單的調整大小控點。</span><span class="sxs-lookup"><span data-stu-id="03552-122">A resizing handle attached to the gallery drop down.</span></span> <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> <span data-ttu-id="03552-123">限制為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="03552-123">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="03552-124">
<dt><span></span><span></span><strong></strong> (無) </span><span class="sxs-lookup"><span data-stu-id="03552-124">
<dt><span></span><span></span><strong></strong> (None)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="03552-125"><dt><span></span><span></span><strong></strong> (垂直) </span><span class="sxs-lookup"><span data-stu-id="03552-125"><dt><span></span><span></span><strong></strong> (Vertical)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="03552-126"><dt><span></span><span></span><strong></strong> (角落) </span><span class="sxs-lookup"><span data-stu-id="03552-126"><dt><span></span><span></span><strong></strong> (Corner)</span></span><br/> </dt> <dd> <span data-ttu-id="03552-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="03552-127">Default.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03552-128"><strong>資料列</strong></span><span class="sxs-lookup"><span data-stu-id="03552-128"><strong>Rows</strong></span></span><br/></td>
<td><span data-ttu-id="03552-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="03552-129">xs:integer</span></span><br/></td>
<td><span data-ttu-id="03552-130">否</span><span class="sxs-lookup"><span data-stu-id="03552-130">No</span></span><br/></td>
<td><span data-ttu-id="03552-131">指定要顯示但不需要滾動的專案資料列數目。</span><span class="sxs-lookup"><span data-stu-id="03552-131">Specifies the number of item rows to be visible without scrolling.</span></span> <br/> <br/><span data-ttu-id="03552-132">
<dt><span></span><span></span><strong></strong> (xs： integer) </span><span class="sxs-lookup"><span data-stu-id="03552-132">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="03552-133">任何正整數或負整數。</span><span class="sxs-lookup"><span data-stu-id="03552-133">Any positive or negative integer.</span></span> <br/> <span data-ttu-id="03552-134">預設值為 <strong>-1</strong> ，指定盡可能顯示最多的專案資料列。</span><span class="sxs-lookup"><span data-stu-id="03552-134">The default is <strong>-1</strong> which specifies to display as many item rows as possible.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="03552-135">子元素</span><span class="sxs-lookup"><span data-stu-id="03552-135">Child elements</span></span>

<span data-ttu-id="03552-136">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="03552-136">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="03552-137">父元素</span><span class="sxs-lookup"><span data-stu-id="03552-137">Parent elements</span></span>



| <span data-ttu-id="03552-138">元素</span><span class="sxs-lookup"><span data-stu-id="03552-138">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03552-139">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="03552-139">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [<span data-ttu-id="03552-140">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="03552-140">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [<span data-ttu-id="03552-141">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="03552-141">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="03552-142">備註</span><span class="sxs-lookup"><span data-stu-id="03552-142">Remarks</span></span>

<span data-ttu-id="03552-143">必要。</span><span class="sxs-lookup"><span data-stu-id="03552-143">Required.</span></span>

<span data-ttu-id="03552-144">[**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)或 **FlowMenuLayout** 元素必須針對每個 [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)、 [**InRibbonGallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)或 [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery-menulayout.md)專案進行一次。</span><span class="sxs-lookup"><span data-stu-id="03552-144">Either the [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or the **FlowMenuLayout** element must occur one time for each [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md), or [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) element.</span></span>

<span data-ttu-id="03552-145">專案會根據資料 *列* 和資料 *行* 屬性固有的行分隔屬性來排列。</span><span class="sxs-lookup"><span data-stu-id="03552-145">Elements are arranged according to the line-break properties inherent to the *row* and *column* attributes.</span></span> <span data-ttu-id="03552-146">當內容超過單行的長度時，功能表會中斷線條、換行，並適當地對齊內容。</span><span class="sxs-lookup"><span data-stu-id="03552-146">When content exceeds the length of a single line, the menu breaks lines, wraps lines, and aligns content appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="03552-147">範例</span><span class="sxs-lookup"><span data-stu-id="03552-147">Examples</span></span>

<span data-ttu-id="03552-148">下列範例示範 [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)的基本標記。</span><span class="sxs-lookup"><span data-stu-id="03552-148">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="03552-149">這一段程式碼會顯示具有 **FlowMenuLayout** 規格的 [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="03552-149">This section of code shows the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) control declaration with a **FlowMenuLayout** specification.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="03552-150">項目資訊</span><span class="sxs-lookup"><span data-stu-id="03552-150">Element information</span></span>

* <span data-ttu-id="03552-151">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="03552-151">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="03552-152">**可以是空** 的：是</span><span class="sxs-lookup"><span data-stu-id="03552-152">**Can be empty**: Yes</span></span>


 

 





