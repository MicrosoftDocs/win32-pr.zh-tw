---
title: RecentItems 元素
description: 代表 [應用程式] 功能表中的 [最近的專案] 控制項。
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- RecentItems 元素視窗功能區
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a433e2f04eae8607b0c14c5494c734ad0f0dd83a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444109"
---
# <a name="recentitems-element"></a><span data-ttu-id="e9ff5-104">RecentItems 元素</span><span class="sxs-lookup"><span data-stu-id="e9ff5-104">RecentItems element</span></span>

<span data-ttu-id="e9ff5-105">代表 [[應用程式] 功能表](windowsribbon-controls-applicationmenu.md)中的 [[最近的專案](windowsribbon-controls-recentitems.md)] 控制項。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="e9ff5-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="e9ff5-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="e9ff5-107">屬性</span><span class="sxs-lookup"><span data-stu-id="e9ff5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9ff5-108">屬性</span><span class="sxs-lookup"><span data-stu-id="e9ff5-108">Attribute</span></span></th>
<th><span data-ttu-id="e9ff5-109">類型</span><span class="sxs-lookup"><span data-stu-id="e9ff5-109">Type</span></span></th>
<th><span data-ttu-id="e9ff5-110">必要</span><span class="sxs-lookup"><span data-stu-id="e9ff5-110">Required</span></span></th>
<th><span data-ttu-id="e9ff5-111">描述</span><span class="sxs-lookup"><span data-stu-id="e9ff5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9ff5-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="e9ff5-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="e9ff5-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="e9ff5-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="e9ff5-114">否</span><span class="sxs-lookup"><span data-stu-id="e9ff5-114">No</span></span><br/></td>
<td><span data-ttu-id="e9ff5-115">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="e9ff5-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="e9ff5-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e9ff5-117">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="e9ff5-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="e9ff5-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9ff5-120"><strong>EnablePinning</strong></span><span class="sxs-lookup"><span data-stu-id="e9ff5-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="e9ff5-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="e9ff5-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="e9ff5-122">否</span><span class="sxs-lookup"><span data-stu-id="e9ff5-122">No</span></span><br/></td>
<td><span data-ttu-id="e9ff5-123">限制為下列其中一個值 (0 和1不是有效的) ：</span><span class="sxs-lookup"><span data-stu-id="e9ff5-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="e9ff5-124">
<dt><span></span><span></span><strong></strong> (true) </span><span class="sxs-lookup"><span data-stu-id="e9ff5-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="e9ff5-125">預設值。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-125">Default.</span></span> <br/> </dd> <span data-ttu-id="e9ff5-126"><dt><span></span><span></span><strong></strong> (false) </span><span class="sxs-lookup"><span data-stu-id="e9ff5-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9ff5-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="e9ff5-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="e9ff5-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="e9ff5-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="e9ff5-129">否</span><span class="sxs-lookup"><span data-stu-id="e9ff5-129">No</span></span><br/></td>
<td><span data-ttu-id="e9ff5-130">要顯示的最近專案數目。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="e9ff5-131">
<dt><span></span><span></span><strong></strong> (xs： nonNegativeInteger) </span><span class="sxs-lookup"><span data-stu-id="e9ff5-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="e9ff5-132">0或大於零的整數值。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="e9ff5-133">預設值為 <strong>10</strong>。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e9ff5-134">子元素</span><span class="sxs-lookup"><span data-stu-id="e9ff5-134">Child elements</span></span>

<span data-ttu-id="e9ff5-135">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e9ff5-136">父元素</span><span class="sxs-lookup"><span data-stu-id="e9ff5-136">Parent elements</span></span>



| <span data-ttu-id="e9ff5-137">元素</span><span class="sxs-lookup"><span data-stu-id="e9ff5-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9ff5-138">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="e9ff5-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e9ff5-139">備註</span><span class="sxs-lookup"><span data-stu-id="e9ff5-139">Remarks</span></span>

<span data-ttu-id="e9ff5-140">必要。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-140">Required.</span></span>

<span data-ttu-id="e9ff5-141">必須針對每個 [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) 元素剛好出現一次。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="e9ff5-142">[ [最近](windowsribbon-controls-recentitems.md) 使用的專案] 控制項會顯示功能區應用程式最近使用的 (MRU) Items 清單。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="e9ff5-143">範例</span><span class="sxs-lookup"><span data-stu-id="e9ff5-143">Examples</span></span>

<span data-ttu-id="e9ff5-144">下列範例將示範 [ [最近使用的專案](windowsribbon-controls-recentitems.md) ] 控制項的基本標記。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="e9ff5-145">下列範例顯示 **RecentItems** 命令聲明。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="e9ff5-146">下列範例顯示相關聯的 **RecentItems** 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="e9ff5-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="e9ff5-147">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e9ff5-147">Element information</span></span>

* <span data-ttu-id="e9ff5-148">**最低支援系統**： Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9ff5-148">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="e9ff5-149">**可以是空** 的：是</span><span class="sxs-lookup"><span data-stu-id="e9ff5-149">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="e9ff5-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9ff5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ff5-151">應用程式功能表控制項</span><span class="sxs-lookup"><span data-stu-id="e9ff5-151">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="e9ff5-152">最近的專案控制項</span><span class="sxs-lookup"><span data-stu-id="e9ff5-152">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





