---
description: 代表要執行之工作單位（例如腳本或列印工作）的邏輯元素。 作業與進程不同，因為作業可以排程或排入佇列，而且其執行不限於單一系統。
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: 'CIM_Job 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944772"
---
# <a name="cim_job-class-hyper-v-management"></a><span data-ttu-id="4ad72-104">CIM_Job 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="4ad72-104">CIM_Job class (Hyper-V management)</span></span>

<span data-ttu-id="4ad72-105">代表要執行之工作單位（例如腳本或列印工作）的邏輯元素。</span><span class="sxs-lookup"><span data-stu-id="4ad72-105">A logical element that represents a unit of work to execute, such as a script or a print job.</span></span> <span data-ttu-id="4ad72-106">作業與進程不同，因為作業可以排程或排入佇列，而且其執行不限於單一系統。</span><span class="sxs-lookup"><span data-stu-id="4ad72-106">A job is distinct from a process because a job can be scheduled or queued, and its execution is not limited to a single system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad72-107">語法</span><span class="sxs-lookup"><span data-stu-id="4ad72-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a><span data-ttu-id="4ad72-108">成員</span><span class="sxs-lookup"><span data-stu-id="4ad72-108">Members</span></span>

<span data-ttu-id="4ad72-109">**CIM \_ 作業** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4ad72-109">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="4ad72-110">方法</span><span class="sxs-lookup"><span data-stu-id="4ad72-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4ad72-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4ad72-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4ad72-112">方法</span><span class="sxs-lookup"><span data-stu-id="4ad72-112">Methods</span></span>

<span data-ttu-id="4ad72-113">**CIM \_ 作業** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4ad72-113">The **CIM\_Job** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4ad72-114">方法</span><span class="sxs-lookup"><span data-stu-id="4ad72-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4ad72-115">描述</span><span class="sxs-lookup"><span data-stu-id="4ad72-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4ad72-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ad72-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4ad72-117">此方法已被取代。</span><span class="sxs-lookup"><span data-stu-id="4ad72-117">This method is deprecated.</span></span> <span data-ttu-id="4ad72-118">請改用 <strong>RequestStateChange</strong> 方法。</span><span class="sxs-lookup"><span data-stu-id="4ad72-118">Instead, use the <strong>RequestStateChange</strong> method.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ad72-119">已淘汰的描述：關閉作業。</span><span class="sxs-lookup"><span data-stu-id="4ad72-119">Deprecated description: Shuts down a job.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="4ad72-120">屬性</span><span class="sxs-lookup"><span data-stu-id="4ad72-120">Properties</span></span>

<span data-ttu-id="4ad72-121">**CIM \_ 作業** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4ad72-121">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ad72-122">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="4ad72-122">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-123">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4ad72-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-125">**True** 表示在完成時刪除作業;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="4ad72-125">**True** to delete the job upon completion; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="4ad72-126">這個屬性不會刪除此屬性設定為 **True** 之前完成的工作。</span><span class="sxs-lookup"><span data-stu-id="4ad72-126">This property will not delete jobs that complete before this property is set to **True**.</span></span>

 

</dd> <dt>

<span data-ttu-id="4ad72-127">**經過時間**</span><span class="sxs-lookup"><span data-stu-id="4ad72-127">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-128">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-130">作業已執行的持續時間。</span><span class="sxs-lookup"><span data-stu-id="4ad72-130">The duration for which the job has run.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-131">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4ad72-131">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-132">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad72-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-134">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**ErrorDescription**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-135">特定廠商的錯誤碼，可捕獲週期性作業的處理資訊。</span><span class="sxs-lookup"><span data-stu-id="4ad72-135">A vendor-specific error code that captures processing information for recurring jobs.</span></span> <span data-ttu-id="4ad72-136">如果作業已完成而沒有錯誤，則值必須設為零。</span><span class="sxs-lookup"><span data-stu-id="4ad72-136">The value must be set to zero if the job completed without error.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-137">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4ad72-137">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad72-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-140">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**ErrorCode**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-140">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-141">自由格式的字串，其中包含 **ErrorCode** 屬性中對應錯誤碼的描述。</span><span class="sxs-lookup"><span data-stu-id="4ad72-141">A free-form string that contains a description of the corresponding error code in the **ErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-142">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="4ad72-142">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-143">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4ad72-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-145">作業的執行次數。</span><span class="sxs-lookup"><span data-stu-id="4ad72-145">The number of times to run the job.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-146">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="4ad72-146">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad72-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-149">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-150">表示作業狀態的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="4ad72-150">A free-form string that represents the status of the job.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-151">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-151">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-152">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad72-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-154">指出 **RunStartInterval** 和 **UntilTime** 屬性中的時間是否代表當地時間或 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="4ad72-154">Indicates whether the times in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

