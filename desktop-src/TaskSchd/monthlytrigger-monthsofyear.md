---
title: MonthlyTrigger. MonthsOfYear 屬性
description: 針對腳本，取得或設定工作在一年中執行的月份。 |MonthlyTrigger. MonthsOfYear 屬性
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- MonthsOfYear 屬性工作排程器
- MonthsOfYear 屬性工作排程器，MonthlyTrigger 物件
- MonthlyTrigger 物件工作排程器、MonthsOfYear 屬性
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5683fb1c85e470ca7c82b069929de0351ea7cffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853763"
---
# <a name="monthlytriggermonthsofyear-property"></a><span data-ttu-id="ac8cc-107">MonthlyTrigger. MonthsOfYear 屬性</span><span class="sxs-lookup"><span data-stu-id="ac8cc-107">MonthlyTrigger.MonthsOfYear property</span></span>

<span data-ttu-id="ac8cc-108">針對腳本，取得或設定工作在一年中執行的月份。</span><span class="sxs-lookup"><span data-stu-id="ac8cc-108">For scripting, gets or sets the months of the year during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac8cc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac8cc-109">Syntax</span></span>


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a><span data-ttu-id="ac8cc-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ac8cc-110">Property value</span></span>

<span data-ttu-id="ac8cc-111">位元遮罩，表示工作執行的年中月份。</span><span class="sxs-lookup"><span data-stu-id="ac8cc-111">A bitwise mask that indicates the months of the year during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac8cc-112">備註</span><span class="sxs-lookup"><span data-stu-id="ac8cc-112">Remarks</span></span>

<span data-ttu-id="ac8cc-113">下表顯示這個屬性所使用之位元遮罩的對應。</span><span class="sxs-lookup"><span data-stu-id="ac8cc-113">The following table shows the mapping of the bitwise mask that is used by this property.</span></span>



