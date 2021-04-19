---
description: 代表工作單位，用來追蹤非同步作業的進度。
ms.assetid: 33c13880-92a4-4367-8f0b-ecdf38b2ff8e
title: Msvm_ConcreteJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob
- Msvm_ConcreteJob.KillJob
- Msvm_ConcreteJob.InstanceID
- Msvm_ConcreteJob.Caption
- Msvm_ConcreteJob.Description
- Msvm_ConcreteJob.ElementName
- Msvm_ConcreteJob.InstallDate
- Msvm_ConcreteJob.Name
- Msvm_ConcreteJob.OperationalStatus
- Msvm_ConcreteJob.StatusDescriptions
- Msvm_ConcreteJob.Status
- Msvm_ConcreteJob.HealthState
- Msvm_ConcreteJob.CommunicationStatus
- Msvm_ConcreteJob.DetailedStatus
- Msvm_ConcreteJob.OperatingStatus
- Msvm_ConcreteJob.PrimaryStatus
- Msvm_ConcreteJob.JobStatus
- Msvm_ConcreteJob.TimeSubmitted
- Msvm_ConcreteJob.ScheduledStartTime
- Msvm_ConcreteJob.StartTime
- Msvm_ConcreteJob.ElapsedTime
- Msvm_ConcreteJob.JobRunTimes
- Msvm_ConcreteJob.RunMonth
- Msvm_ConcreteJob.RunDay
- Msvm_ConcreteJob.RunDayOfWeek
- Msvm_ConcreteJob.RunStartInterval
- Msvm_ConcreteJob.LocalOrUtcTime
- Msvm_ConcreteJob.UntilTime
- Msvm_ConcreteJob.Notify
- Msvm_ConcreteJob.Owner
- Msvm_ConcreteJob.Priority
- Msvm_ConcreteJob.PercentComplete
- Msvm_ConcreteJob.DeleteOnCompletion
- Msvm_ConcreteJob.ErrorCode
- Msvm_ConcreteJob.ErrorDescription
- Msvm_ConcreteJob.ErrorSummaryDescription
- Msvm_ConcreteJob.RecoveryAction
- Msvm_ConcreteJob.OtherRecoveryAction
- Msvm_ConcreteJob.JobState
- Msvm_ConcreteJob.TimeOfLastStateChange
- Msvm_ConcreteJob.TimeBeforeRemoval
- Msvm_ConcreteJob.Cancellable
- Msvm_ConcreteJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2cff9594bfd39cf365020a1da8ae2f1ec0aea562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985213"
---
# <a name="msvm_concretejob-class"></a><span data-ttu-id="4fb1a-103">Msvm \_ ConcreteJob 類別</span><span class="sxs-lookup"><span data-stu-id="4fb1a-103">Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="4fb1a-104">作業的實際版本。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-104">A concrete version of job.</span></span> <span data-ttu-id="4fb1a-105">此類別代表一般和 instantiatable 工作單位（例如批次或列印工作），特別用於 Hyper-v 以追蹤非同步作業的進度。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-105">This class represents a generic and instantiatable unit of work, such as a batch or a print job, and is specifically used in Hyper-V to track the progress of asynchronous operations.</span></span>

<span data-ttu-id="4fb1a-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb1a-107">語法</span><span class="sxs-lookup"><span data-stu-id="4fb1a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
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
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 
                00000000000500.000000:000
              ;
  boolean  Cancellable;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="4fb1a-108">成員</span><span class="sxs-lookup"><span data-stu-id="4fb1a-108">Members</span></span>

<span data-ttu-id="4fb1a-109">**Msvm \_ ConcreteJob** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4fb1a-109">The **Msvm\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="4fb1a-110">方法</span><span class="sxs-lookup"><span data-stu-id="4fb1a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4fb1a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4fb1a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4fb1a-112">方法</span><span class="sxs-lookup"><span data-stu-id="4fb1a-112">Methods</span></span>

