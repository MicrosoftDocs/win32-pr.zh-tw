---
description: 表示以 AT 命令建立的工作。
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Win32_ScheduledJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025849"
---
# <a name="win32_scheduledjob-class"></a><span data-ttu-id="c8073-103">Win32 \_ register-scheduledjob 類別</span><span class="sxs-lookup"><span data-stu-id="c8073-103">Win32\_ScheduledJob class</span></span>

<span data-ttu-id="c8073-104">**Win32 \_ register-scheduledjob** [WMI 類別](../wmisdk/retrieving-a-class.md)   代表以 **AT** 命令建立的工作。</span><span class="sxs-lookup"><span data-stu-id="c8073-104">The **Win32\_ScheduledJob** [WMI class](../wmisdk/retrieving-a-class.md) represents a job created with the **AT** command.</span></span>

> [!Note]  
> <span data-ttu-id="c8073-105">**Win32 \_ register-scheduledjob** 類別不代表從主控台的排程工作 Wizard 建立的工作。</span><span class="sxs-lookup"><span data-stu-id="c8073-105">The **Win32\_ScheduledJob** class does not represent a job created with the Scheduled Task Wizard from the Control Panel.</span></span> <span data-ttu-id="c8073-106">您無法在 [排程工作] UI 中變更 WMI 所建立的工作。</span><span class="sxs-lookup"><span data-stu-id="c8073-106">You cannot change a task created by WMI in the Scheduled Tasks UI.</span></span> <span data-ttu-id="c8073-107">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="c8073-107">For more information, see the Remarks section.</span></span>

 

<span data-ttu-id="c8073-108">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c8073-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c8073-109">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="c8073-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8073-110">語法</span><span class="sxs-lookup"><span data-stu-id="c8073-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="c8073-111">成員</span><span class="sxs-lookup"><span data-stu-id="c8073-111">Members</span></span>

<span data-ttu-id="c8073-112">**Win32 \_ register-scheduledjob** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c8073-112">The **Win32\_ScheduledJob** class has these types of members:</span></span>