<span data-ttu-id="4ad72-155">**本地時間** (1) </span><span class="sxs-lookup"><span data-stu-id="4ad72-155">**Local Time** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

<span data-ttu-id="4ad72-156">**UTC 時間** (2) </span><span class="sxs-lookup"><span data-stu-id="4ad72-156">**UTC Time** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4ad72-157">**通知**</span><span class="sxs-lookup"><span data-stu-id="4ad72-157">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad72-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-160">當作業完成或失敗時要通知的使用者。</span><span class="sxs-lookup"><span data-stu-id="4ad72-160">The user to notify when a job completes or fails.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-161">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="4ad72-161">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad72-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-164">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RecoveryAction**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-165">描述 **RecoveryAction** 屬性為 **其他** ( "1" ) 時之復原動作的字串。</span><span class="sxs-lookup"><span data-stu-id="4ad72-165">A string that describes the recovery action when the **RecoveryAction** property is **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-166">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="4ad72-166">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4ad72-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-169">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ OwningJobElement**](cim-owningjobelement.md)」。) </span><span class="sxs-lookup"><span data-stu-id="4ad72-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OwningJobElement**](cim-owningjobelement.md).")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-170">提交作業的使用者，或要求作業的服務或方法名稱。</span><span class="sxs-lookup"><span data-stu-id="4ad72-170">The user that submitted the Job, or the service or method name that requested the job.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-171">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="4ad72-171">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-172">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad72-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-174">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "percent" ) ， [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0) ， [**Timespan.maxvalue**](/windows/desktop/WmiSdk/standard-qualifiers) (101) ， **PUnit** ( "percent" ) </span><span class="sxs-lookup"><span data-stu-id="4ad72-174">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-175">完成的作業百分比。</span><span class="sxs-lookup"><span data-stu-id="4ad72-175">The percentage of the job that is complete.</span></span>

> [!Note]  
> <span data-ttu-id="4ad72-176">值 "101" 未定義，將不會在規格的下一個主要修訂中允許。</span><span class="sxs-lookup"><span data-stu-id="4ad72-176">The value "101" is undefined and will be not be allowed in the next major revision of the specification.</span></span>

 

</dd> <dt>