<span data-ttu-id="4fb1a-113">**Msvm \_ ConcreteJob** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-113">The **Msvm\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="4fb1a-114">方法</span><span class="sxs-lookup"><span data-stu-id="4fb1a-114">Method</span></span>                                                            | <span data-ttu-id="4fb1a-115">描述</span><span class="sxs-lookup"><span data-stu-id="4fb1a-115">Description</span></span>                                                                      |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="4fb1a-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-116">**GetError**</span></span>](geterror-msvm-concretejob.md)                     | <span data-ttu-id="4fb1a-117">抓取作業的錯誤物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-117">Retrieves the error object for the job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="4fb1a-118">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-118">**GetErrorEx**</span></span>](geterrorex-msvm-concretejob.md)                 | <span data-ttu-id="4fb1a-119">抓取作業的錯誤物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-119">Retrieves the error objects for the job, if any exist.</span></span><br/>                |
| <span data-ttu-id="4fb1a-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-120">**KillJob**</span></span>                                                       | <span data-ttu-id="4fb1a-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-121">This method is not supported.</span></span><br/>                                         |
| [<span data-ttu-id="4fb1a-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-122">**RequestStateChange**</span></span>](requeststatechange-msvm-concretejob.md) | <span data-ttu-id="4fb1a-123">要求作業狀態變更為指定的狀態。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-123">Requests that the state of the job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4fb1a-124">屬性</span><span class="sxs-lookup"><span data-stu-id="4fb1a-124">Properties</span></span>