-   [<span data-ttu-id="c8073-113">方法</span><span class="sxs-lookup"><span data-stu-id="c8073-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c8073-114">屬性</span><span class="sxs-lookup"><span data-stu-id="c8073-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c8073-115">方法</span><span class="sxs-lookup"><span data-stu-id="c8073-115">Methods</span></span>

<span data-ttu-id="c8073-116">**Win32 \_ register-scheduledjob** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c8073-116">The **Win32\_ScheduledJob** class has these methods.</span></span>



| <span data-ttu-id="c8073-117">方法</span><span class="sxs-lookup"><span data-stu-id="c8073-117">Method</span></span>                                                      | <span data-ttu-id="c8073-118">描述</span><span class="sxs-lookup"><span data-stu-id="c8073-118">Description</span></span>                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8073-119">**創建**</span><span class="sxs-lookup"><span data-stu-id="c8073-119">**Create**</span></span>](create-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="c8073-120">類別方法，可將作業提交至作業系統，以在指定的未來時間和日期執行。</span><span class="sxs-lookup"><span data-stu-id="c8073-120">Class method that submits a job to the operating system for execution at a specified future time and date.</span></span><br/> |
| [<span data-ttu-id="c8073-121">**刪除**</span><span class="sxs-lookup"><span data-stu-id="c8073-121">**Delete**</span></span>](delete-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="c8073-122">刪除排程工作的類別方法。</span><span class="sxs-lookup"><span data-stu-id="c8073-122">Class method that deletes a scheduled job.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="c8073-123">屬性</span><span class="sxs-lookup"><span data-stu-id="c8073-123">Properties</span></span>

<span data-ttu-id="c8073-124">**Win32 \_ register-scheduledjob** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c8073-124">The **Win32\_ScheduledJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8073-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="c8073-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8073-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-128">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-128">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-129">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="c8073-129">A short textual description of the object.</span></span>

<span data-ttu-id="c8073-130">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8073-131">**命令**</span><span class="sxs-lookup"><span data-stu-id="c8073-131">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8073-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-134">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Command**" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Command**")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-135">命令的名稱、批次程式或二進位檔案 (和命令列引數，) 排程服務用來叫用作業的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="c8073-135">Name of the command, batch program, or binary file (and command-line arguments) that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="c8073-136">範例： "**defrag** **/q/f**"</span><span class="sxs-lookup"><span data-stu-id="c8073-136">Example: "**defrag** **/q/f**"</span></span>

</dd> <dt>

<span data-ttu-id="c8073-137">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="c8073-137">**DaysOfMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c8073-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-140">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfMonth**")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-141">排程執行作業的當月天數。</span><span class="sxs-lookup"><span data-stu-id="c8073-141">Days of the month when the job is scheduled to run.</span></span> <span data-ttu-id="c8073-142">如果工作排程在一個月的多天執行，這些值可以聯結在邏輯 OR 中。</span><span class="sxs-lookup"><span data-stu-id="c8073-142">If a job is scheduled to run on multiple days of the month, these values can be joined in a logical OR.</span></span> <span data-ttu-id="c8073-143">例如，如果作業是在每個月的1和16執行，則 **DaysOfMonth** 屬性的值會是1或32768。</span><span class="sxs-lookup"><span data-stu-id="c8073-143">For example, if a job is to run on the 1st and 16th of each month, the value of the **DaysOfMonth** property would be 1 OR 32768.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="c8073-144"><span id="1"></span>**1** (1) </span><span class="sxs-lookup"><span data-stu-id="c8073-144"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-145">第一</span><span class="sxs-lookup"><span data-stu-id="c8073-145">1st</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="c8073-146"><span id="2"></span>**2** (2) </span><span class="sxs-lookup"><span data-stu-id="c8073-146"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-147">第二</span><span class="sxs-lookup"><span data-stu-id="c8073-147">2nd</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="c8073-148"><span id="3"></span>**3** (4) </span><span class="sxs-lookup"><span data-stu-id="c8073-148"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-149">第三</span><span class="sxs-lookup"><span data-stu-id="c8073-149">3rd</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="c8073-150"><span id="4"></span>**4** (8) </span><span class="sxs-lookup"><span data-stu-id="c8073-150"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-151">第四</span><span class="sxs-lookup"><span data-stu-id="c8073-151">4th</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="c8073-152"><span id="5"></span>**5** (16) </span><span class="sxs-lookup"><span data-stu-id="c8073-152"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-153">第 5 個</span><span class="sxs-lookup"><span data-stu-id="c8073-153">5th</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="c8073-154"><span id="6"></span>**6** (32) </span><span class="sxs-lookup"><span data-stu-id="c8073-154"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-155">第 6 個</span><span class="sxs-lookup"><span data-stu-id="c8073-155">6th</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="c8073-156"><span id="7"></span>**7** (64) </span><span class="sxs-lookup"><span data-stu-id="c8073-156"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-157">第 7 個</span><span class="sxs-lookup"><span data-stu-id="c8073-157">7th</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="c8073-158"><span id="8"></span>**8** (128) </span><span class="sxs-lookup"><span data-stu-id="c8073-158"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-159">第 8 個</span><span class="sxs-lookup"><span data-stu-id="c8073-159">8th</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="c8073-160"><span id="9"></span>**9** (256) </span><span class="sxs-lookup"><span data-stu-id="c8073-160"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-161">第 9 個</span><span class="sxs-lookup"><span data-stu-id="c8073-161">9th</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="c8073-162"><span id="10"></span>**10** (512) </span><span class="sxs-lookup"><span data-stu-id="c8073-162"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-163">日</span><span class="sxs-lookup"><span data-stu-id="c8073-163">10th</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="c8073-164"><span id="11"></span>**11** (1024) </span><span class="sxs-lookup"><span data-stu-id="c8073-164"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-165">11th</span><span class="sxs-lookup"><span data-stu-id="c8073-165">11th</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="c8073-166"><span id="12"></span>**12** (2048) </span><span class="sxs-lookup"><span data-stu-id="c8073-166"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-167">12th</span><span class="sxs-lookup"><span data-stu-id="c8073-167">12th</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="c8073-168"><span id="13"></span>**13** (4096) </span><span class="sxs-lookup"><span data-stu-id="c8073-168"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-169">13th</span><span class="sxs-lookup"><span data-stu-id="c8073-169">13th</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="c8073-170"><span id="14"></span>**14** (8192) </span><span class="sxs-lookup"><span data-stu-id="c8073-170"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-171">日</span><span class="sxs-lookup"><span data-stu-id="c8073-171">14th</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="c8073-172"><span id="15"></span>**15** (16384) </span><span class="sxs-lookup"><span data-stu-id="c8073-172"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-173">日</span><span class="sxs-lookup"><span data-stu-id="c8073-173">15th</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="c8073-174"><span id="16"></span>**16** (32768) </span><span class="sxs-lookup"><span data-stu-id="c8073-174"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-175">十六</span><span class="sxs-lookup"><span data-stu-id="c8073-175">16th</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="c8073-176"><span id="17"></span>**17** (65536) </span><span class="sxs-lookup"><span data-stu-id="c8073-176"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-177">17日</span><span class="sxs-lookup"><span data-stu-id="c8073-177">17th</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="c8073-178"><span id="18"></span>**18** (131072) </span><span class="sxs-lookup"><span data-stu-id="c8073-178"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-179">日前</span><span class="sxs-lookup"><span data-stu-id="c8073-179">18th</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="c8073-180"><span id="19"></span>**19** (262144) </span><span class="sxs-lookup"><span data-stu-id="c8073-180"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-181">19日</span><span class="sxs-lookup"><span data-stu-id="c8073-181">19th</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="c8073-182"><span id="20"></span>**20** (524288) </span><span class="sxs-lookup"><span data-stu-id="c8073-182"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-183">月</span><span class="sxs-lookup"><span data-stu-id="c8073-183">20th</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="c8073-184"><span id="21"></span>**21** (1048576) </span><span class="sxs-lookup"><span data-stu-id="c8073-184"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-185">21st</span><span class="sxs-lookup"><span data-stu-id="c8073-185">21st</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="c8073-186"><span id="22"></span>**22** (2097152) </span><span class="sxs-lookup"><span data-stu-id="c8073-186"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-187">22nd</span><span class="sxs-lookup"><span data-stu-id="c8073-187">22nd</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="c8073-188"><span id="23"></span>**23** (4194304) </span><span class="sxs-lookup"><span data-stu-id="c8073-188"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-189">23rd</span><span class="sxs-lookup"><span data-stu-id="c8073-189">23rd</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="c8073-190"><span id="24"></span>**24** (8388608) </span><span class="sxs-lookup"><span data-stu-id="c8073-190"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-191">24 日</span><span class="sxs-lookup"><span data-stu-id="c8073-191">24th</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="c8073-192"><span id="25"></span>**25** (16777216) </span><span class="sxs-lookup"><span data-stu-id="c8073-192"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-193">百分點</span><span class="sxs-lookup"><span data-stu-id="c8073-193">25th</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="c8073-194"><span id="26"></span>**26** (33554432) </span><span class="sxs-lookup"><span data-stu-id="c8073-194"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-195">26 日</span><span class="sxs-lookup"><span data-stu-id="c8073-195">26th</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="c8073-196"><span id="27"></span>**27** (67108864) </span><span class="sxs-lookup"><span data-stu-id="c8073-196"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-197">27 日</span><span class="sxs-lookup"><span data-stu-id="c8073-197">27th</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="c8073-198"><span id="28"></span>**28** (134217728) </span><span class="sxs-lookup"><span data-stu-id="c8073-198"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-199">28 日</span><span class="sxs-lookup"><span data-stu-id="c8073-199">28th</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="c8073-200"><span id="29"></span>**29** (268435456) </span><span class="sxs-lookup"><span data-stu-id="c8073-200"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-201">29 日</span><span class="sxs-lookup"><span data-stu-id="c8073-201">29th</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="c8073-202"><span id="30"></span>**30** (536870912) </span><span class="sxs-lookup"><span data-stu-id="c8073-202"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-203">號</span><span class="sxs-lookup"><span data-stu-id="c8073-203">30th</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="c8073-204"><span id="31"></span>**31** (1073741824) </span><span class="sxs-lookup"><span data-stu-id="c8073-204"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="c8073-205">31 日</span><span class="sxs-lookup"><span data-stu-id="c8073-205">31st</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c8073-206">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="c8073-206">**DaysOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-207">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c8073-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-209">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfWeek**")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-210">排程執行工作的星期幾。</span><span class="sxs-lookup"><span data-stu-id="c8073-210">Days of the week when a job is scheduled to run.</span></span> <span data-ttu-id="c8073-211">如果工作排程在一周的多天執行，這些值可以聯結在邏輯 OR 中。</span><span class="sxs-lookup"><span data-stu-id="c8073-211">If a job is scheduled to run on multiple days of the week, the values can be joined in a logical OR.</span></span> <span data-ttu-id="c8073-212">例如，如果工作排定在星期一、星期三和星期五執行， **DaysOfWeek** 屬性的值會是1或4或16。</span><span class="sxs-lookup"><span data-stu-id="c8073-212">For example, if a job is scheduled to run on Mondays, Wednesdays, and Fridays the value of the **DaysOfWeek** property would be 1 OR 4 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="c8073-213">**星期一** (1) </span><span class="sxs-lookup"><span data-stu-id="c8073-213">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="c8073-214">**星期二** (2) </span><span class="sxs-lookup"><span data-stu-id="c8073-214">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="c8073-215">**星期三** (4) </span><span class="sxs-lookup"><span data-stu-id="c8073-215">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="c8073-216">**星期四** (8) </span><span class="sxs-lookup"><span data-stu-id="c8073-216">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="c8073-217">**星期五** (16) </span><span class="sxs-lookup"><span data-stu-id="c8073-217">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="c8073-218">**星期六** (32) </span><span class="sxs-lookup"><span data-stu-id="c8073-218">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="c8073-219">**星期日** (64) </span><span class="sxs-lookup"><span data-stu-id="c8073-219">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8073-220">**說明**</span><span class="sxs-lookup"><span data-stu-id="c8073-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8073-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-223">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-224">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="c8073-224">A textual description of the object.</span></span>