<span data-ttu-id="4ad72-177">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="4ad72-177">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-178">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4ad72-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-179">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-180">工作的重要性。</span><span class="sxs-lookup"><span data-stu-id="4ad72-180">The importance of the job.</span></span> <span data-ttu-id="4ad72-181">編號愈低，優先順序愈高。</span><span class="sxs-lookup"><span data-stu-id="4ad72-181">The lower the number, the higher the priority.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-182">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="4ad72-182">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-183">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ad72-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-185">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**OtherRecoveryAction**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**OtherRecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-186">描述執行作業失敗時要採取的修復動作。</span><span class="sxs-lookup"><span data-stu-id="4ad72-186">Describes the recovery action to take when a run job fails.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4ad72-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4ad72-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4ad72-188">什麼是要採取的復原動作未知。</span><span class="sxs-lookup"><span data-stu-id="4ad72-188">It is unknown as to what recovery action to take.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4ad72-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4ad72-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4ad72-190">復原動作將會在 **OtherRecoveryAction** 屬性中指定。</span><span class="sxs-lookup"><span data-stu-id="4ad72-190">The recovery action will be specified in the **OtherRecoveryAction** property.</span></span>

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span data-ttu-id="4ad72-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**請勿繼續** (2) </span><span class="sxs-lookup"><span data-stu-id="4ad72-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4ad72-192">停止執行作業，並適當地更新其狀態。</span><span class="sxs-lookup"><span data-stu-id="4ad72-192">Stop the execution of the job and appropriately update its status.</span></span>

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span data-ttu-id="4ad72-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**繼續進行下一個工作** (3) </span><span class="sxs-lookup"><span data-stu-id="4ad72-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4ad72-194">繼續執行佇列中的下一個工作。</span><span class="sxs-lookup"><span data-stu-id="4ad72-194">Continue with the next job in the queue.</span></span>

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span data-ttu-id="4ad72-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span> (4) **重新執行作業**</span><span class="sxs-lookup"><span data-stu-id="4ad72-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4ad72-196">應重新執行作業。</span><span class="sxs-lookup"><span data-stu-id="4ad72-196">The job should be re-run.</span></span>

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span data-ttu-id="4ad72-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**執行復原工作** (5) </span><span class="sxs-lookup"><span data-stu-id="4ad72-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Run Recovery Job** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4ad72-198">執行使用 **RecoveryJob** 關聯性建立關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="4ad72-198">Run the Job associated using the **RecoveryJob** relationship.</span></span> <span data-ttu-id="4ad72-199">請注意，復原工作必須已在將執行它的佇列中。</span><span class="sxs-lookup"><span data-stu-id="4ad72-199">Note that the recovery Job must already be in the queue from which it will run.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4ad72-200">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="4ad72-200">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-201">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="4ad72-201">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-203">限定詞： [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31) ， [**int32.maxvalue (31**](/windows/desktop/WmiSdk/standard-qualifiers)) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RunMonth**"，"**CIM \_ 作業**。**RunDayOfWeek**"，"**CIM \_ 作業**。**RunStartInterval**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-203">Qualifiers: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-204">搭配 **RunDayOfWeek** 屬性使用的整數，表示處理作業的日期;或者，如果 **RunDayOfWeek** 設定為零，則 **RunDay** 會指出處理作業的月份日期。</span><span class="sxs-lookup"><span data-stu-id="4ad72-204">An integer that is used on conjunction with the **RunDayOfWeek** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span> <span data-ttu-id="4ad72-205">如果 **RunDay** 是負整數，它會指定相對於月底的一天，或如果 **RunDay** 是正整數，則會指定一天相對於當月的開始時間。</span><span class="sxs-lookup"><span data-stu-id="4ad72-205">If **RunDay** is a negative integer, it specifies a day relative to the end of the month, or if **RunDay** is a positive integer, it specifies a day relative to the beginning of the month.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-206">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="4ad72-206">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-207">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="4ad72-207">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-208">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-209">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RunMonth**"，"**CIM \_ 作業**。**RunDay**"，"**CIM \_ 作業**。**RunStartInterval**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-209">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-210">搭配 **RunDay** 屬性使用的整數，表示處理作業的日期;或者，如果 **RunDayOfWeek** 設定為零，則 **RunDay** 會指出處理作業的月份日期。</span><span class="sxs-lookup"><span data-stu-id="4ad72-210">An integer that is used on conjunction with the **RunDay** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span>

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

<span data-ttu-id="4ad72-211">**-星期六** (-7) </span><span class="sxs-lookup"><span data-stu-id="4ad72-211">**-Saturday** (-7)</span></span>


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

<span data-ttu-id="4ad72-212">**-星期五** (-6) </span><span class="sxs-lookup"><span data-stu-id="4ad72-212">**-Friday** (-6)</span></span>


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

<span data-ttu-id="4ad72-213">**-星期四** (-5) </span><span class="sxs-lookup"><span data-stu-id="4ad72-213">**-Thursday** (-5)</span></span>


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

<span data-ttu-id="4ad72-214">**-星期三** (-4) </span><span class="sxs-lookup"><span data-stu-id="4ad72-214">**-Wednesday** (-4)</span></span>


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

<span data-ttu-id="4ad72-215">**-星期二** (-3) </span><span class="sxs-lookup"><span data-stu-id="4ad72-215">**-Tuesday** (-3)</span></span>


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

<span data-ttu-id="4ad72-216">**-星期一** (-2) </span><span class="sxs-lookup"><span data-stu-id="4ad72-216">**-Monday** (-2)</span></span>


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