<span data-ttu-id="4fb1a-125">**Msvm \_ ConcreteJob** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-125">The **Msvm\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4fb1a-126">**可取消**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-127">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-129">指出是否可以取消作業。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="4fb1a-130">這個屬性的值不保證取消作業的要求將會成功。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-131">**標題**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-134">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-134">A short description of the object.</span></span> <span data-ttu-id="4fb1a-135">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-137">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-139">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4fb1a-140">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4fb1a-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-142">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-142">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-145">指定作業是否應該在完成時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-145">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="4fb1a-146">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-146">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-147">**說明**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-150">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-150">A description of the object.</span></span> <span data-ttu-id="4fb1a-151">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-152">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-152">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-153">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-155">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-155">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4fb1a-156">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4fb1a-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-158">**經過時間**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-158">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-159">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-161">作業已執行的時間間隔，或作業完成時的總執行時間。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-161">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="4fb1a-162">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-162">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-166">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-166">A display name for the object.</span></span> <span data-ttu-id="4fb1a-167">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-168">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-168">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-169">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-171">特定廠商的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-171">A vendor-specific error code.</span></span> <span data-ttu-id="4fb1a-172">如果作業已完成而沒有錯誤，則值必須設為零。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-172">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="4fb1a-173">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-173">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-174">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-174">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-177">包含廠商錯誤描述的字串。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-177">A string that contains the vendor error description.</span></span> <span data-ttu-id="4fb1a-178">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-178">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-179">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-179">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-182">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業**](cim-job.md)」。**ErrorCode**") </span><span class="sxs-lookup"><span data-stu-id="4fb1a-182">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-183">錯誤的摘要描述（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-183">A summary description of the error, if present.</span></span> <span data-ttu-id="4fb1a-184">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-184">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-185">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-185">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-186">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-188">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-188">The current health of the element.</span></span> <span data-ttu-id="4fb1a-189">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-189">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="4fb1a-190">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-190">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="4fb1a-191">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-192">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-192">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-193">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-195">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-195">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="4fb1a-196">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-200">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-201">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4fb1a-202">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-203">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-203">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-204">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-206">作業應該執行的次數。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-206">The number of times that the job should be run.</span></span> <span data-ttu-id="4fb1a-207">值為1表示作業不是週期性的，而任何非零值則表示作業將重複發生的次數限制。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-207">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="4fb1a-208">零表示作業可以處理的次數沒有任何限制，但會在到達 **UntilTime** 之後終止，否則會以手動方式結束作業，以終止作業。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-208">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="4fb1a-209">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-209">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-210">**JobState**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-210">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-211">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-213">**JobState** 是一個整數列舉，表示作業的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-213">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="4fb1a-214">它也可以表示這些狀態之間的轉換，例如「正在關機」和「啟動」。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-214">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="4fb1a-215">這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-215">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="4fb1a-216">值</span><span class="sxs-lookup"><span data-stu-id="4fb1a-216">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="4fb1a-217">意義</span><span class="sxs-lookup"><span data-stu-id="4fb1a-217">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="4fb1a-218"><dt>**新**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-218"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="4fb1a-219">作業從未啟動。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-219">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="4fb1a-220"><dt>**開始**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-220"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="4fb1a-221">這項作業會從 2 (新的) 、5 (暫止) 或 11 (服務) 狀態移到執行 (狀態的 4) 。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-221">The job is moving from the 2 (New), 5 (Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                   |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="4fb1a-222"><dt>**正在**</dt>執行 <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-222"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="4fb1a-223">工作正在執行。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-223">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="4fb1a-224">已 <dt>**暫**</dt>止 <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-224"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="4fb1a-225">作業已停止，但可以順暢的方式重新開機。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-225">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="4fb1a-226">正在 <dt>**關閉**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-226"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="4fb1a-227">工作正在移至 7 (完成) 、8 (終止) 或 9 (已終止) 狀態。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-227">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="4fb1a-228"><dt>**完成**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-228"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="4fb1a-229">作業已正常完成。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-229">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="4fb1a-230"><dt>**終止**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-230"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="4fb1a-231">作業已由「終止」狀態變更要求停止。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-231">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="4fb1a-232">作業和其所有基礎進程都已結束，而且只能以新的作業重新開機。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-232">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="4fb1a-233">只有當作業特定作業時，才需要重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-233">The requirement that the job be restarted only as a new job is job-specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="4fb1a-234">已 <dt>**終止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-234"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="4fb1a-235">作業已由「終止」狀態變更要求停止。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-235">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="4fb1a-236">基礎進程可能仍在執行中，而且可能需要進行清除以釋出資源。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-236">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="4fb1a-237"><dt>**例外**</dt>狀況 <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-237"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="4fb1a-238">作業處於異常狀態，可能表示發生錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-238">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="4fb1a-239">工作的實際狀態可能會透過工作專屬的物件提供。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-239">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="4fb1a-240"><dt>**服務**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-240"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="4fb1a-241">作業處於支援問題探索、解決或兩者的廠商特定狀態。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-241">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="4fb1a-242"><dt>**DMTF 保留**</dt>的 <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-242"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="4fb1a-243">保留的。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-243">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="4fb1a-244"><dt>**廠商保留**</dt>的 <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-244"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="4fb1a-245">保留的。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-245">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="4fb1a-246">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-246">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-249">表示作業狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-249">A string that represents the job status.</span></span> <span data-ttu-id="4fb1a-250">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-250">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-251">**JobType**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-251">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-252">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-254">指出此物件正在追蹤的作業類型。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-254">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4fb1a-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**定義虛擬機器** (1) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Define Virtual Machine** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**修改虛擬機器** (2) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modify Virtual Machine** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**銷毀虛擬機器** (3) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Destroy Virtual Machine** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>

<span data-ttu-id="4fb1a-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**修改管理服務設定** (4) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modify Management Service Settings** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span> (10) **初始化虛擬機器**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Initialize Virtual Machine** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**正在等候啟動虛擬機器** (11) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Waiting to Start Virtual Machine** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**啟動虛擬機器** (12) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Start Virtual Machine** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**關閉虛擬機器** (13) 的電源</span><span class="sxs-lookup"><span data-stu-id="4fb1a-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Power Off Virtual Machine** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**將虛擬機器儲存** (14) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Save Virtual Machine** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>將 **虛擬機器還原** (15) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restore Virtual Machine** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**關機虛擬機器** (16) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Shut Down Virtual Machine** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**暫停虛擬機器** (26) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Pause Virtual Machine** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**繼續虛擬機器** (27) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Resume Virtual Machine** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**重設虛擬機器** (28) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Reset Virtual Machine** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**重新開機虛擬機器** (29) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Reboot Virtual Machine** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="4fb1a-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**新增虛擬機器資源** (30) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Add Virtual Machine Resources** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="4fb1a-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**修改虛擬機器資源** (31) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modify Virtual Machine Resources** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="4fb1a-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span> (32) **移除虛擬機器資源**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Remove Virtual Machine Resources** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>

