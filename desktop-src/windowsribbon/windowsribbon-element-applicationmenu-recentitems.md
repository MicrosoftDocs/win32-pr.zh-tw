---
title: ApplicationMenu. RecentItems 屬性
description: 代表 [應用程式] 功能表中 [最近的專案] 控制項的容器。
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- ApplicationMenu. RecentItems 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473ab6436eabd7fcbbbfb533a8ae4afc07098c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384729"
---
# <a name="applicationmenurecentitems-property"></a><span data-ttu-id="ffa86-104">ApplicationMenu. RecentItems 屬性</span><span class="sxs-lookup"><span data-stu-id="ffa86-104">ApplicationMenu.RecentItems property</span></span>

<span data-ttu-id="ffa86-105">代表 [[應用程式] 功能表](windowsribbon-controls-applicationmenu.md)中 [[最近的專案](windowsribbon-controls-recentitems.md)] 控制項的容器。</span><span class="sxs-lookup"><span data-stu-id="ffa86-105">Represents a container for the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="ffa86-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="ffa86-106">Usage</span></span>

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
```

## <a name="attributes"></a><span data-ttu-id="ffa86-107">屬性</span><span class="sxs-lookup"><span data-stu-id="ffa86-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffa86-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ffa86-108">Attribute</span></span></th>
<th><span data-ttu-id="ffa86-109">類型</span><span class="sxs-lookup"><span data-stu-id="ffa86-109">Type</span></span></th>
<th><span data-ttu-id="ffa86-110">必要</span><span class="sxs-lookup"><span data-stu-id="ffa86-110">Required</span></span></th>
<th><span data-ttu-id="ffa86-111">描述</span><span class="sxs-lookup"><span data-stu-id="ffa86-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffa86-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ffa86-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ffa86-113">xs： positiveInteger 或 xs： string</span><span class="sxs-lookup"><span data-stu-id="ffa86-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ffa86-114">No</span><span class="sxs-lookup"><span data-stu-id="ffa86-114">No</span></span><br/></td>
<td><span data-ttu-id="ffa86-115">將元素與 <a href="windowsribbon-element-command.md"><strong>命令</strong></a>產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ffa86-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ffa86-116">
<dt><span></span><span></span><strong></strong> (xs： positiveInteger 或 xs： string) </span><span class="sxs-lookup"><span data-stu-id="ffa86-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ffa86-117">字串、介於2與59999（含）之間的整數值，或介於0x2 與0xea5f （含）之間的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="ffa86-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ffa86-118">值在功能區 XML 檔中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ffa86-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ffa86-119">最大長度：100個字元。</span><span class="sxs-lookup"><span data-stu-id="ffa86-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ffa86-120">子元素</span><span class="sxs-lookup"><span data-stu-id="ffa86-120">Child elements</span></span>



| <span data-ttu-id="ffa86-121">元素</span><span class="sxs-lookup"><span data-stu-id="ffa86-121">Element</span></span>                                                             | <span data-ttu-id="ffa86-122">描述</span><span class="sxs-lookup"><span data-stu-id="ffa86-122">Description</span></span>                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="ffa86-123">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="ffa86-123">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)<br/> | <span data-ttu-id="ffa86-124">必須剛好發生一次</span><span class="sxs-lookup"><span data-stu-id="ffa86-124">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ffa86-125">父元素</span><span class="sxs-lookup"><span data-stu-id="ffa86-125">Parent elements</span></span>



| <span data-ttu-id="ffa86-126">元素</span><span class="sxs-lookup"><span data-stu-id="ffa86-126">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="ffa86-127">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="ffa86-127">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ffa86-128">備註</span><span class="sxs-lookup"><span data-stu-id="ffa86-128">Remarks</span></span>

<span data-ttu-id="ffa86-129">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ffa86-129">Optional.</span></span>

<span data-ttu-id="ffa86-130">每個 [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="ffa86-130">May occur at most once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element.</span></span>

<span data-ttu-id="ffa86-131">[ [最近](windowsribbon-controls-recentitems.md) 使用的專案] 控制項會顯示功能區應用程式最近使用的 (MRU) Items 清單。</span><span class="sxs-lookup"><span data-stu-id="ffa86-131">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="ffa86-132">範例</span><span class="sxs-lookup"><span data-stu-id="ffa86-132">Examples</span></span>

<span data-ttu-id="ffa86-133">下列範例將示範 [ [最近使用的專案](windowsribbon-controls-recentitems.md) ] 控制項的基本標記。</span><span class="sxs-lookup"><span data-stu-id="ffa86-133">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="ffa86-134">下列範例顯示 [**RecentItems**](windowsribbon-element-recentitems.md) 命令聲明。</span><span class="sxs-lookup"><span data-stu-id="ffa86-134">The following example shows a [**RecentItems**](windowsribbon-element-recentitems.md) Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="ffa86-135">下列範例顯示相關聯的 **ApplicationMenu RecentItems** 和 [**RecentItems**](windowsribbon-element-recentitems.md) 控制項宣告。</span><span class="sxs-lookup"><span data-stu-id="ffa86-135">The following example shows the associated **ApplicationMenu.RecentItems** and [**RecentItems**](windowsribbon-element-recentitems.md) controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a><span data-ttu-id="ffa86-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffa86-136">Requirements</span></span>



| <span data-ttu-id="ffa86-137">需求</span><span class="sxs-lookup"><span data-stu-id="ffa86-137">Requirement</span></span> | <span data-ttu-id="ffa86-138">值</span><span class="sxs-lookup"><span data-stu-id="ffa86-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ffa86-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffa86-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa86-140">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffa86-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ffa86-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffa86-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa86-142">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffa86-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ffa86-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffa86-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa86-144">應用程式功能表控制項</span><span class="sxs-lookup"><span data-stu-id="ffa86-144">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="ffa86-145">最近的專案控制項</span><span class="sxs-lookup"><span data-stu-id="ffa86-145">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