<span data-ttu-id="4ad72-217">**-星期日** (-1) </span><span class="sxs-lookup"><span data-stu-id="4ad72-217">**-Sunday** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

<span data-ttu-id="4ad72-218">**ExactDayOfMonth** (0) </span><span class="sxs-lookup"><span data-stu-id="4ad72-218">**ExactDayOfMonth** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="4ad72-219">**星期日** (1) </span><span class="sxs-lookup"><span data-stu-id="4ad72-219">**Sunday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="4ad72-220">**星期一** (2) </span><span class="sxs-lookup"><span data-stu-id="4ad72-220">**Monday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="4ad72-221">**星期二** (3) </span><span class="sxs-lookup"><span data-stu-id="4ad72-221">**Tuesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="4ad72-222">**星期三** (4) </span><span class="sxs-lookup"><span data-stu-id="4ad72-222">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="4ad72-223">**星期四** (5) </span><span class="sxs-lookup"><span data-stu-id="4ad72-223">**Thursday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="4ad72-224">**星期五** (6) </span><span class="sxs-lookup"><span data-stu-id="4ad72-224">**Friday** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="4ad72-225">**星期六** (7) </span><span class="sxs-lookup"><span data-stu-id="4ad72-225">**Saturday** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4ad72-226">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="4ad72-226">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-227">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="4ad72-227">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-228">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-229">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RunDay**"，"**CIM \_ 作業**。**RunDayOfWeek**"，"**CIM \_ 作業**。**RunStartInterval**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-229">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-230">處理作業的月份。</span><span class="sxs-lookup"><span data-stu-id="4ad72-230">The month when the job is processed.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="4ad72-231">**1 月** (0) </span><span class="sxs-lookup"><span data-stu-id="4ad72-231">**January** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="4ad72-232">**二月** (1) </span><span class="sxs-lookup"><span data-stu-id="4ad72-232">**February** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="4ad72-233">**3 月** (2) </span><span class="sxs-lookup"><span data-stu-id="4ad72-233">**March** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="4ad72-234">**四月** (3) </span><span class="sxs-lookup"><span data-stu-id="4ad72-234">**April** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="4ad72-235">**5 月** (4) </span><span class="sxs-lookup"><span data-stu-id="4ad72-235">**May** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="4ad72-236">**6 月** (5) </span><span class="sxs-lookup"><span data-stu-id="4ad72-236">**June** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="4ad72-237">**7 月** (6) </span><span class="sxs-lookup"><span data-stu-id="4ad72-237">**July** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="4ad72-238">**8 月** (7) </span><span class="sxs-lookup"><span data-stu-id="4ad72-238">**August** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="4ad72-239">**9 月** (8) </span><span class="sxs-lookup"><span data-stu-id="4ad72-239">**September** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="4ad72-240">**10 月** (9) </span><span class="sxs-lookup"><span data-stu-id="4ad72-240">**October** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="4ad72-241">**11 月** (10) </span><span class="sxs-lookup"><span data-stu-id="4ad72-241">**November** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="4ad72-242">**12 月** (11) </span><span class="sxs-lookup"><span data-stu-id="4ad72-242">**December** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4ad72-243">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="4ad72-243">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-244">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-244">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-245">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-246">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**RunMonth**"，"**CIM \_ 作業**。**RunDay**"，"**CIM \_ 作業**。**RunDayOfWeek**"，"**CIM \_ 作業**。**RunStartInterval**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-246">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-247">處理作業的午夜之後的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="4ad72-247">The time interval after midnight when the job is be processed.</span></span> <span data-ttu-id="4ad72-248">例如，"00000000020000.000000： 000" 表示作業是在兩個點鐘的當地時間或之後執行，或 UTC 時間 (UTC 是以 **LocalOrUtcTime** 屬性) 指定。</span><span class="sxs-lookup"><span data-stu-id="4ad72-248">For example, "00000000020000.000000:000" indicates that the job is be run on or after two o'clock local time, or UTC time (UTC is specified with the **LocalOrUtcTime** property).</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-249">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-249">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-250">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-251">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-251">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-252">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「**CIM \_ 作業**」。**RunMonth**"，"**CIM \_ 作業**。**RunDay**"，"**CIM \_ 作業**。**RunDayOfWeek**"，"**CIM \_ 作業**。**RunStartInterval**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-252">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="4ad72-253">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="4ad72-253">This property is deprecated.</span></span> <span data-ttu-id="4ad72-254">建議您改用 **RunMonth**、 **RunDay**、 **RunDayOfWeek** 和 **RunStartInterval** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4ad72-254">Instead we recommend that you use the **RunMonth**, **RunDay**, **RunDayOfWeek**, and **RunStartInterval** properties.</span></span>

 

