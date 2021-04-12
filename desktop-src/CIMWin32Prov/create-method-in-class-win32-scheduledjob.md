---
description: 將作業提交至作業系統，以在未來指定的時間和日期執行。
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Win32_ScheduledJob 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317916"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="771a1-103">Win32 Register-scheduledjob 類別的 Create 方法 \_</span><span class="sxs-lookup"><span data-stu-id="771a1-103">Create method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="771a1-104">**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將作業提交至作業系統，以在未來指定的時間和日期執行。</span><span class="sxs-lookup"><span data-stu-id="771a1-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method submits a job to an operating system for execution at a specified time and date in the future.</span></span> <span data-ttu-id="771a1-105">此方法需要在提交作業的電腦上啟動排程服務。</span><span class="sxs-lookup"><span data-stu-id="771a1-105">This method requires that the schedule service be started on the computer to which the job is submitted.</span></span>

<span data-ttu-id="771a1-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="771a1-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="771a1-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="771a1-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="771a1-108">語法</span><span class="sxs-lookup"><span data-stu-id="771a1-108">Syntax</span></span>


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a><span data-ttu-id="771a1-109">參數</span><span class="sxs-lookup"><span data-stu-id="771a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="771a1-110">*命令* \[在\]</span><span class="sxs-lookup"><span data-stu-id="771a1-110">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771a1-111">排程服務用來叫用作業的命令、批次程式或二進位檔和命令列參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="771a1-111">Name of the command, batch program, or binary file and command-line parameters that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="771a1-112">範例： "defrag/q/f"。</span><span class="sxs-lookup"><span data-stu-id="771a1-112">Example: "defrag /q /f".</span></span>

</dd> <dt>

<span data-ttu-id="771a1-113">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="771a1-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771a1-114">國際標準時間 (UTC) 時間來執行工作。</span><span class="sxs-lookup"><span data-stu-id="771a1-114">Coordinated Universal Time (UTC) time to run a job.</span></span> <span data-ttu-id="771a1-115">格式必須為： "YYYYMMDDHHMMSS.FFFFFF"。MMMMMM (+-) OOO "，其中" YYYYMMDD "必須以" "取代 \* \* \* \* \* \* \* \* 。</span><span class="sxs-lookup"><span data-stu-id="771a1-115">The form must be: "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="771a1-116">例如： " \* \* \* \* \* \* \* \* 143000.000000-420" 會指定 14.30 (2:30 P.M. ) PST，並有日光節約時間生效。</span><span class="sxs-lookup"><span data-stu-id="771a1-116">For example: "\*\*\*\*\*\*\*\*143000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