<span data-ttu-id="4fb1a-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**要求初始虛擬機器記憶體** (40) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Request Initial Virtual Machine Memory** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**將記憶體新增至虛擬機器** (41) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Add Memory to Virtual Machine** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**從虛擬機器** (42) 移除記憶體</span><span class="sxs-lookup"><span data-stu-id="4fb1a-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Remove Memory from Virtual Machine** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>

<span data-ttu-id="4fb1a-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**合併 VHD 磁片** (50) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Merging VHD Disks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**在虛擬機器中建立 VSS 快照** 集 (51) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Create VSS Snapshot inside Virtual Machine** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>

<span data-ttu-id="4fb1a-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**取得匯入設定資料** (60) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Get Import Setting Data** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>匯 **入虛擬機器** (61) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Import Virtual Machine** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**匯出虛擬機器** (62) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Export Virtual Machine** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>

<span data-ttu-id="4fb1a-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**註冊 Configuration** (63) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Register Configuration** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>

<span data-ttu-id="4fb1a-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**取消登錄 Configuration** (64) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Unregister Configuration** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Snapshot 虛擬機器** (70) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Snapshot Virtual Machine** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="4fb1a-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**將虛擬機器快照** 集套用 (71) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Apply Virtual Machine Snapshot** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="4fb1a-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span> (72) **刪除虛擬機器快照** 集</span><span class="sxs-lookup"><span data-stu-id="4fb1a-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Delete Virtual Machine Snapshot** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>

<span data-ttu-id="4fb1a-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**清除虛擬機器快照集狀態** (73) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Clear Virtual Machine Snapshot State** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>

<span data-ttu-id="4fb1a-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**將資源新增至資源集** 區 (80) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Add Resources to Resource Pool** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>

<span data-ttu-id="4fb1a-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**從資源集區移除資源** (81) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Remove Resources from Resource Pool** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>

<span data-ttu-id="4fb1a-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**修改 Replication Server Settings** (90) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modify Replication Server Settings** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="4fb1a-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**建立複寫關聯** 性 (91) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Create Replication Relationship** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>

<span data-ttu-id="4fb1a-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**修改複寫關聯性設定** (92) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modify Replication Relationship Settings** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="4fb1a-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**移除複寫關聯** 性 (93) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Remove Replication Relationship** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>

<span data-ttu-id="4fb1a-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**開始 Inband 初始** 複寫 (94) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Start Inband Initial Replication** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>

<span data-ttu-id="4fb1a-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>匯 **入** 複寫 (95) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Import Replication** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>

<span data-ttu-id="4fb1a-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>複寫 **狀態變更** (96) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Replicate State Change** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>

<span data-ttu-id="4fb1a-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**起始容錯移轉** (97) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Initiate Failover** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>

<span data-ttu-id="4fb1a-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**還原容錯移轉** (98) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Revert Failover** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>

<span data-ttu-id="4fb1a-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**認可容錯移轉** (99) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Commit Failover** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>

<span data-ttu-id="4fb1a-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Inititate 同步** 複寫 (100) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Inititate Synced Replication** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>

<span data-ttu-id="4fb1a-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**取消同步** 複寫 (101) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Cancel Synced Replication** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>

<span data-ttu-id="4fb1a-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**起始測試複本** (102) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Initiate Test Replica** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>

<span data-ttu-id="4fb1a-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**移除測試複本** (103) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Remove Test Replica** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>

<span data-ttu-id="4fb1a-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**反向** 複寫 (104) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Reverse Replication** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>

<span data-ttu-id="4fb1a-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>複寫 **傳送 Delta** (105) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Replication Sending Delta** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>

<span data-ttu-id="4fb1a-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>複寫 **接收 Delta** (106) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Replication Receiving Delta** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="4fb1a-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>重新 **同步** 處理 (107) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>

