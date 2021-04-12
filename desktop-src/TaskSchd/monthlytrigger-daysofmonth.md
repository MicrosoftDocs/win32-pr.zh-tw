---
title: MonthlyTrigger. DaysOfMonth 屬性
description: 針對腳本，取得或設定工作執行的月份天數。
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- DaysOfMonth 屬性工作排程器
- DaysOfMonth 屬性工作排程器，MonthlyTrigger 物件
- MonthlyTrigger 物件工作排程器、DaysOfMonth 屬性
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104358"
---
# <a name="monthlytriggerdaysofmonth-property"></a><span data-ttu-id="22ce1-106">MonthlyTrigger. DaysOfMonth 屬性</span><span class="sxs-lookup"><span data-stu-id="22ce1-106">MonthlyTrigger.DaysOfMonth property</span></span>

<span data-ttu-id="22ce1-107">針對腳本，取得或設定工作執行的月份天數。</span><span class="sxs-lookup"><span data-stu-id="22ce1-107">For scripting, gets or sets the days of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ce1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="22ce1-108">Syntax</span></span>


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a><span data-ttu-id="22ce1-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="22ce1-109">Property value</span></span>

<span data-ttu-id="22ce1-110">位元遮罩，表示工作執行的當月天數。</span><span class="sxs-lookup"><span data-stu-id="22ce1-110">A bitwise mask that indicates the days of the month during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="22ce1-111">備註</span><span class="sxs-lookup"><span data-stu-id="22ce1-111">Remarks</span></span>