<span data-ttu-id="771a1-117">StartTime 屬性值的 " (+-) OOO" 區段是本地時間轉譯目前的偏差。</span><span class="sxs-lookup"><span data-stu-id="771a1-117">The "(+-)OOO" section of the StartTime property value is the current bias for local time translation.</span></span> <span data-ttu-id="771a1-118">偏差是 UTC 時間與當地時間之間的差異。</span><span class="sxs-lookup"><span data-stu-id="771a1-118">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="771a1-119">若要計算時區的偏差，請將您時區提前或晚于格林威治標準時間的小時數乘以60的 (GMT)  (如果您的時區是在 GMT 之前，則以小時為單位，如果您的時區晚于 gmt) ，則為負數。</span><span class="sxs-lookup"><span data-stu-id="771a1-119">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="771a1-120">如果您的時區使用日光節約時間，請在您的計算中加入額外的60。</span><span class="sxs-lookup"><span data-stu-id="771a1-120">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="771a1-121">例如，太平洋標準時區是 GMT 後八小時，因此偏差等於-420 (-8 \* 60 + 60) 當日光節約時間正在使用中時，當日光節約時間未使用時，則為-480 (-8 \* 60) 。</span><span class="sxs-lookup"><span data-stu-id="771a1-121">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="771a1-122">您也可以藉由查詢 [**Win32 \_ 時區**](win32-timezone.md) 類別的偏差屬性來判斷偏差的值。</span><span class="sxs-lookup"><span data-stu-id="771a1-122">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-123">*RunRepeatedly* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="771a1-123">*RunRepeatedly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="771a1-124">若 **為 True**，則排程工作會在特定天數重複執行。</span><span class="sxs-lookup"><span data-stu-id="771a1-124">If **True**, a scheduled job runs repeatedly on specific days.</span></span> <span data-ttu-id="771a1-125">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="771a1-125">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-126">*DaysOfWeek* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="771a1-126">*DaysOfWeek* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="771a1-127">排程執行工作的周間天數;只有在 *RunRepeatedly* 參數為 **True** 時才會使用。</span><span class="sxs-lookup"><span data-stu-id="771a1-127">Days of the week when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span> <span data-ttu-id="771a1-128">若要排定一周中超過一天的作業，請在邏輯 OR 中聯結適當的值。</span><span class="sxs-lookup"><span data-stu-id="771a1-128">To schedule a job for more than one day of the week, join the appropriate values in a logical OR.</span></span> <span data-ttu-id="771a1-129">例如，若要針對星期二和星期五排程作業， *DaysOfWeek* 的值為2或16。</span><span class="sxs-lookup"><span data-stu-id="771a1-129">For example, to schedule a job for Tuesdays and Fridays, the value of *DaysOfWeek* are 2 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="771a1-130">**星期一** (1) </span><span class="sxs-lookup"><span data-stu-id="771a1-130">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="771a1-131">**星期二** (2) </span><span class="sxs-lookup"><span data-stu-id="771a1-131">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="771a1-132">**星期三** (4) </span><span class="sxs-lookup"><span data-stu-id="771a1-132">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="771a1-133">**星期四** (8) </span><span class="sxs-lookup"><span data-stu-id="771a1-133">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="771a1-134">**星期五** (16) </span><span class="sxs-lookup"><span data-stu-id="771a1-134">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="771a1-135">**星期六** (32) </span><span class="sxs-lookup"><span data-stu-id="771a1-135">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="771a1-136">**星期日** (64) </span><span class="sxs-lookup"><span data-stu-id="771a1-136">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="771a1-137">*DaysOfMonth* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="771a1-137">*DaysOfMonth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="771a1-138">排程執行作業的當月天數;只有在 *RunRepeatedly* 參數為 **True** 時才會使用。</span><span class="sxs-lookup"><span data-stu-id="771a1-138">Days of the month when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="771a1-139"><span id="1"></span>**1** (1) </span><span class="sxs-lookup"><span data-stu-id="771a1-139"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-140">每月第1天</span><span class="sxs-lookup"><span data-stu-id="771a1-140">Day 1 of a month</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="771a1-141"><span id="2"></span>**2** (2) </span><span class="sxs-lookup"><span data-stu-id="771a1-141"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-142">每月第2天</span><span class="sxs-lookup"><span data-stu-id="771a1-142">Day 2 of a month</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="771a1-143"><span id="3"></span>**3** (4) </span><span class="sxs-lookup"><span data-stu-id="771a1-143"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-144">每月第3天</span><span class="sxs-lookup"><span data-stu-id="771a1-144">Day 3 of a month</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="771a1-145"><span id="4"></span>**4** (8) </span><span class="sxs-lookup"><span data-stu-id="771a1-145"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-146">每月第4天</span><span class="sxs-lookup"><span data-stu-id="771a1-146">Day 4 of a month</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="771a1-147"><span id="5"></span>**5** (16) </span><span class="sxs-lookup"><span data-stu-id="771a1-147"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-148">每月第5天</span><span class="sxs-lookup"><span data-stu-id="771a1-148">Day 5 of a month</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="771a1-149"><span id="6"></span>**6** (32) </span><span class="sxs-lookup"><span data-stu-id="771a1-149"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-150">每月第6天</span><span class="sxs-lookup"><span data-stu-id="771a1-150">Day 6 of a month</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="771a1-151"><span id="7"></span>**7** (64) </span><span class="sxs-lookup"><span data-stu-id="771a1-151"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-152">月7日</span><span class="sxs-lookup"><span data-stu-id="771a1-152">Day 7 of a month</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="771a1-153"><span id="8"></span>**8** (128) </span><span class="sxs-lookup"><span data-stu-id="771a1-153"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-154">每月第8天</span><span class="sxs-lookup"><span data-stu-id="771a1-154">Day 8 of a month</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="771a1-155"><span id="9"></span>**9** (256) </span><span class="sxs-lookup"><span data-stu-id="771a1-155"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-156">每月第9天</span><span class="sxs-lookup"><span data-stu-id="771a1-156">Day 9 of a month</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="771a1-157"><span id="10"></span>**10** (512) </span><span class="sxs-lookup"><span data-stu-id="771a1-157"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-158">每月第10天</span><span class="sxs-lookup"><span data-stu-id="771a1-158">Day 10 of a month</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="771a1-159"><span id="11"></span>**11** (1024) </span><span class="sxs-lookup"><span data-stu-id="771a1-159"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-160">每月第11天</span><span class="sxs-lookup"><span data-stu-id="771a1-160">Day 11 of a month</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="771a1-161"><span id="12"></span>**12** (2048) </span><span class="sxs-lookup"><span data-stu-id="771a1-161"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-162">每月第12天</span><span class="sxs-lookup"><span data-stu-id="771a1-162">Day 12 of a month</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="771a1-163"><span id="13"></span>**13** (4096) </span><span class="sxs-lookup"><span data-stu-id="771a1-163"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-164">每月第13天</span><span class="sxs-lookup"><span data-stu-id="771a1-164">Day 13 of a month</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="771a1-165"><span id="14"></span>**14** (8192) </span><span class="sxs-lookup"><span data-stu-id="771a1-165"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-166">月14日</span><span class="sxs-lookup"><span data-stu-id="771a1-166">Day 14 of a month</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="771a1-167"><span id="15"></span>**15** (16384) </span><span class="sxs-lookup"><span data-stu-id="771a1-167"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-168">月15日</span><span class="sxs-lookup"><span data-stu-id="771a1-168">Day 15 of a month</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="771a1-169"><span id="16"></span>**16** (32768) </span><span class="sxs-lookup"><span data-stu-id="771a1-169"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-170">每月第16天</span><span class="sxs-lookup"><span data-stu-id="771a1-170">Day 16 of a month</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="771a1-171"><span id="17"></span>**17** (65536) </span><span class="sxs-lookup"><span data-stu-id="771a1-171"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-172">每月17日</span><span class="sxs-lookup"><span data-stu-id="771a1-172">Day 17 of a month</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="771a1-173"><span id="18"></span>**18** (131072) </span><span class="sxs-lookup"><span data-stu-id="771a1-173"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-174">每月18日</span><span class="sxs-lookup"><span data-stu-id="771a1-174">Day 18 of a month</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="771a1-175"><span id="19"></span>**19** (262144) </span><span class="sxs-lookup"><span data-stu-id="771a1-175"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-176">月19日</span><span class="sxs-lookup"><span data-stu-id="771a1-176">Day 19 of a month</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="771a1-177"><span id="20"></span>**20** (524288) </span><span class="sxs-lookup"><span data-stu-id="771a1-177"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-178">每月第20天</span><span class="sxs-lookup"><span data-stu-id="771a1-178">Day 20 of a month</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="771a1-179"><span id="21"></span>**21** (1048576) </span><span class="sxs-lookup"><span data-stu-id="771a1-179"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-180">每月21日</span><span class="sxs-lookup"><span data-stu-id="771a1-180">Day 21 of a month</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="771a1-181"><span id="22"></span>**22** (2097152) </span><span class="sxs-lookup"><span data-stu-id="771a1-181"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-182">每月第22天</span><span class="sxs-lookup"><span data-stu-id="771a1-182">Day 22 of a month</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="771a1-183"><span id="23"></span>**23** (4194304) </span><span class="sxs-lookup"><span data-stu-id="771a1-183"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-184">每月23日</span><span class="sxs-lookup"><span data-stu-id="771a1-184">Day 23 of a month</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="771a1-185"><span id="24"></span>**24** (8388608) </span><span class="sxs-lookup"><span data-stu-id="771a1-185"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-186">每月第24天</span><span class="sxs-lookup"><span data-stu-id="771a1-186">Day 24 of a month</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="771a1-187"><span id="25"></span>**25** (16777216) </span><span class="sxs-lookup"><span data-stu-id="771a1-187"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-188">每月25日</span><span class="sxs-lookup"><span data-stu-id="771a1-188">Day 25 of a month</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="771a1-189"><span id="26"></span>**26** (33554432) </span><span class="sxs-lookup"><span data-stu-id="771a1-189"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-190">每月26日</span><span class="sxs-lookup"><span data-stu-id="771a1-190">Day 26 of a month</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="771a1-191"><span id="27"></span>**27** (67108864) </span><span class="sxs-lookup"><span data-stu-id="771a1-191"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-192">每月第27天</span><span class="sxs-lookup"><span data-stu-id="771a1-192">Day 27 of a month</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="771a1-193"><span id="28"></span>**28** (134217728) </span><span class="sxs-lookup"><span data-stu-id="771a1-193"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-194">一個月的第28天</span><span class="sxs-lookup"><span data-stu-id="771a1-194">Day 28 of a month</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="771a1-195"><span id="29"></span>**29** (268435456) </span><span class="sxs-lookup"><span data-stu-id="771a1-195"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-196">每月第29天</span><span class="sxs-lookup"><span data-stu-id="771a1-196">Day 29 of a month</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="771a1-197"><span id="30"></span>**30** (536870912) </span><span class="sxs-lookup"><span data-stu-id="771a1-197"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-198">每月30日</span><span class="sxs-lookup"><span data-stu-id="771a1-198">Day 30 of a month</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="771a1-199"><span id="31"></span>**31** (1073741824) </span><span class="sxs-lookup"><span data-stu-id="771a1-199"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="771a1-200">月31日</span><span class="sxs-lookup"><span data-stu-id="771a1-200">Day 31 of a month</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="771a1-201">*InteractWithDesktop* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="771a1-201">*InteractWithDesktop* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="771a1-202">若 **為 True**，表示指定的工作應該是互動式的，這表示使用者可以在工作執行時將輸入提供給排程工作。</span><span class="sxs-lookup"><span data-stu-id="771a1-202">If **True**, the specified job should be interactive, which means that a user can give input to a scheduled job while the job is executing.</span></span> <span data-ttu-id="771a1-203">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="771a1-203">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-204">*JobId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="771a1-204">*JobId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="771a1-205">作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="771a1-205">Identifier number of a job.</span></span> <span data-ttu-id="771a1-206">此參數是在電腦上排程之作業的控制碼。</span><span class="sxs-lookup"><span data-stu-id="771a1-206">This parameter is a handle to a job being scheduled on a computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="771a1-207">傳回值</span><span class="sxs-lookup"><span data-stu-id="771a1-207">Return value</span></span>

