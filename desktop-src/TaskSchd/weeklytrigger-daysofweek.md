---
title: WeeklyTrigger. DaysOfWeek 屬性
description: 針對腳本，取得或設定工作執行的星期幾。
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- DaysOfWeek 屬性工作排程器
- DaysOfWeek 屬性工作排程器，WeeklyTrigger 物件
- WeeklyTrigger 物件工作排程器、DaysOfWeek 屬性
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509476"
---
# <a name="weeklytriggerdaysofweek-property"></a><span data-ttu-id="23516-106">WeeklyTrigger. DaysOfWeek 屬性</span><span class="sxs-lookup"><span data-stu-id="23516-106">WeeklyTrigger.DaysOfWeek property</span></span>

<span data-ttu-id="23516-107">針對腳本，取得或設定工作執行的星期幾。</span><span class="sxs-lookup"><span data-stu-id="23516-107">For scripting, gets or sets the days of the week on which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="23516-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="23516-108">Syntax</span></span>


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a><span data-ttu-id="23516-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="23516-109">Property value</span></span>

<span data-ttu-id="23516-110">位元遮罩，表示工作在一周中的哪幾天執行。</span><span class="sxs-lookup"><span data-stu-id="23516-110">A bitwise mask that indicates the days of the week on which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="23516-111">備註</span><span class="sxs-lookup"><span data-stu-id="23516-111">Remarks</span></span>

<span data-ttu-id="23516-112">下表顯示這個屬性所使用之位元遮罩的對應。</span><span class="sxs-lookup"><span data-stu-id="23516-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="23516-113">Month</span><span class="sxs-lookup"><span data-stu-id="23516-113">Month</span></span>     | <span data-ttu-id="23516-114">十六進位值</span><span class="sxs-lookup"><span data-stu-id="23516-114">Hex value</span></span> | <span data-ttu-id="23516-115">十進位值</span><span class="sxs-lookup"><span data-stu-id="23516-115">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="23516-116">星期日</span><span class="sxs-lookup"><span data-stu-id="23516-116">Sunday</span></span>    | <span data-ttu-id="23516-117">0X01</span><span class="sxs-lookup"><span data-stu-id="23516-117">0X01</span></span>      | <span data-ttu-id="23516-118">1</span><span class="sxs-lookup"><span data-stu-id="23516-118">1</span></span>             |
| <span data-ttu-id="23516-119">星期一</span><span class="sxs-lookup"><span data-stu-id="23516-119">Monday</span></span>    | <span data-ttu-id="23516-120">0x02</span><span class="sxs-lookup"><span data-stu-id="23516-120">0x02</span></span>      | <span data-ttu-id="23516-121">2</span><span class="sxs-lookup"><span data-stu-id="23516-121">2</span></span>             |
| <span data-ttu-id="23516-122">Tuesday</span><span class="sxs-lookup"><span data-stu-id="23516-122">Tuesday</span></span>   | <span data-ttu-id="23516-123">0X04</span><span class="sxs-lookup"><span data-stu-id="23516-123">0X04</span></span>      | <span data-ttu-id="23516-124">4</span><span class="sxs-lookup"><span data-stu-id="23516-124">4</span></span>             |
| <span data-ttu-id="23516-125">星期三</span><span class="sxs-lookup"><span data-stu-id="23516-125">Wednesday</span></span> | <span data-ttu-id="23516-126">0X08</span><span class="sxs-lookup"><span data-stu-id="23516-126">0X08</span></span>      | <span data-ttu-id="23516-127">8</span><span class="sxs-lookup"><span data-stu-id="23516-127">8</span></span>             |
| <span data-ttu-id="23516-128">Thursday</span><span class="sxs-lookup"><span data-stu-id="23516-128">Thursday</span></span>  | <span data-ttu-id="23516-129">0X10</span><span class="sxs-lookup"><span data-stu-id="23516-129">0X10</span></span>      | <span data-ttu-id="23516-130">16</span><span class="sxs-lookup"><span data-stu-id="23516-130">16</span></span>            |
| <span data-ttu-id="23516-131">星期五</span><span class="sxs-lookup"><span data-stu-id="23516-131">Friday</span></span>    | <span data-ttu-id="23516-132">0x20</span><span class="sxs-lookup"><span data-stu-id="23516-132">0x20</span></span>      | <span data-ttu-id="23516-133">32</span><span class="sxs-lookup"><span data-stu-id="23516-133">32</span></span>            |
| <span data-ttu-id="23516-134">星期六</span><span class="sxs-lookup"><span data-stu-id="23516-134">Saturday</span></span>  | <span data-ttu-id="23516-135">0X40</span><span class="sxs-lookup"><span data-stu-id="23516-135">0X40</span></span>      | <span data-ttu-id="23516-136">64</span><span class="sxs-lookup"><span data-stu-id="23516-136">64</span></span>            |



 

<span data-ttu-id="23516-137">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) 元素來指定一周中的天數。</span><span class="sxs-lookup"><span data-stu-id="23516-137">When reading or writing your own XML for a task, the days of the week are specified using the [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="23516-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="23516-138">Requirements</span></span>



| <span data-ttu-id="23516-139">需求</span><span class="sxs-lookup"><span data-stu-id="23516-139">Requirement</span></span> | <span data-ttu-id="23516-140">值</span><span class="sxs-lookup"><span data-stu-id="23516-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23516-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23516-141">Minimum supported client</span></span><br/> | <span data-ttu-id="23516-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23516-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="23516-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23516-143">Minimum supported server</span></span><br/> | <span data-ttu-id="23516-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23516-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23516-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="23516-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="23516-146"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23516-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23516-147">DLL</span><span class="sxs-lookup"><span data-stu-id="23516-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23516-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23516-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23516-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23516-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23516-150">工作排程器</span><span class="sxs-lookup"><span data-stu-id="23516-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