<span data-ttu-id="c8073-225">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8073-226">**經過時間**</span><span class="sxs-lookup"><span data-stu-id="c8073-226">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-227">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c8073-227">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8073-229">作業已執行的時間長度。</span><span class="sxs-lookup"><span data-stu-id="c8073-229">Length of time the job has been executing.</span></span>

<span data-ttu-id="c8073-230">這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-230">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8073-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c8073-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-232">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c8073-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-234">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="c8073-234">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-235">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="c8073-235">Indicates when the object was installed.</span></span> <span data-ttu-id="c8073-236">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="c8073-236">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c8073-237">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8073-238">**InteractWithDesktop**</span><span class="sxs-lookup"><span data-stu-id="c8073-238">**InteractWithDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-239">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c8073-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-241">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **JOB \_ 非互動式**" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_NONINTERACTIVE**")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-242">指定的作業是互動式的，這表示使用者可以在執行中的排程工作時提供輸入。</span><span class="sxs-lookup"><span data-stu-id="c8073-242">Specified job is interactive, which means that a user can give input to a scheduled job while it is executing.</span></span>

</dd> <dt>

<span data-ttu-id="c8073-243">**JobId**</span><span class="sxs-lookup"><span data-stu-id="c8073-243">**JobId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-244">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c8073-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-246">限定詞： [**Key**](../wmisdk/key-qualifier.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| \| [**\_ ENUM JobId 的**](/windows/win32/api/lmat/ns-lmat-at_enum)網路管理結構 \| \*\*\*\*" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobId**")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-247">識別作業的數目。</span><span class="sxs-lookup"><span data-stu-id="c8073-247">Identifying number of the job.</span></span> <span data-ttu-id="c8073-248">方法會使用它做為此電腦上所排程之一個作業的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c8073-248">It is used by methods as a handle to one job being scheduled on this computer.</span></span>

