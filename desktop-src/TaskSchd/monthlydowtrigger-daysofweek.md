---
title: MonthlyDOWTrigger. DaysOfWeek 屬性
description: 針對腳本，取得或設定工作在一周中的哪幾天執行。
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- DaysOfWeek 屬性工作排程器
- DaysOfWeek 屬性工作排程器，MonthlyDOWTrigger 物件
- MonthlyDOWTrigger 物件工作排程器、DaysOfWeek 屬性
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466441"
---
# <a name="monthlydowtriggerdaysofweek-property"></a><span data-ttu-id="370e9-106">MonthlyDOWTrigger. DaysOfWeek 屬性</span><span class="sxs-lookup"><span data-stu-id="370e9-106">MonthlyDOWTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="370e9-107">針對腳本，取得或設定工作在一周中的哪幾天執行。</span><span class="sxs-lookup"><span data-stu-id="370e9-107">For scripting, gets or sets the days of the week during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="370e9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="370e9-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="370e9-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="370e9-109">Property value</span></span>

<span data-ttu-id="370e9-110">位元遮罩，表示工作在一周中的哪幾天執行。</span><span class="sxs-lookup"><span data-stu-id="370e9-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="370e9-111">備註</span><span class="sxs-lookup"><span data-stu-id="370e9-111">Remarks</span></span>

<span data-ttu-id="370e9-112">下表顯示這個屬性所使用之位元遮罩的對應。</span><span class="sxs-lookup"><span data-stu-id="370e9-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="370e9-113">週中的日</span><span class="sxs-lookup"><span data-stu-id="370e9-113">Day of Week</span></span> | <span data-ttu-id="370e9-114">十六進位值</span><span class="sxs-lookup"><span data-stu-id="370e9-114">Hex Value</span></span> | <span data-ttu-id="370e9-115">十進位值</span><span class="sxs-lookup"><span data-stu-id="370e9-115">Decimal Value</span></span> |
|-------------|-----------|---------------|
| <span data-ttu-id="370e9-116">星期日</span><span class="sxs-lookup"><span data-stu-id="370e9-116">Sunday</span></span>      | <span data-ttu-id="370e9-117">0x01</span><span class="sxs-lookup"><span data-stu-id="370e9-117">0x01</span></span>      | <span data-ttu-id="370e9-118">1</span><span class="sxs-lookup"><span data-stu-id="370e9-118">1</span></span>             |
| <span data-ttu-id="370e9-119">星期一</span><span class="sxs-lookup"><span data-stu-id="370e9-119">Monday</span></span>      | <span data-ttu-id="370e9-120">0x02</span><span class="sxs-lookup"><span data-stu-id="370e9-120">0x02</span></span>      | <span data-ttu-id="370e9-121">2</span><span class="sxs-lookup"><span data-stu-id="370e9-121">2</span></span>             |
| <span data-ttu-id="370e9-122">Tuesday</span><span class="sxs-lookup"><span data-stu-id="370e9-122">Tuesday</span></span>     | <span data-ttu-id="370e9-123">0x04</span><span class="sxs-lookup"><span data-stu-id="370e9-123">0x04</span></span>      | <span data-ttu-id="370e9-124">4</span><span class="sxs-lookup"><span data-stu-id="370e9-124">4</span></span>             |
| <span data-ttu-id="370e9-125">星期三</span><span class="sxs-lookup"><span data-stu-id="370e9-125">Wednesday</span></span>   | <span data-ttu-id="370e9-126">0x08</span><span class="sxs-lookup"><span data-stu-id="370e9-126">0x08</span></span>      | <span data-ttu-id="370e9-127">8</span><span class="sxs-lookup"><span data-stu-id="370e9-127">8</span></span>             |
| <span data-ttu-id="370e9-128">Thursday</span><span class="sxs-lookup"><span data-stu-id="370e9-128">Thursday</span></span>    | <span data-ttu-id="370e9-129">0x10</span><span class="sxs-lookup"><span data-stu-id="370e9-129">0x10</span></span>      | <span data-ttu-id="370e9-130">16</span><span class="sxs-lookup"><span data-stu-id="370e9-130">16</span></span>            |
| <span data-ttu-id="370e9-131">星期五</span><span class="sxs-lookup"><span data-stu-id="370e9-131">Friday</span></span>      | <span data-ttu-id="370e9-132">0x20</span><span class="sxs-lookup"><span data-stu-id="370e9-132">0x20</span></span>      | <span data-ttu-id="370e9-133">32</span><span class="sxs-lookup"><span data-stu-id="370e9-133">32</span></span>            |
| <span data-ttu-id="370e9-134">星期六</span><span class="sxs-lookup"><span data-stu-id="370e9-134">Saturday</span></span>    | <span data-ttu-id="370e9-135">0x40</span><span class="sxs-lookup"><span data-stu-id="370e9-135">0x40</span></span>      | <span data-ttu-id="370e9-136">64</span><span class="sxs-lookup"><span data-stu-id="370e9-136">64</span></span>            |



 

<span data-ttu-id="370e9-137">在讀取或寫入工作的 XML 時， [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) 專案會指定每週每月星期幾行事曆的第幾天。</span><span class="sxs-lookup"><span data-stu-id="370e9-137">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="370e9-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="370e9-138">Requirements</span></span>



| <span data-ttu-id="370e9-139">需求</span><span class="sxs-lookup"><span data-stu-id="370e9-139">Requirement</span></span> | <span data-ttu-id="370e9-140">值</span><span class="sxs-lookup"><span data-stu-id="370e9-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="370e9-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="370e9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="370e9-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="370e9-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="370e9-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="370e9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="370e9-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="370e9-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="370e9-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="370e9-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="370e9-146"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="370e9-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="370e9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="370e9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="370e9-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="370e9-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="370e9-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="370e9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370e9-150">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="370e9-150">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="370e9-151">工作排程器</span><span class="sxs-lookup"><span data-stu-id="370e9-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