| <span data-ttu-id="ac8cc-114">Month</span><span class="sxs-lookup"><span data-stu-id="ac8cc-114">Month</span></span>     | <span data-ttu-id="ac8cc-115">十六進位值</span><span class="sxs-lookup"><span data-stu-id="ac8cc-115">Hex value</span></span> | <span data-ttu-id="ac8cc-116">十進位值</span><span class="sxs-lookup"><span data-stu-id="ac8cc-116">Decimal value</span></span> |
|-----------|-----------|---------------|
| <span data-ttu-id="ac8cc-117">一月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-117">January</span></span>   | <span data-ttu-id="ac8cc-118">0X01</span><span class="sxs-lookup"><span data-stu-id="ac8cc-118">0X01</span></span>      | <span data-ttu-id="ac8cc-119">1</span><span class="sxs-lookup"><span data-stu-id="ac8cc-119">1</span></span>             |
| <span data-ttu-id="ac8cc-120">二月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-120">February</span></span>  | <span data-ttu-id="ac8cc-121">0x02</span><span class="sxs-lookup"><span data-stu-id="ac8cc-121">0x02</span></span>      | <span data-ttu-id="ac8cc-122">2</span><span class="sxs-lookup"><span data-stu-id="ac8cc-122">2</span></span>             |
| <span data-ttu-id="ac8cc-123">3 月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-123">March</span></span>     | <span data-ttu-id="ac8cc-124">0X04</span><span class="sxs-lookup"><span data-stu-id="ac8cc-124">0X04</span></span>      | <span data-ttu-id="ac8cc-125">4</span><span class="sxs-lookup"><span data-stu-id="ac8cc-125">4</span></span>             |
| <span data-ttu-id="ac8cc-126">四月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-126">April</span></span>     | <span data-ttu-id="ac8cc-127">0X08</span><span class="sxs-lookup"><span data-stu-id="ac8cc-127">0X08</span></span>      | <span data-ttu-id="ac8cc-128">8</span><span class="sxs-lookup"><span data-stu-id="ac8cc-128">8</span></span>             |
| <span data-ttu-id="ac8cc-129">五月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-129">May</span></span>       | <span data-ttu-id="ac8cc-130">0X10</span><span class="sxs-lookup"><span data-stu-id="ac8cc-130">0X10</span></span>      | <span data-ttu-id="ac8cc-131">16</span><span class="sxs-lookup"><span data-stu-id="ac8cc-131">16</span></span>            |
| <span data-ttu-id="ac8cc-132">6 月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-132">June</span></span>      | <span data-ttu-id="ac8cc-133">0X20</span><span class="sxs-lookup"><span data-stu-id="ac8cc-133">0X20</span></span>      | <span data-ttu-id="ac8cc-134">32</span><span class="sxs-lookup"><span data-stu-id="ac8cc-134">32</span></span>            |
| <span data-ttu-id="ac8cc-135">7 月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-135">July</span></span>      | <span data-ttu-id="ac8cc-136">0x40</span><span class="sxs-lookup"><span data-stu-id="ac8cc-136">0x40</span></span>      | <span data-ttu-id="ac8cc-137">64</span><span class="sxs-lookup"><span data-stu-id="ac8cc-137">64</span></span>            |
| <span data-ttu-id="ac8cc-138">8 月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-138">August</span></span>    | <span data-ttu-id="ac8cc-139">0X80</span><span class="sxs-lookup"><span data-stu-id="ac8cc-139">0X80</span></span>      | <span data-ttu-id="ac8cc-140">128</span><span class="sxs-lookup"><span data-stu-id="ac8cc-140">128</span></span>           |
| <span data-ttu-id="ac8cc-141">9 月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-141">September</span></span> | <span data-ttu-id="ac8cc-142">0X100</span><span class="sxs-lookup"><span data-stu-id="ac8cc-142">0X100</span></span>     | <span data-ttu-id="ac8cc-143">256</span><span class="sxs-lookup"><span data-stu-id="ac8cc-143">256</span></span>           |
| <span data-ttu-id="ac8cc-144">10 月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-144">October</span></span>   | <span data-ttu-id="ac8cc-145">0X200</span><span class="sxs-lookup"><span data-stu-id="ac8cc-145">0X200</span></span>     | <span data-ttu-id="ac8cc-146">512</span><span class="sxs-lookup"><span data-stu-id="ac8cc-146">512</span></span>           |
| <span data-ttu-id="ac8cc-147">11 月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-147">November</span></span>  | <span data-ttu-id="ac8cc-148">0X400</span><span class="sxs-lookup"><span data-stu-id="ac8cc-148">0X400</span></span>     | <span data-ttu-id="ac8cc-149">1024</span><span class="sxs-lookup"><span data-stu-id="ac8cc-149">1024</span></span>          |
| <span data-ttu-id="ac8cc-150">12 月</span><span class="sxs-lookup"><span data-stu-id="ac8cc-150">December</span></span>  | <span data-ttu-id="ac8cc-151">0X800</span><span class="sxs-lookup"><span data-stu-id="ac8cc-151">0X800</span></span>     | <span data-ttu-id="ac8cc-152">2048</span><span class="sxs-lookup"><span data-stu-id="ac8cc-152">2048</span></span>          |



 

<span data-ttu-id="ac8cc-153">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**months**](taskschedulerschema-months-monthlyscheduletype-element.md) 元素來指定年份的月份。</span><span class="sxs-lookup"><span data-stu-id="ac8cc-153">When reading or writing your own XML for a task, the months of the year are specified using the [**Months**](taskschedulerschema-months-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac8cc-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac8cc-154">Requirements</span></span>



| <span data-ttu-id="ac8cc-155">需求</span><span class="sxs-lookup"><span data-stu-id="ac8cc-155">Requirement</span></span> | <span data-ttu-id="ac8cc-156">值</span><span class="sxs-lookup"><span data-stu-id="ac8cc-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8cc-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac8cc-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ac8cc-158">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac8cc-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ac8cc-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac8cc-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ac8cc-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac8cc-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac8cc-161">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ac8cc-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="ac8cc-162"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ac8cc-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ac8cc-163">DLL</span><span class="sxs-lookup"><span data-stu-id="ac8cc-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac8cc-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac8cc-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac8cc-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac8cc-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac8cc-166">工作排程器</span><span class="sxs-lookup"><span data-stu-id="ac8cc-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="ac8cc-167">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="ac8cc-167">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