<span data-ttu-id="4fb1a-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**將變更記錄** 檔 (108) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Apply change log** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>

<span data-ttu-id="4fb1a-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**停止初始** 複寫 (109) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Stop Initial Replication** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>

<span data-ttu-id="4fb1a-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**停止重新同步** 處理 (110) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Stop Resynchronizing** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>

<span data-ttu-id="4fb1a-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**取得複本統計資料** (111) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Get Replica statistics** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="4fb1a-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**準備一致性檢查程式** (112) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Prepare for Consistency Checker** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>

<span data-ttu-id="4fb1a-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**一致性檢查** 程式 (113) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Consistency Checker** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="4fb1a-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**停止一致性檢查** 程式 (114) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Stop Consistency Checker** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>

<span data-ttu-id="4fb1a-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**測試複寫連接** (115) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Test Replication Connection** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>

<span data-ttu-id="4fb1a-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>正在傳送 **初始複本** (116) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Sending Initial Replica** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>

<span data-ttu-id="4fb1a-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**開始重新同步初始** 複寫 (117) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Start Resync Initial Replication** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>

<span data-ttu-id="4fb1a-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**開始匯出初始** 複寫 (118) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Start Export Initial Replication** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>

<span data-ttu-id="4fb1a-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**重設複本統計資料** (119) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Reset Replica Statistics** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>

<span data-ttu-id="4fb1a-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**將已註冊** 的差異套用 (120) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Apply Registered Deltas** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>

<span data-ttu-id="4fb1a-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>重新 **同步處理擴充** 複寫 (121) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Resynchronizing Extended Replication** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>

<span data-ttu-id="4fb1a-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**正在讀取測試複本** 設定 (122) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Reading Test Replica Configuration** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>

<span data-ttu-id="4fb1a-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>將複寫 **模式變更為主要** (123) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Change the replication mode to primary** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>

<span data-ttu-id="4fb1a-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**起始容錯回復** (124) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Initiate Failback** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>

<span data-ttu-id="4fb1a-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**更新磁片集** (125) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Update Disk Set** (125)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-326">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-326">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>

<span data-ttu-id="4fb1a-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**定義乙太網路交換器** (130) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Define Ethernet Switch** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>

<span data-ttu-id="4fb1a-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**修改乙太網路交換器設定** (131) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modify Ethernet Switch Settings** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>

<span data-ttu-id="4fb1a-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**銷毀乙太網路交換器** (132) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Destroy Ethernet Switch** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="4fb1a-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**將乙太網路交換器資源新增** (133) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Add Ethernet Switch Resources** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="4fb1a-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**修改乙太網路交換器資源** (134) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modify Ethernet Switch Resources** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="4fb1a-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**移除乙太網路交換器資源** (135) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Remove Ethernet Switch Resources** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**驗證規劃的虛擬機器** (140) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Validate Planned Virtual Machine** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span> (141) **實現虛擬機器**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizing Virtual Machine** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>

<span data-ttu-id="4fb1a-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**建立資源集** 區 (150) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Creating a Resource Pool** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="4fb1a-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**變更資源集區的父資源** (151) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Changing the Parent Resources of a Resource Pool** (151)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="4fb1a-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**變更資源集區的非 Alloction 設定** (152) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Changing the Non-alloction Settings of a Resource Pool** (152)</span></span>


</dt> <dd></dd> <dt>

<span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>

<span data-ttu-id="4fb1a-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span> (153) **刪除資源集** 區</span><span class="sxs-lookup"><span data-stu-id="4fb1a-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Deleting a Resource Pool** (153)</span></span>


</dt> <dd></dd> <dt>

<span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="4fb1a-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**啟用 REMOTEFX GPU** (160) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Enable RemoteFx GPU** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="4fb1a-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**停用 REMOTEFX GPU** (161) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Disable RemoteFx GPU** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>

<span data-ttu-id="4fb1a-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**修改3D 服務設定** (162) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modify 3D Service Settings** (162)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-342">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-342">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>