<span data-ttu-id="771a1-208">在成功時傳回 0 (零) 的值，並傳回不同的數位來表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="771a1-208">Returns a value of 0 (zero) when successful, and a different number to indicate an error.</span></span> <span data-ttu-id="771a1-209">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="771a1-209">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="771a1-210">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="771a1-210">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="771a1-211">**成功完成**</span><span class="sxs-lookup"><span data-stu-id="771a1-211">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="771a1-212">0</span><span class="sxs-lookup"><span data-stu-id="771a1-212">0</span></span>

<span data-ttu-id="771a1-213">已接受要求。</span><span class="sxs-lookup"><span data-stu-id="771a1-213">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-214">**不支援**</span><span class="sxs-lookup"><span data-stu-id="771a1-214">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="771a1-215">1</span><span class="sxs-lookup"><span data-stu-id="771a1-215">1</span></span>

<span data-ttu-id="771a1-216">不支援此要求。</span><span class="sxs-lookup"><span data-stu-id="771a1-216">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-217">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="771a1-217">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="771a1-218">2</span><span class="sxs-lookup"><span data-stu-id="771a1-218">2</span></span>

<span data-ttu-id="771a1-219">使用者沒有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="771a1-219">The user does not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-220">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="771a1-220">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="771a1-221">8</span><span class="sxs-lookup"><span data-stu-id="771a1-221">8</span></span>

