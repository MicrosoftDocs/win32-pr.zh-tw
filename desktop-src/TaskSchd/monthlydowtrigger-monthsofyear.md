---
title: MonthlyDOWTrigger. MonthsOfYear 屬性
description: 針對腳本，取得或設定工作在一年中執行的月份。 |MonthlyDOWTrigger. MonthsOfYear 屬性
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- MonthsOfYear 屬性工作排程器
- MonthsOfYear 屬性工作排程器，MonthlyDOWTrigger 物件
- MonthlyDOWTrigger 物件工作排程器、MonthsOfYear 屬性
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853863"
---
# <a name="monthlydowtriggermonthsofyear-property"></a><span data-ttu-id="86ed1-107">MonthlyDOWTrigger. MonthsOfYear 屬性</span><span class="sxs-lookup"><span data-stu-id="86ed1-107">MonthlyDOWTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="86ed1-108">針對腳本，取得或設定工作在一年中執行的月份。</span><span class="sxs-lookup"><span data-stu-id="86ed1-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ed1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="86ed1-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="86ed1-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="86ed1-110">Property value</span></span>

<span data-ttu-id="86ed1-111">位元遮罩，表示工作執行的年中月份。</span><span class="sxs-lookup"><span data-stu-id="86ed1-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="86ed1-112">備註</span><span class="sxs-lookup"><span data-stu-id="86ed1-112">Remarks</span></span>