<span data-ttu-id="4fb1a-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**備份虛擬機器** (170) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Backup Virtual Machine** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>

<span data-ttu-id="4fb1a-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**來賓服務介面** (180) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Guest Service Interface** (180)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-345">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-345">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>

<span data-ttu-id="4fb1a-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**查詢來賓叢集資訊** (181) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Query Guest Cluster Information** (181)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-347">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-347">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>

<span data-ttu-id="4fb1a-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**定義集合** (190) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Define Collection** (190)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-349">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-349">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>

<span data-ttu-id="4fb1a-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**銷毀收集** (191) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destroy Collection** (191)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-351">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-351">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>

<span data-ttu-id="4fb1a-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**重新命名集合** (192) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Rename Collection** (192)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-353">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-353">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>

<span data-ttu-id="4fb1a-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**將成員新增至集合** (193) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Add Member to Collection** (193)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-355">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-355">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>

<span data-ttu-id="4fb1a-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**從集合中移除成員** (194) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Remove Member from Collection** (194)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-357">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-357">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>

<span data-ttu-id="4fb1a-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**將設定新增至集合** (195) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Add Setting to Collection** (195)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-359">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-359">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>

<span data-ttu-id="4fb1a-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**從集合中移除設定** (196) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Remove Setting from Collection** (196)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-361">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-361">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>

<span data-ttu-id="4fb1a-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**修改集合 (197) 上的設定**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modify Setting on Collection** (197)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-363">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-363">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>

<span data-ttu-id="4fb1a-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span> (198) 的 **快照集集合**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Snapshot Collection** (198)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-365">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-365">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>

<span data-ttu-id="4fb1a-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**將快照集轉換為參考點** (200) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convert Snapshot to Reference Point** (200)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-367">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-367">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>

<span data-ttu-id="4fb1a-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**建立參考點** (201) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Create Reference Point** (201)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-369">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-369">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>

<span data-ttu-id="4fb1a-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**刪除參考點** (202) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Delete Reference Point** (202)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-371">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-371">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>

<span data-ttu-id="4fb1a-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**匯出參考點** (203) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Export Reference Point** (203)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-373">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-373">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>

<span data-ttu-id="4fb1a-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**從參考點移除相關聯的資料** (204) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Remove Associated Data from Reference Point** (204)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-375">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-375">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="4fb1a-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**在集合上建立參考點** (205) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Create Reference Point on Collection** (205)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-377">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-377">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="4fb1a-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>將 **集合上的參考點匯出** (206) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Export Reference Point on Collection** (206)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-379">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-379">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="4fb1a-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**從集合上的參考點移除相關聯的資料** (207) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Remove Associated Data from Reference Point on Collection** (207)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-381">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-381">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="4fb1a-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**刪除集合上的參考點** (208) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Delete Reference Point on Collection** (208)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-383">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-383">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>

<span data-ttu-id="4fb1a-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>匯 **入參考點中繼資料** (209) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Import Reference Point metadata** (209)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-385">在 Windows 10 中新增為 **清除參考點** 的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-385">Value added in Windows 10 as **Cleanup Reference Point**.</span></span>

 

</dd> <dt>

<span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>