<span data-ttu-id="771a1-222">互動式進程。</span><span class="sxs-lookup"><span data-stu-id="771a1-222">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-223">**找不到路徑**</span><span class="sxs-lookup"><span data-stu-id="771a1-223">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="771a1-224">9</span><span class="sxs-lookup"><span data-stu-id="771a1-224">9</span></span>

<span data-ttu-id="771a1-225">找不到服務可執行檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="771a1-225">The directory path to the service executable file cannot be found.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-226">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="771a1-226">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="771a1-227">21</span><span class="sxs-lookup"><span data-stu-id="771a1-227">21</span></span>

<span data-ttu-id="771a1-228">傳遞給服務的參數無效。</span><span class="sxs-lookup"><span data-stu-id="771a1-228">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-229">**服務未啟動**</span><span class="sxs-lookup"><span data-stu-id="771a1-229">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="771a1-230">22</span><span class="sxs-lookup"><span data-stu-id="771a1-230">22</span></span>

<span data-ttu-id="771a1-231">執行此服務的帳戶無效，或缺少執行服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="771a1-231">The account that this service runs under is invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="771a1-232">**其他**</span><span class="sxs-lookup"><span data-stu-id="771a1-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="771a1-233">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="771a1-233">23 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="771a1-234">備註</span><span class="sxs-lookup"><span data-stu-id="771a1-234">Remarks</span></span>