| <span data-ttu-id="22ce1-112">月中的日</span><span class="sxs-lookup"><span data-stu-id="22ce1-112">Day of month</span></span> | <span data-ttu-id="22ce1-113">十六進位值</span><span class="sxs-lookup"><span data-stu-id="22ce1-113">Hex value</span></span>  | <span data-ttu-id="22ce1-114">十進位值</span><span class="sxs-lookup"><span data-stu-id="22ce1-114">Decimal value</span></span> |
|--------------|------------|---------------|
| <span data-ttu-id="22ce1-115">1</span><span class="sxs-lookup"><span data-stu-id="22ce1-115">1</span></span>            | <span data-ttu-id="22ce1-116">0x01</span><span class="sxs-lookup"><span data-stu-id="22ce1-116">0x01</span></span>       | <span data-ttu-id="22ce1-117">1</span><span class="sxs-lookup"><span data-stu-id="22ce1-117">1</span></span>             |
| <span data-ttu-id="22ce1-118">2</span><span class="sxs-lookup"><span data-stu-id="22ce1-118">2</span></span>            | <span data-ttu-id="22ce1-119">0x02</span><span class="sxs-lookup"><span data-stu-id="22ce1-119">0x02</span></span>       | <span data-ttu-id="22ce1-120">2</span><span class="sxs-lookup"><span data-stu-id="22ce1-120">2</span></span>             |
| <span data-ttu-id="22ce1-121">3</span><span class="sxs-lookup"><span data-stu-id="22ce1-121">3</span></span>            | <span data-ttu-id="22ce1-122">0x04</span><span class="sxs-lookup"><span data-stu-id="22ce1-122">0x04</span></span>       | <span data-ttu-id="22ce1-123">4</span><span class="sxs-lookup"><span data-stu-id="22ce1-123">4</span></span>             |
| <span data-ttu-id="22ce1-124">4</span><span class="sxs-lookup"><span data-stu-id="22ce1-124">4</span></span>            | <span data-ttu-id="22ce1-125">0x08</span><span class="sxs-lookup"><span data-stu-id="22ce1-125">0x08</span></span>       | <span data-ttu-id="22ce1-126">8</span><span class="sxs-lookup"><span data-stu-id="22ce1-126">8</span></span>             |
| <span data-ttu-id="22ce1-127">5</span><span class="sxs-lookup"><span data-stu-id="22ce1-127">5</span></span>            | <span data-ttu-id="22ce1-128">0x10</span><span class="sxs-lookup"><span data-stu-id="22ce1-128">0x10</span></span>       | <span data-ttu-id="22ce1-129">16</span><span class="sxs-lookup"><span data-stu-id="22ce1-129">16</span></span>            |
| <span data-ttu-id="22ce1-130">6</span><span class="sxs-lookup"><span data-stu-id="22ce1-130">6</span></span>            | <span data-ttu-id="22ce1-131">0x20</span><span class="sxs-lookup"><span data-stu-id="22ce1-131">0x20</span></span>       | <span data-ttu-id="22ce1-132">32</span><span class="sxs-lookup"><span data-stu-id="22ce1-132">32</span></span>            |
| <span data-ttu-id="22ce1-133">7</span><span class="sxs-lookup"><span data-stu-id="22ce1-133">7</span></span>            | <span data-ttu-id="22ce1-134">0x40</span><span class="sxs-lookup"><span data-stu-id="22ce1-134">0x40</span></span>       | <span data-ttu-id="22ce1-135">64</span><span class="sxs-lookup"><span data-stu-id="22ce1-135">64</span></span>            |
| <span data-ttu-id="22ce1-136">8</span><span class="sxs-lookup"><span data-stu-id="22ce1-136">8</span></span>            | <span data-ttu-id="22ce1-137">0x80</span><span class="sxs-lookup"><span data-stu-id="22ce1-137">0x80</span></span>       | <span data-ttu-id="22ce1-138">128</span><span class="sxs-lookup"><span data-stu-id="22ce1-138">128</span></span>           |
| <span data-ttu-id="22ce1-139">9</span><span class="sxs-lookup"><span data-stu-id="22ce1-139">9</span></span>            | <span data-ttu-id="22ce1-140">0x100</span><span class="sxs-lookup"><span data-stu-id="22ce1-140">0x100</span></span>      | <span data-ttu-id="22ce1-141">256</span><span class="sxs-lookup"><span data-stu-id="22ce1-141">256</span></span>           |
| <span data-ttu-id="22ce1-142">10</span><span class="sxs-lookup"><span data-stu-id="22ce1-142">10</span></span>           | <span data-ttu-id="22ce1-143">0x200</span><span class="sxs-lookup"><span data-stu-id="22ce1-143">0x200</span></span>      | <span data-ttu-id="22ce1-144">512</span><span class="sxs-lookup"><span data-stu-id="22ce1-144">512</span></span>           |
| <span data-ttu-id="22ce1-145">11</span><span class="sxs-lookup"><span data-stu-id="22ce1-145">11</span></span>           | <span data-ttu-id="22ce1-146">0x400</span><span class="sxs-lookup"><span data-stu-id="22ce1-146">0x400</span></span>      | <span data-ttu-id="22ce1-147">1024</span><span class="sxs-lookup"><span data-stu-id="22ce1-147">1024</span></span>          |
| <span data-ttu-id="22ce1-148">12</span><span class="sxs-lookup"><span data-stu-id="22ce1-148">12</span></span>           | <span data-ttu-id="22ce1-149">0x800</span><span class="sxs-lookup"><span data-stu-id="22ce1-149">0x800</span></span>      | <span data-ttu-id="22ce1-150">2048</span><span class="sxs-lookup"><span data-stu-id="22ce1-150">2048</span></span>          |
| <span data-ttu-id="22ce1-151">13</span><span class="sxs-lookup"><span data-stu-id="22ce1-151">13</span></span>           | <span data-ttu-id="22ce1-152">0x1000</span><span class="sxs-lookup"><span data-stu-id="22ce1-152">0x1000</span></span>     | <span data-ttu-id="22ce1-153">4096</span><span class="sxs-lookup"><span data-stu-id="22ce1-153">4096</span></span>          |
| <span data-ttu-id="22ce1-154">14</span><span class="sxs-lookup"><span data-stu-id="22ce1-154">14</span></span>           | <span data-ttu-id="22ce1-155">0x2000</span><span class="sxs-lookup"><span data-stu-id="22ce1-155">0x2000</span></span>     | <span data-ttu-id="22ce1-156">8192</span><span class="sxs-lookup"><span data-stu-id="22ce1-156">8192</span></span>          |
| <span data-ttu-id="22ce1-157">15</span><span class="sxs-lookup"><span data-stu-id="22ce1-157">15</span></span>           | <span data-ttu-id="22ce1-158">0x4000</span><span class="sxs-lookup"><span data-stu-id="22ce1-158">0x4000</span></span>     | <span data-ttu-id="22ce1-159">16384</span><span class="sxs-lookup"><span data-stu-id="22ce1-159">16384</span></span>         |
| <span data-ttu-id="22ce1-160">16</span><span class="sxs-lookup"><span data-stu-id="22ce1-160">16</span></span>           | <span data-ttu-id="22ce1-161">0x8000</span><span class="sxs-lookup"><span data-stu-id="22ce1-161">0x8000</span></span>     | <span data-ttu-id="22ce1-162">32768</span><span class="sxs-lookup"><span data-stu-id="22ce1-162">32768</span></span>         |
| <span data-ttu-id="22ce1-163">17</span><span class="sxs-lookup"><span data-stu-id="22ce1-163">17</span></span>           | <span data-ttu-id="22ce1-164">0x10000</span><span class="sxs-lookup"><span data-stu-id="22ce1-164">0x10000</span></span>    | <span data-ttu-id="22ce1-165">65536</span><span class="sxs-lookup"><span data-stu-id="22ce1-165">65536</span></span>         |
| <span data-ttu-id="22ce1-166">18</span><span class="sxs-lookup"><span data-stu-id="22ce1-166">18</span></span>           | <span data-ttu-id="22ce1-167">0x20000</span><span class="sxs-lookup"><span data-stu-id="22ce1-167">0x20000</span></span>    | <span data-ttu-id="22ce1-168">131072</span><span class="sxs-lookup"><span data-stu-id="22ce1-168">131072</span></span>        |
| <span data-ttu-id="22ce1-169">19</span><span class="sxs-lookup"><span data-stu-id="22ce1-169">19</span></span>           | <span data-ttu-id="22ce1-170">0x40000</span><span class="sxs-lookup"><span data-stu-id="22ce1-170">0x40000</span></span>    | <span data-ttu-id="22ce1-171">262144</span><span class="sxs-lookup"><span data-stu-id="22ce1-171">262144</span></span>        |
| <span data-ttu-id="22ce1-172">20</span><span class="sxs-lookup"><span data-stu-id="22ce1-172">20</span></span>           | <span data-ttu-id="22ce1-173">0x80000</span><span class="sxs-lookup"><span data-stu-id="22ce1-173">0x80000</span></span>    | <span data-ttu-id="22ce1-174">524288</span><span class="sxs-lookup"><span data-stu-id="22ce1-174">524288</span></span>        |
| <span data-ttu-id="22ce1-175">21</span><span class="sxs-lookup"><span data-stu-id="22ce1-175">21</span></span>           | <span data-ttu-id="22ce1-176">0x100000</span><span class="sxs-lookup"><span data-stu-id="22ce1-176">0x100000</span></span>   | <span data-ttu-id="22ce1-177">1048576</span><span class="sxs-lookup"><span data-stu-id="22ce1-177">1048576</span></span>       |
| <span data-ttu-id="22ce1-178">22</span><span class="sxs-lookup"><span data-stu-id="22ce1-178">22</span></span>           | <span data-ttu-id="22ce1-179">0x200000</span><span class="sxs-lookup"><span data-stu-id="22ce1-179">0x200000</span></span>   | <span data-ttu-id="22ce1-180">2097152</span><span class="sxs-lookup"><span data-stu-id="22ce1-180">2097152</span></span>       |
| <span data-ttu-id="22ce1-181">23</span><span class="sxs-lookup"><span data-stu-id="22ce1-181">23</span></span>           | <span data-ttu-id="22ce1-182">0x400000</span><span class="sxs-lookup"><span data-stu-id="22ce1-182">0x400000</span></span>   | <span data-ttu-id="22ce1-183">4194304</span><span class="sxs-lookup"><span data-stu-id="22ce1-183">4194304</span></span>       |
| <span data-ttu-id="22ce1-184">24</span><span class="sxs-lookup"><span data-stu-id="22ce1-184">24</span></span>           | <span data-ttu-id="22ce1-185">0x800000</span><span class="sxs-lookup"><span data-stu-id="22ce1-185">0x800000</span></span>   | <span data-ttu-id="22ce1-186">8388608</span><span class="sxs-lookup"><span data-stu-id="22ce1-186">8388608</span></span>       |
| <span data-ttu-id="22ce1-187">25</span><span class="sxs-lookup"><span data-stu-id="22ce1-187">25</span></span>           | <span data-ttu-id="22ce1-188">0x1000000</span><span class="sxs-lookup"><span data-stu-id="22ce1-188">0x1000000</span></span>  | <span data-ttu-id="22ce1-189">16777216</span><span class="sxs-lookup"><span data-stu-id="22ce1-189">16777216</span></span>      |
| <span data-ttu-id="22ce1-190">26</span><span class="sxs-lookup"><span data-stu-id="22ce1-190">26</span></span>           | <span data-ttu-id="22ce1-191">0x2000000</span><span class="sxs-lookup"><span data-stu-id="22ce1-191">0x2000000</span></span>  | <span data-ttu-id="22ce1-192">33554432</span><span class="sxs-lookup"><span data-stu-id="22ce1-192">33554432</span></span>      |
| <span data-ttu-id="22ce1-193">27</span><span class="sxs-lookup"><span data-stu-id="22ce1-193">27</span></span>           | <span data-ttu-id="22ce1-194">0x4000000</span><span class="sxs-lookup"><span data-stu-id="22ce1-194">0x4000000</span></span>  | <span data-ttu-id="22ce1-195">67108864</span><span class="sxs-lookup"><span data-stu-id="22ce1-195">67108864</span></span>      |
| <span data-ttu-id="22ce1-196">28</span><span class="sxs-lookup"><span data-stu-id="22ce1-196">28</span></span>           | <span data-ttu-id="22ce1-197">0x8000000</span><span class="sxs-lookup"><span data-stu-id="22ce1-197">0x8000000</span></span>  | <span data-ttu-id="22ce1-198">134217728</span><span class="sxs-lookup"><span data-stu-id="22ce1-198">134217728</span></span>     |
| <span data-ttu-id="22ce1-199">29</span><span class="sxs-lookup"><span data-stu-id="22ce1-199">29</span></span>           | <span data-ttu-id="22ce1-200">0x10000000</span><span class="sxs-lookup"><span data-stu-id="22ce1-200">0x10000000</span></span> | <span data-ttu-id="22ce1-201">268435456</span><span class="sxs-lookup"><span data-stu-id="22ce1-201">268435456</span></span>     |
| <span data-ttu-id="22ce1-202">30</span><span class="sxs-lookup"><span data-stu-id="22ce1-202">30</span></span>           | <span data-ttu-id="22ce1-203">0x20000000</span><span class="sxs-lookup"><span data-stu-id="22ce1-203">0x20000000</span></span> | <span data-ttu-id="22ce1-204">536870912</span><span class="sxs-lookup"><span data-stu-id="22ce1-204">536870912</span></span>     |
| <span data-ttu-id="22ce1-205">31</span><span class="sxs-lookup"><span data-stu-id="22ce1-205">31</span></span>           | <span data-ttu-id="22ce1-206">0x40000000</span><span class="sxs-lookup"><span data-stu-id="22ce1-206">0x40000000</span></span> | <span data-ttu-id="22ce1-207">1073741824</span><span class="sxs-lookup"><span data-stu-id="22ce1-207">1073741824</span></span>    |
| <span data-ttu-id="22ce1-208">最後一個</span><span class="sxs-lookup"><span data-stu-id="22ce1-208">Last</span></span>         | <span data-ttu-id="22ce1-209">0x80000000</span><span class="sxs-lookup"><span data-stu-id="22ce1-209">0x80000000</span></span> | <span data-ttu-id="22ce1-210">2147483648</span><span class="sxs-lookup"><span data-stu-id="22ce1-210">2147483648</span></span>    |



 