<span data-ttu-id="4fb1a-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**裝載或卸載可指派的裝置** (260) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Mount or Dismount Assignable Device** (260)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="4fb1a-387">在 Windows 10 中新增的值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-387">Value added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4fb1a-388">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-388">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-389">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-391">指出 **RunStartInterval** 和 **UntilTime** 屬性中所表示的時間是否代表當地時間或 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-391">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="4fb1a-392">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="4fb1a-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**本地時間** (1) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC 時間** (2 ) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4fb1a-395">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-395">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-396">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-398">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-398">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-399">此作業實例的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-399">The display name for this instance of a job.</span></span> <span data-ttu-id="4fb1a-400">此外，顯示名稱可用來做為搜尋或查詢的屬性。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-400">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="4fb1a-401">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-402">**通知**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-402">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-405">在作業完成或失敗時收到通知的使用者。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-405">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="4fb1a-406">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-406">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-407">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-407">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-408">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-410">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-410">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4fb1a-411">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4fb1a-412">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-414">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4fb1a-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-416">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-416">The current statuses of the object.</span></span> <span data-ttu-id="4fb1a-417">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-418">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-418">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-419">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-421">字串，描述當實例的 **RecoveryAction** 屬性為 1 (其他) 時的復原動作。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-421">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="4fb1a-422">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-422">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-423">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-423">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-426">提交作業的使用者。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-426">The user who submitted the job.</span></span> <span data-ttu-id="4fb1a-427">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-427">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-428">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-428">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-429">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-431">限定詞： **MinValue** ( 0 ) ， **int32.maxvalue ( 100** ) ， **單位** ( "Percent" ) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-431">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-432">作業的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-432">The completion percentage of the job.</span></span> <span data-ttu-id="4fb1a-433">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-433">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-434">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-434">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-435">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-437">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-437">Provides high level status information.</span></span> <span data-ttu-id="4fb1a-438">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-438">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4fb1a-439">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-439">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4fb1a-440">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-440">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-441">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-441">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-442">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-442">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-444">作業執行的重要性。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-444">The importance of a job's execution.</span></span> <span data-ttu-id="4fb1a-445">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-445">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-446">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-446">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-447">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-448">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-449">描述未成功執行的作業所要採取的復原動作。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-449">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="4fb1a-450">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-450">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="4fb1a-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**請勿繼續** (2) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**繼續進行下一個工作** (3) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span> (4) **重新執行作業**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**執行復原工作** (5 ) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4fb1a-457">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-457">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-458">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-458">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-459">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-460">限定詞： **MinValue** (-31 ) 、 **int32.maxvalue ( 31** ) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-460">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-461">應處理作業之月份的日期。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-461">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="4fb1a-462">根據 **RunDayOfWeek** 的值，此屬性有不同的解釋。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-462">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="4fb1a-463">當 **RunDayOfWeek** 為0，而 **RunDay** 為正數時， **RunDay** 會定義處理作業的月份日期。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-463">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="4fb1a-464">例如，如果 **RunDayOfWeek** 為0，而 **RunDay** 為12，則會在當月 <sup>的12天</sup> 處理工作。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-464">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="4fb1a-465">當 **RunDayOfWeek** 為0，而 **RunDay** 為負數時， **RunDay** 會定義處理工作的當月最後一天之前的天數。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-465">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="4fb1a-466">1表示當月最後一天，2表示當月最後一天之前的一天，依此類推。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-466">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="4fb1a-467">例如，如果 **RunDayOfWeek** 是0，而 **RunDay** 是1，則會在當月的最後一天處理工作。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-467">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="4fb1a-468">當 **RunDayOfWeek** 不是0時， **RunDayOfWeek** 是將處理作業的星期幾（相對於 **RunDay**）。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-468">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="4fb1a-469">例如，如果 **RunDay** 為15，而 **RunDayOfWeek** 為 7 (+ 星期六) ，則工作會在每 <sup>月15日</sup> 的第一個星期六或之後處理。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-469">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="4fb1a-470">如果 **RunDay** 為20，而 **RunDayOfWeek** 為 7 ( 星期六) ，則會在當月 <sup>的20天</sup> 前或之前的第一個星期六處理工作。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-470">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="4fb1a-471">如果 **RunDay** 是1，而 **RunDayOfWeek** 是 1 ( 星期日) ，則會在當月的最後一個星期日處理工作。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-471">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="4fb1a-472">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-472">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-473">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-473">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-474">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-474">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-476">與 **RunDay** 搭配使用的正整數或負整數，表示處理作業的周中日或月中的日。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-476">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="4fb1a-477">如需詳細資訊，請參閱 **RunDay** 屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-477">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="4fb1a-478">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-478">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="4fb1a-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-星期六** ( 7) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-星期五** ( 6) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-星期四** ( 5) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-星期三** ( 4) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-星期二** ( 3) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-星期一** ( 2) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-星期日** ( 1) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**星期日** (1) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**星期一** (2) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**星期二** (3) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**星期三** (4) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**星期四** (5) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**星期五** (6) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**星期六** (7 ) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4fb1a-494">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-494">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-495">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-495">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-496">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-497">應處理作業的月份。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-497">The month during which the job should be processed.</span></span> <span data-ttu-id="4fb1a-498">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-498">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="4fb1a-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**1 月** (0) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**二月** (1) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**3 月** (2) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**四月** (3) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**5 月** (4) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**6 月** (5) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**7 月** (6) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**8 月** (7) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**9 月** (8) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**10 月** (9) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**11 月** (10) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**12 月** (11 ) </span><span class="sxs-lookup"><span data-stu-id="4fb1a-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4fb1a-511">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-511">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-512">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-512">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-513">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-514">應處理作業的午夜之後的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-514">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="4fb1a-515">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-515">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-516">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-516">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-517">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-517">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-518">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-519">工作的排程開始時間（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-519">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="4fb1a-520">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-520">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-521">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-521">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-522">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-522">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-523">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-524">作業開始的時間。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-524">The time that the job began.</span></span> <span data-ttu-id="4fb1a-525">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-525">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-526">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-526">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-527">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-528">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-528">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-529">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-530">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-531">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="4fb1a-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-532">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-533">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4fb1a-534">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-535">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-535">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-536">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-536">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-537">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-538">作業完成執行後的保留時間（以分鐘為單位），這是在該執行中的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-538">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="4fb1a-539">無論 **DeleteOnCompletion** 屬性的值為何，此作業都必須保持存在一段時間。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-539">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="4fb1a-540">預設為五分鐘。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-540">The default is five minutes.</span></span> <span data-ttu-id="4fb1a-541">這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))，而且一律設定為00000000000500.000000：000。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-541">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-543">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-544">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-545">上次變更工作狀態的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-545">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="4fb1a-546">如果作業的狀態未變更，而且此屬性已填入，則必須將它設定為0間隔值。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-546">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="4fb1a-547">如果已要求狀態變更但遭到拒絕或尚未處理，則無法更新屬性。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-547">If a state change was requested but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="4fb1a-548">這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-548">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-549">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-549">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-550">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-550">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-551">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-551">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-552">提交作業的時間。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-552">The time that the job was submitted.</span></span> <span data-ttu-id="4fb1a-553">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-553">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="4fb1a-554">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-554">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fb1a-555">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-555">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4fb1a-556">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4fb1a-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fb1a-557">作業無效或應該停止的時間。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-557">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="4fb1a-558">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-558">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fb1a-559">備註</span><span class="sxs-lookup"><span data-stu-id="4fb1a-559">Remarks</span></span>