<span data-ttu-id="771a1-235">如果您的排程工作啟動了互動式程式，例如「記事本」，則 **InteractWithDeskto** 屬性必須設定為 **True** ，否則就看不到該程式的畫面。</span><span class="sxs-lookup"><span data-stu-id="771a1-235">If your scheduled job starts an interactive program such as Notepad, then the **InteractWithDeskto** property must be set to **True** or the program's screen is not visible.</span></span> <span data-ttu-id="771a1-236">即使此程式未出現在畫面上，仍會出現在 **工作管理員** 中。</span><span class="sxs-lookup"><span data-stu-id="771a1-236">The process still appears in the **Task Manager** even if it does not appear on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="771a1-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="771a1-237">Requirements</span></span>



| <span data-ttu-id="771a1-238">需求</span><span class="sxs-lookup"><span data-stu-id="771a1-238">Requirement</span></span> | <span data-ttu-id="771a1-239">值</span><span class="sxs-lookup"><span data-stu-id="771a1-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="771a1-240">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="771a1-240">Minimum supported client</span></span><br/> | <span data-ttu-id="771a1-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="771a1-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="771a1-242">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="771a1-242">Minimum supported server</span></span><br/> | <span data-ttu-id="771a1-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="771a1-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="771a1-244">命名空間</span><span class="sxs-lookup"><span data-stu-id="771a1-244">Namespace</span></span><br/>                | <span data-ttu-id="771a1-245">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="771a1-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="771a1-246">MOF</span><span class="sxs-lookup"><span data-stu-id="771a1-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="771a1-247"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="771a1-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="771a1-248">DLL</span><span class="sxs-lookup"><span data-stu-id="771a1-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="771a1-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="771a1-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="771a1-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="771a1-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="771a1-251">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="771a1-251">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="771a1-252">**Win32 \_ register-scheduledjob**</span><span class="sxs-lookup"><span data-stu-id="771a1-252">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