<span data-ttu-id="22ce1-211">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) 元素來指定月份的日期。</span><span class="sxs-lookup"><span data-stu-id="22ce1-211">When reading or writing your own XML for a task, the days of the month are specified using the [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="22ce1-212">規格需求</span><span class="sxs-lookup"><span data-stu-id="22ce1-212">Requirements</span></span>



| <span data-ttu-id="22ce1-213">需求</span><span class="sxs-lookup"><span data-stu-id="22ce1-213">Requirement</span></span> | <span data-ttu-id="22ce1-214">值</span><span class="sxs-lookup"><span data-stu-id="22ce1-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22ce1-215">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22ce1-215">Minimum supported client</span></span><br/> | <span data-ttu-id="22ce1-216">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22ce1-216">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="22ce1-217">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22ce1-217">Minimum supported server</span></span><br/> | <span data-ttu-id="22ce1-218">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22ce1-218">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22ce1-219">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="22ce1-219">Type library</span></span><br/>             | <dl> <span data-ttu-id="22ce1-220"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="22ce1-220"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="22ce1-221">DLL</span><span class="sxs-lookup"><span data-stu-id="22ce1-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22ce1-222"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22ce1-222"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22ce1-223">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22ce1-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ce1-224">工作排程器</span><span class="sxs-lookup"><span data-stu-id="22ce1-224">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="22ce1-225">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="22ce1-225">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