<span data-ttu-id="86ed1-113">下表顯示這個屬性所使用之位元遮罩的對應。</span><span class="sxs-lookup"><span data-stu-id="86ed1-113">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="86ed1-114">Month</span><span class="sxs-lookup"><span data-stu-id="86ed1-114">Month</span></span>     | <span data-ttu-id="86ed1-115">十六進位值</span><span class="sxs-lookup"><span data-stu-id="86ed1-115">Hex value</span></span> | <span data-ttu-id="86ed1-116">十進位值</span><span class="sxs-lookup"><span data-stu-id="86ed1-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="86ed1-117">一月</span><span class="sxs-lookup"><span data-stu-id="86ed1-117">January</span></span>   | <span data-ttu-id="86ed1-118">0X01</span><span class="sxs-lookup"><span data-stu-id="86ed1-118">0X01</span></span>      | <span data-ttu-id="86ed1-119">1</span><span class="sxs-lookup"><span data-stu-id="86ed1-119">1</span></span>             |
| <span data-ttu-id="86ed1-120">二月</span><span class="sxs-lookup"><span data-stu-id="86ed1-120">February</span></span>  | <span data-ttu-id="86ed1-121">0x02</span><span class="sxs-lookup"><span data-stu-id="86ed1-121">0x02</span></span>      | <span data-ttu-id="86ed1-122">2</span><span class="sxs-lookup"><span data-stu-id="86ed1-122">2</span></span>             |
| <span data-ttu-id="86ed1-123">3 月</span><span class="sxs-lookup"><span data-stu-id="86ed1-123">March</span></span>     | <span data-ttu-id="86ed1-124">0X04</span><span class="sxs-lookup"><span data-stu-id="86ed1-124">0X04</span></span>      | <span data-ttu-id="86ed1-125">4</span><span class="sxs-lookup"><span data-stu-id="86ed1-125">4</span></span>             |
| <span data-ttu-id="86ed1-126">四月</span><span class="sxs-lookup"><span data-stu-id="86ed1-126">April</span></span>     | <span data-ttu-id="86ed1-127">0X08</span><span class="sxs-lookup"><span data-stu-id="86ed1-127">0X08</span></span>      | <span data-ttu-id="86ed1-128">8</span><span class="sxs-lookup"><span data-stu-id="86ed1-128">8</span></span>             |
| <span data-ttu-id="86ed1-129">五月</span><span class="sxs-lookup"><span data-stu-id="86ed1-129">May</span></span>       | <span data-ttu-id="86ed1-130">0X10</span><span class="sxs-lookup"><span data-stu-id="86ed1-130">0X10</span></span>      | <span data-ttu-id="86ed1-131">16</span><span class="sxs-lookup"><span data-stu-id="86ed1-131">16</span></span>            |
| <span data-ttu-id="86ed1-132">6 月</span><span class="sxs-lookup"><span data-stu-id="86ed1-132">June</span></span>      | <span data-ttu-id="86ed1-133">0X20</span><span class="sxs-lookup"><span data-stu-id="86ed1-133">0X20</span></span>      | <span data-ttu-id="86ed1-134">32</span><span class="sxs-lookup"><span data-stu-id="86ed1-134">32</span></span>            |
| <span data-ttu-id="86ed1-135">7 月</span><span class="sxs-lookup"><span data-stu-id="86ed1-135">July</span></span>      | <span data-ttu-id="86ed1-136">0x40</span><span class="sxs-lookup"><span data-stu-id="86ed1-136">0x40</span></span>      | <span data-ttu-id="86ed1-137">64</span><span class="sxs-lookup"><span data-stu-id="86ed1-137">64</span></span>            |
| <span data-ttu-id="86ed1-138">8 月</span><span class="sxs-lookup"><span data-stu-id="86ed1-138">August</span></span>    | <span data-ttu-id="86ed1-139">0X80</span><span class="sxs-lookup"><span data-stu-id="86ed1-139">0X80</span></span>      | <span data-ttu-id="86ed1-140">128</span><span class="sxs-lookup"><span data-stu-id="86ed1-140">128</span></span>           |
| <span data-ttu-id="86ed1-141">9 月</span><span class="sxs-lookup"><span data-stu-id="86ed1-141">September</span></span> | <span data-ttu-id="86ed1-142">0X100</span><span class="sxs-lookup"><span data-stu-id="86ed1-142">0X100</span></span>     | <span data-ttu-id="86ed1-143">256</span><span class="sxs-lookup"><span data-stu-id="86ed1-143">256</span></span>           |
| <span data-ttu-id="86ed1-144">10 月</span><span class="sxs-lookup"><span data-stu-id="86ed1-144">October</span></span>   | <span data-ttu-id="86ed1-145">0X200</span><span class="sxs-lookup"><span data-stu-id="86ed1-145">0X200</span></span>     | <span data-ttu-id="86ed1-146">512</span><span class="sxs-lookup"><span data-stu-id="86ed1-146">512</span></span>           |
| <span data-ttu-id="86ed1-147">11 月</span><span class="sxs-lookup"><span data-stu-id="86ed1-147">November</span></span>  | <span data-ttu-id="86ed1-148">0X400</span><span class="sxs-lookup"><span data-stu-id="86ed1-148">0X400</span></span>     | <span data-ttu-id="86ed1-149">1024</span><span class="sxs-lookup"><span data-stu-id="86ed1-149">1024</span></span>          |
| <span data-ttu-id="86ed1-150">12 月</span><span class="sxs-lookup"><span data-stu-id="86ed1-150">December</span></span>  | <span data-ttu-id="86ed1-151">0X800</span><span class="sxs-lookup"><span data-stu-id="86ed1-151">0X800</span></span>     | <span data-ttu-id="86ed1-152">2048</span><span class="sxs-lookup"><span data-stu-id="86ed1-152">2048</span></span>          |



 

<span data-ttu-id="86ed1-153">在讀取或寫入工作的 XML 時，每月的每月星期幾日曆中的月份是由工作排程器架構的 [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) 元素所指定。</span><span class="sxs-lookup"><span data-stu-id="86ed1-153">When reading or writing XML for a task, the months of the year of a monthly day-of-week calendar are specified by the [**Months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="86ed1-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="86ed1-154">Requirements</span></span>



| <span data-ttu-id="86ed1-155">需求</span><span class="sxs-lookup"><span data-stu-id="86ed1-155">Requirement</span></span> | <span data-ttu-id="86ed1-156">值</span><span class="sxs-lookup"><span data-stu-id="86ed1-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86ed1-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86ed1-157">Minimum supported client</span></span><br/> | <span data-ttu-id="86ed1-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86ed1-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="86ed1-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86ed1-159">Minimum supported server</span></span><br/> | <span data-ttu-id="86ed1-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86ed1-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86ed1-161">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="86ed1-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="86ed1-162"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86ed1-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86ed1-163">DLL</span><span class="sxs-lookup"><span data-stu-id="86ed1-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86ed1-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86ed1-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ed1-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86ed1-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ed1-166">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="86ed1-166">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="86ed1-167">工作排程器</span><span class="sxs-lookup"><span data-stu-id="86ed1-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