</dd> <dt>

<span data-ttu-id="c8073-249">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="c8073-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-250">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8073-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-252">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "JobStatus" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( " \| \| [**在 \_ 列舉**](/windows/win32/api/lmat/ns-lmat-at_enum)旗標的 Win32API 網路管理結構 \|  \| **作業 \_ EXEC \_ 錯誤**" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-252">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**Flags**\|**JOB\_EXEC\_ERROR**")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-253">上次排程執行此作業的執行狀態。</span><span class="sxs-lookup"><span data-stu-id="c8073-253">Status of execution the last time this job was scheduled to run.</span></span>

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

<span data-ttu-id="c8073-254">**成功** ( 「成功」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-254">**Success** ("Success")</span></span>


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

<span data-ttu-id="c8073-255">**失敗** ( 「失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-255">**Failure** ("Failure")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8073-256">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c8073-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8073-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-259">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-259">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-260">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="c8073-260">Label by which the object is known.</span></span> <span data-ttu-id="c8073-261">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="c8073-261">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c8073-262">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8073-263">**通知**</span><span class="sxs-lookup"><span data-stu-id="c8073-263">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8073-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8073-266">當作業完成或失敗時，使用者會收到通知。</span><span class="sxs-lookup"><span data-stu-id="c8073-266">User is notified upon job completion or failure.</span></span>

<span data-ttu-id="c8073-267">這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-267">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8073-268">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="c8073-268">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-269">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8073-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8073-271">提交工作的使用者。</span><span class="sxs-lookup"><span data-stu-id="c8073-271">User who submitted the job.</span></span>

<span data-ttu-id="c8073-272">這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-272">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8073-273">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="c8073-273">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-274">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c8073-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8073-276">作業執行的重要性。</span><span class="sxs-lookup"><span data-stu-id="c8073-276">Importance of a job's execution.</span></span>

<span data-ttu-id="c8073-277">這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-277">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8073-278">**RunRepeatedly**</span><span class="sxs-lookup"><span data-stu-id="c8073-278">**RunRepeatedly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-279">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c8073-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-281">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「 \| \| [**在 \_ 資訊**](/windows/win32/api/lmat/ns-lmat-at_info) \| **旗標** \| **工作 \_ \_ 定期執行** Win32API 網路管理結構」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_RUN\_PERIODICALLY**")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-282">排程工作會在排定作業的天數重複執行。</span><span class="sxs-lookup"><span data-stu-id="c8073-282">Scheduled job runs repeatedly on the days that the job is scheduled.</span></span> <span data-ttu-id="c8073-283">如果 **為 False**，則作業會執行一次。</span><span class="sxs-lookup"><span data-stu-id="c8073-283">If **False**, then the job is run one time.</span></span>

</dd> <dt>

<span data-ttu-id="c8073-284">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="c8073-284">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-285">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c8073-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-287">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "StartTime" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**AT \_ ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobTime**" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-287">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobTime**")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-288">執行作業的 UTC 時間，格式為 "YYYYMMDDHHMMSS.FFFFFF"。MMMMMM (+-) OOO "，其中" YYYYMMDD "必須以" "取代 \* \* \* \* \* \* \* \* 。</span><span class="sxs-lookup"><span data-stu-id="c8073-288">UTC time to run the job, in the form of "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="c8073-289">取代是必要的，因為排程服務只允許將作業設定為執行一次，或在一個月或一周的某一天執行。</span><span class="sxs-lookup"><span data-stu-id="c8073-289">The replacement is necessary because the scheduling service only allows jobs to be configured to run one time, or run on a day of the month or week.</span></span> <span data-ttu-id="c8073-290">無法在特定日期執行作業。</span><span class="sxs-lookup"><span data-stu-id="c8073-290">A job cannot be run on a specific date.</span></span>

<span data-ttu-id="c8073-291">**StartTime** 屬性值的 " (+-) OOO" 區段是本地時間轉譯目前的偏差。</span><span class="sxs-lookup"><span data-stu-id="c8073-291">The "(+-)OOO" section of the **StartTime** property value is the current bias for local time translation.</span></span> <span data-ttu-id="c8073-292">偏差是 UTC 時間與本地時間之間的差異。</span><span class="sxs-lookup"><span data-stu-id="c8073-292">The bias is the difference between the UTC time and local time.</span></span> <span data-ttu-id="c8073-293">若要計算時區的偏差，請將您時區提前或晚于格林威治標準時間的小時數乘以60的 (GMT)  (如果您的時區是在 GMT 之前，則以小時為單位，如果您的時區晚于 gmt) ，則為負數。</span><span class="sxs-lookup"><span data-stu-id="c8073-293">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="c8073-294">如果您的時區使用日光節約時間，請在您的計算中加入額外的60。</span><span class="sxs-lookup"><span data-stu-id="c8073-294">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="c8073-295">例如，太平洋標準時區是 GMT 後八小時，因此偏差等於-420 (-8 \* 60 + 60) 當日光節約時間正在使用中時，當日光節約時間未使用時，則為-480 (-8 \* 60) 。</span><span class="sxs-lookup"><span data-stu-id="c8073-295">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="c8073-296">您也可以藉由查詢 [**Win32 \_ 時區**](win32-timezone.md) 類別的偏差屬性來判斷偏差的值。</span><span class="sxs-lookup"><span data-stu-id="c8073-296">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

<span data-ttu-id="c8073-297">例如： " \* \* \* \* \* \* \* \* 123000.000000-420" 會指定 14.30 (2:30 P.M. ) PST，並有日光節約時間生效。</span><span class="sxs-lookup"><span data-stu-id="c8073-297">For example: "\*\*\*\*\*\*\*\*123000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

</dd> <dt>

<span data-ttu-id="c8073-298">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c8073-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-299">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8073-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8073-301">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c8073-302">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="c8073-302">String that indicates the current status of the object.</span></span> <span data-ttu-id="c8073-303">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="c8073-303">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c8073-304">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="c8073-304">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c8073-305">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="c8073-305">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c8073-306">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="c8073-306">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c8073-307">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="c8073-307">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c8073-308">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="c8073-308">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c8073-309">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-309">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c8073-310">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="c8073-310">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c8073-311">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="c8073-311">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c8073-312">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-312">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c8073-313">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-313">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c8073-314">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-314">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c8073-315">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-315">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c8073-316">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-316">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c8073-317">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-317">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c8073-318">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-318">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c8073-319">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-319">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c8073-320">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="c8073-320">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c8073-321">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-321">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c8073-322">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="c8073-322">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8073-323">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="c8073-323">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-324">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c8073-324">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8073-326">提交作業的時間。</span><span class="sxs-lookup"><span data-stu-id="c8073-326">Time that the job was submitted.</span></span>

<span data-ttu-id="c8073-327">這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-327">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8073-328">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="c8073-328">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8073-329">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c8073-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8073-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8073-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8073-331">作業無效或應該停止的時間。</span><span class="sxs-lookup"><span data-stu-id="c8073-331">Time at which the job is invalid or should be stopped.</span></span>

<span data-ttu-id="c8073-332">這個屬性繼承自 [**CIM \_ 工作**](cim-job.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-332">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8073-333">備註</span><span class="sxs-lookup"><span data-stu-id="c8073-333">Remarks</span></span>

<span data-ttu-id="c8073-334">針對排程服務排程的每個作業都會持續儲存 (排程器可以在重新開機) 之後啟動作業，並在一周或每個月的指定時間執行。</span><span class="sxs-lookup"><span data-stu-id="c8073-334">Each job scheduled against the schedule service is stored persistently (the scheduler can start a job after a reboot), and is executed at the specified time and day of the week or month.</span></span> <span data-ttu-id="c8073-335">如果電腦不在使用中，或排程服務未在指定的工作時間執行，則排程服務會在下一天的指定時間執行指定的工作。</span><span class="sxs-lookup"><span data-stu-id="c8073-335">If the computer is not active, or if the scheduled service is not running at the specified job time, the schedule service runs the specified job on the next day at the specified time.</span></span>

<span data-ttu-id="c8073-336">工作的排程是根據國際標準時間 (UTC) 加上格林威治標準時間 (GMT) 的偏差位移，這表示可以使用任何時區來指定作業。</span><span class="sxs-lookup"><span data-stu-id="c8073-336">Jobs are scheduled according to Coordinated Universal Time (UTC) with bias offset from Greenwich Mean Time (GMT), which means that a job can be specified using any time zone.</span></span> <span data-ttu-id="c8073-337">在列舉物件時， **Win32 \_ register-scheduledjob** 類別會傳回 UTC 位移的當地時間，並在建立新的作業時轉換為當地時間。</span><span class="sxs-lookup"><span data-stu-id="c8073-337">The **Win32\_ScheduledJob** class returns the local time with UTC offset when enumerating an object, and converts to local time when creating new jobs.</span></span> <span data-ttu-id="c8073-338">例如，指定要在波士頓的電腦上于下午10:30 執行的工作</span><span class="sxs-lookup"><span data-stu-id="c8073-338">For example, a job specified to run on a computer in Boston at 10:30 P.M.</span></span> <span data-ttu-id="c8073-339">星期一 PST time 將排程在本機上午1:30 執行。</span><span class="sxs-lookup"><span data-stu-id="c8073-339">Monday PST time will be scheduled to run locally at 1:30 A.M.</span></span> <span data-ttu-id="c8073-340">星期二 EST</span><span class="sxs-lookup"><span data-stu-id="c8073-340">Tuesday EST.</span></span>

> [!Note]  
> <span data-ttu-id="c8073-341">用戶端必須考慮日光節約時間是否在本機電腦上運作，如果是，則從 UTC 位移減去60分鐘的偏差。</span><span class="sxs-lookup"><span data-stu-id="c8073-341">A client must take into account whether or not daylight savings time is in operation on the local computer, and if it is, then subtract a bias of 60 minutes from the UTC offset.</span></span>

 

<span data-ttu-id="c8073-342">**Win32 \_ register-scheduledjob** 類別衍生自 [**CIM \_ 工作**](cim-job.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-342">The **Win32\_ScheduledJob** class is derived from [**CIM\_Job**](cim-job.md).</span></span> <span data-ttu-id="c8073-343">您必須是 administrators 群組的成員，才能使用這個類別建立排程工作。</span><span class="sxs-lookup"><span data-stu-id="c8073-343">You must be a member of the administrators group to create a scheduled job using this class.</span></span>

<span data-ttu-id="c8073-344">**Win32 \_ register-scheduledjob** 類別是在內部使用 AT 通訊協定，其系結至從 Windows 8 和 Windows Server 2012 開始的淘汰。</span><span class="sxs-lookup"><span data-stu-id="c8073-344">The **Win32\_ScheduledJob** class is internally using the AT protocol, which is bound to deprecation starting with Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="c8073-345">第一個步驟是預設停用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c8073-345">As a first step the AT protocol is disabled by default.</span></span> <span data-ttu-id="c8073-346">如果停用通訊協定，例如在 **Win32 \_ register-scheduledjob** 物件上呼叫 [**Create**](create-method-in-class-win32-scheduledjob.md)方法將會失敗，並出現錯誤0x8。</span><span class="sxs-lookup"><span data-stu-id="c8073-346">If the protocol is disabled, for example calling the [**Create**](create-method-in-class-win32-scheduledjob.md) method on a **Win32\_ScheduledJob** object will fail with error 0x8.</span></span> <span data-ttu-id="c8073-347">您可以藉由新增下列登錄專案，重新開啟 AT 通訊協定：</span><span class="sxs-lookup"><span data-stu-id="c8073-347">You can turn the AT protocol back on by adding the following registry entry:</span></span>

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

<span data-ttu-id="c8073-348">您可能需要重新開機電腦，才能使設定生效。</span><span class="sxs-lookup"><span data-stu-id="c8073-348">You may need to restart the machine to make the setting effective.</span></span>

<span data-ttu-id="c8073-349">因為 **win32 \_ register-scheduledjob** 是以 [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) win32 API 為基礎，所以您無法搭配工作排程器使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="c8073-349">Because **Win32\_ScheduledJob** is based on the [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) Win32 API, you cannot use this class in conjunction with the Task Scheduler.</span></span> <span data-ttu-id="c8073-350">如果您想要使用工作排程器，請使用工作排程器 API。</span><span class="sxs-lookup"><span data-stu-id="c8073-350">If you wish to use Task Scheduler, use the Task Scheduler API.</span></span> <span data-ttu-id="c8073-351">如需詳細資訊，請參閱 [工作排程器參考](../taskschd/task-scheduler-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="c8073-351">For more information, see the [Task Scheduler Reference](../taskschd/task-scheduler-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c8073-352">範例</span><span class="sxs-lookup"><span data-stu-id="c8073-352">Examples</span></span>

<span data-ttu-id="c8073-353">下列 VBScript 程式碼範例會排程 Notepad.exe 在每個星期三的本機電腦時間以互動的方式在1:25 執行。</span><span class="sxs-lookup"><span data-stu-id="c8073-353">The following VBScript code example schedules Notepad.exe to run interactively at 1:25 by the local computer time every Wednesday.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a><span data-ttu-id="c8073-354">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8073-354">Requirements</span></span>



| <span data-ttu-id="c8073-355">需求</span><span class="sxs-lookup"><span data-stu-id="c8073-355">Requirement</span></span> | <span data-ttu-id="c8073-356">值</span><span class="sxs-lookup"><span data-stu-id="c8073-356">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8073-357">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8073-357">Minimum supported client</span></span><br/> | <span data-ttu-id="c8073-358">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8073-358">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8073-359">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8073-359">Minimum supported server</span></span><br/> | <span data-ttu-id="c8073-360">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8073-360">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8073-361">命名空間</span><span class="sxs-lookup"><span data-stu-id="c8073-361">Namespace</span></span><br/>                | <span data-ttu-id="c8073-362">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c8073-362">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8073-363">MOF</span><span class="sxs-lookup"><span data-stu-id="c8073-363">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8073-364"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8073-364"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8073-365">DLL</span><span class="sxs-lookup"><span data-stu-id="c8073-365">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8073-366"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8073-366"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8073-367">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8073-367">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8073-368">**CIM \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="c8073-368">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dt>

[<span data-ttu-id="c8073-369">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="c8073-369">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c8073-370">WMI 工作：已排程的工作</span><span class="sxs-lookup"><span data-stu-id="c8073-370">WMI Tasks: Scheduled Tasks</span></span>](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