<span data-ttu-id="4ad72-255">排程目前作業開始的時間。</span><span class="sxs-lookup"><span data-stu-id="4ad72-255">The time when the current job is scheduled to start.</span></span> <span data-ttu-id="4ad72-256">這段時間可由日期和時程表示，或以相對於要求屬性時間的間隔來表示。</span><span class="sxs-lookup"><span data-stu-id="4ad72-256">This time can be represented by a date and time, or an interval relative to the time when the property is requested.</span></span> <span data-ttu-id="4ad72-257">全部為零的值表示作業已在執行中。</span><span class="sxs-lookup"><span data-stu-id="4ad72-257">A value of all zeroes indicates that the job is already executing.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-258">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-258">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-259">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-261">作業開始的時間。</span><span class="sxs-lookup"><span data-stu-id="4ad72-261">The time when the job started.</span></span> <span data-ttu-id="4ad72-262">這段時間可由日期和時程表示，或以相對於要求屬性時間的間隔來表示。</span><span class="sxs-lookup"><span data-stu-id="4ad72-262">This time can be represented by a date and time, or by an interval relative to the time when the property is requested.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-263">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="4ad72-263">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-264">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-264">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ad72-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-266">提交作業的時間。</span><span class="sxs-lookup"><span data-stu-id="4ad72-266">The time when the job was submitted.</span></span> <span data-ttu-id="4ad72-267">全部為零的值表示父項目不能報告日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4ad72-267">A value of all zeroes indicates that the parent element is not capable of reporting a date and time.</span></span>

</dd> <dt>

<span data-ttu-id="4ad72-268">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-268">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ad72-269">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4ad72-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-270">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4ad72-270">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4ad72-271">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業**」。**LocalOrUtcTime**") </span><span class="sxs-lookup"><span data-stu-id="4ad72-271">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**LocalOrUtcTime**")</span></span>
</dt> </dl>

<span data-ttu-id="4ad72-272">作業變成無效或應該停止的時間。</span><span class="sxs-lookup"><span data-stu-id="4ad72-272">The time after which the job becomes invalid or should be stopped.</span></span> <span data-ttu-id="4ad72-273">時間可以用日期和時程表示，或以相對於要求此屬性時間的間隔來表示。</span><span class="sxs-lookup"><span data-stu-id="4ad72-273">The time can be represented by a date and time, or by an interval relative to the time when this property is requested.</span></span> <span data-ttu-id="4ad72-274">所有九的值表示作業可以無限期執行。</span><span class="sxs-lookup"><span data-stu-id="4ad72-274">A value of all nines indicates that the job can run indefinitely.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ad72-275">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ad72-275">Requirements</span></span>



| <span data-ttu-id="4ad72-276">需求</span><span class="sxs-lookup"><span data-stu-id="4ad72-276">Requirement</span></span> | <span data-ttu-id="4ad72-277">值</span><span class="sxs-lookup"><span data-stu-id="4ad72-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad72-278">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ad72-278">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad72-279">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ad72-279">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4ad72-280">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ad72-280">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad72-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ad72-281">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4ad72-282">命名空間</span><span class="sxs-lookup"><span data-stu-id="4ad72-282">Namespace</span></span><br/>                | <span data-ttu-id="4ad72-283">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="4ad72-283">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4ad72-284">MOF</span><span class="sxs-lookup"><span data-stu-id="4ad72-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ad72-285"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4ad72-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ad72-286">DLL</span><span class="sxs-lookup"><span data-stu-id="4ad72-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ad72-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ad72-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ad72-288">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ad72-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ad72-289">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="4ad72-289">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