<span data-ttu-id="4fb1a-560">存取 **Msvm \_ ConcreteJob** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-560">Access to the **Msvm\_ConcreteJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4fb1a-561">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="4fb1a-561">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb1a-562">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fb1a-562">Requirements</span></span>



| <span data-ttu-id="4fb1a-563">需求</span><span class="sxs-lookup"><span data-stu-id="4fb1a-563">Requirement</span></span> | <span data-ttu-id="4fb1a-564">值</span><span class="sxs-lookup"><span data-stu-id="4fb1a-564">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb1a-565">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fb1a-565">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb1a-566">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fb1a-566">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4fb1a-567">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fb1a-567">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb1a-568">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fb1a-568">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4fb1a-569">命名空間</span><span class="sxs-lookup"><span data-stu-id="4fb1a-569">Namespace</span></span><br/>                | <span data-ttu-id="4fb1a-570">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4fb1a-570">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4fb1a-571">MOF</span><span class="sxs-lookup"><span data-stu-id="4fb1a-571">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fb1a-572"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-572"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fb1a-573">DLL</span><span class="sxs-lookup"><span data-stu-id="4fb1a-573">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fb1a-574"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4fb1a-574"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4fb1a-575">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fb1a-575">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb1a-576">**CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="4fb1a-576">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="4fb1a-577">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4fb1a-577">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4fb1a-578">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="4fb1a-578">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

