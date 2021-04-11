---
title: CounterItem. LineStyle 屬性
description: 抓取或設定用來繪製計數器值的線條樣式。
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- LineStyle 屬性 SysMon
- LineStyle 屬性 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，LineStyle 屬性
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934337"
---
# <a name="counteritemlinestyle-property"></a><span data-ttu-id="bb21d-106">CounterItem. LineStyle 屬性</span><span class="sxs-lookup"><span data-stu-id="bb21d-106">CounterItem.LineStyle property</span></span>

<span data-ttu-id="bb21d-107">抓取或設定用來繪製計數器值的線條樣式。</span><span class="sxs-lookup"><span data-stu-id="bb21d-107">Retrieves or sets the line style used to graph the counter value.</span></span>

<span data-ttu-id="bb21d-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bb21d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb21d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb21d-109">Syntax</span></span>


```VB
Property LineStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="bb21d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="bb21d-110">Property value</span></span>

<span data-ttu-id="bb21d-111">用來繪製計數器值的線條樣式。</span><span class="sxs-lookup"><span data-stu-id="bb21d-111">The line style used to graph the counter value.</span></span> <span data-ttu-id="bb21d-112">這些值會對應至下表中顯示的系統常數。</span><span class="sxs-lookup"><span data-stu-id="bb21d-112">The values correspond to system constants shown in the following table.</span></span>



| <span data-ttu-id="bb21d-113">值</span><span class="sxs-lookup"><span data-stu-id="bb21d-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="bb21d-114">意義</span><span class="sxs-lookup"><span data-stu-id="bb21d-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <span data-ttu-id="bb21d-115"><dt>**Drawing2D. DashStyle. 立體**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bb21d-115"><dt>**System.Drawing.Drawing2D.DashStyle.Solid**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="bb21d-116">實線。</span><span class="sxs-lookup"><span data-stu-id="bb21d-116">Solid line.</span></span> <span data-ttu-id="bb21d-117">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="bb21d-117">This is the default value.</span></span><br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <span data-ttu-id="bb21d-118"><dt>**Drawing2D. DashStyle. 破折號**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bb21d-118"><dt>**System.Drawing.Drawing2D.DashStyle.Dash**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="bb21d-119">具有長段和窄空格的虛線。</span><span class="sxs-lookup"><span data-stu-id="bb21d-119">Dotted line with long segments and narrow spaces.</span></span><br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <span data-ttu-id="bb21d-120"><dt>**Drawing2D. DashStyle 點**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bb21d-120"><dt>**System.Drawing.Drawing2D.DashStyle.Dot**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="bb21d-121">具有統一區段和空格的虛線。</span><span class="sxs-lookup"><span data-stu-id="bb21d-121">Dotted line with uniform segments and spaces.</span></span><br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <span data-ttu-id="bb21d-122"><dt>**Drawing2D. DashStyle. 點**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bb21d-122"><dt>**System.Drawing.Drawing2D.DashStyle.DashDot**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="bb21d-123">具有交替簡短和長段的虛線。</span><span class="sxs-lookup"><span data-stu-id="bb21d-123">Dotted line with alternating short and long segments.</span></span><br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <span data-ttu-id="bb21d-124"><dt>**Drawing2D. DashStyle. DashDotDot**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="bb21d-124"><dt>**System.Drawing.Drawing2D.DashStyle.DashDotDot**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="bb21d-125">具有交替連字號和雙點的虛線。</span><span class="sxs-lookup"><span data-stu-id="bb21d-125">Dotted line with alternating dashes and double dots.</span></span><br/>  |



 

## <a name="exceptions"></a><span data-ttu-id="bb21d-126">例外狀況</span><span class="sxs-lookup"><span data-stu-id="bb21d-126">Exceptions</span></span>



| <span data-ttu-id="bb21d-127">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="bb21d-127">Exception type</span></span>               | <span data-ttu-id="bb21d-128">條件</span><span class="sxs-lookup"><span data-stu-id="bb21d-128">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="bb21d-129">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="bb21d-129">**System.ArgumentException**</span></span> | <span data-ttu-id="bb21d-130">指定的線條樣式無效。</span><span class="sxs-lookup"><span data-stu-id="bb21d-130">The specified line style is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bb21d-131">備註</span><span class="sxs-lookup"><span data-stu-id="bb21d-131">Remarks</span></span>

<span data-ttu-id="bb21d-132">若要指定 DashStyle 以外的值， [**CounterItem 寬度**](counteritem-width.md) 必須設定為1。</span><span class="sxs-lookup"><span data-stu-id="bb21d-132">To specify a value other than DashStyle.Solid, [**CounterItem.Width**](counteritem-width.md) must be set to 1.</span></span> <span data-ttu-id="bb21d-133">如果寬度大於1，SYSMON 會忽略指定的線條樣式並使用 DashStyle。</span><span class="sxs-lookup"><span data-stu-id="bb21d-133">If the width is greater than 1, SYSMON ignores the specified line style and uses DashStyle.Solid.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb21d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb21d-134">Requirements</span></span>



| <span data-ttu-id="bb21d-135">需求</span><span class="sxs-lookup"><span data-stu-id="bb21d-135">Requirement</span></span> | <span data-ttu-id="bb21d-136">值</span><span class="sxs-lookup"><span data-stu-id="bb21d-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb21d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb21d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bb21d-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb21d-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bb21d-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb21d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bb21d-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb21d-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb21d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bb21d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb21d-142"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bb21d-142"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb21d-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb21d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb21d-144">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="bb21d-144">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





