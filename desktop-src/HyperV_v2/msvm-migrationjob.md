---
description: 此類別代表由虛擬系統移轉服務為儲存或虛擬系統移轉所建立的遷移作業工作。
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Msvm_MigrationJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989318"
---
# <a name="msvm_migrationjob-class"></a><span data-ttu-id="dd123-103">Msvm \_ MigrationJob 類別</span><span class="sxs-lookup"><span data-stu-id="dd123-103">Msvm\_MigrationJob class</span></span>

<span data-ttu-id="dd123-104">此類別代表由虛擬系統移轉服務為儲存或虛擬系統移轉所建立的遷移作業工作。</span><span class="sxs-lookup"><span data-stu-id="dd123-104">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span>

<span data-ttu-id="dd123-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dd123-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd123-106">語法</span><span class="sxs-lookup"><span data-stu-id="dd123-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
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
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="dd123-107">成員</span><span class="sxs-lookup"><span data-stu-id="dd123-107">Members</span></span>

<span data-ttu-id="dd123-108">**Msvm \_ MigrationJob** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dd123-108">The **Msvm\_MigrationJob** class has these types of members:</span></span>

-   [<span data-ttu-id="dd123-109">方法</span><span class="sxs-lookup"><span data-stu-id="dd123-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd123-110">屬性</span><span class="sxs-lookup"><span data-stu-id="dd123-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd123-111">方法</span><span class="sxs-lookup"><span data-stu-id="dd123-111">Methods</span></span>

<span data-ttu-id="dd123-112">**Msvm \_ MigrationJob** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dd123-112">The **Msvm\_MigrationJob** class has these methods.</span></span>



| <span data-ttu-id="dd123-113">方法</span><span class="sxs-lookup"><span data-stu-id="dd123-113">Method</span></span>                                                             | <span data-ttu-id="dd123-114">描述</span><span class="sxs-lookup"><span data-stu-id="dd123-114">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd123-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="dd123-115">**GetError**</span></span>](geterror-msvm-migrationjob.md)                     | <span data-ttu-id="dd123-116">抓取遷移作業的錯誤物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="dd123-116">Retrieves the error object for the migration job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="dd123-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="dd123-117">**GetErrorEx**</span></span>](geterrorex-msvm-migrationjob.md)                 | <span data-ttu-id="dd123-118">抓取遷移作業的錯誤物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="dd123-118">Retrieves the error objects for the migration job, if any exist.</span></span><br/>                |
| <span data-ttu-id="dd123-119">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="dd123-119">**KillJob**</span></span>                                                        | <span data-ttu-id="dd123-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="dd123-120">This method is not supported.</span></span><br/>                                                   |
| [<span data-ttu-id="dd123-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="dd123-121">**RequestStateChange**</span></span>](requeststatechange-msvm-migrationjob.md) | <span data-ttu-id="dd123-122">要求將遷移作業的狀態變更為指定的狀態。</span><span class="sxs-lookup"><span data-stu-id="dd123-122">Requests that the state of the migration job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dd123-123">屬性</span><span class="sxs-lookup"><span data-stu-id="dd123-123">Properties</span></span>

<span data-ttu-id="dd123-124">**Msvm \_ MigrationJob** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dd123-124">The **Msvm\_MigrationJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd123-125">**可取消**</span><span class="sxs-lookup"><span data-stu-id="dd123-125">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-126">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dd123-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-128">指出是否可以取消作業。</span><span class="sxs-lookup"><span data-stu-id="dd123-128">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="dd123-129">這個屬性的值不保證取消作業的要求將會成功。</span><span class="sxs-lookup"><span data-stu-id="dd123-129">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-130">**標題**</span><span class="sxs-lookup"><span data-stu-id="dd123-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-133">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="dd123-133">A short description of the object.</span></span> <span data-ttu-id="dd123-134">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="dd123-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-135">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="dd123-135">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-136">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-138">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="dd123-138">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="dd123-139">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="dd123-139">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dd123-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dd123-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-141">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="dd123-141">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dd123-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-144">指定作業是否應該在完成時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="dd123-144">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="dd123-145">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-145">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-146">**說明**</span><span class="sxs-lookup"><span data-stu-id="dd123-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-149">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="dd123-149">A description of the object.</span></span> <span data-ttu-id="dd123-150">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="dd123-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-151">**DestinationHost**</span><span class="sxs-lookup"><span data-stu-id="dd123-151">**DestinationHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-154">虛擬系統正在遷移的目的地虛擬化平臺的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="dd123-154">The hostname of the destination virtualization platform that the virtual system is migrating to.</span></span> <span data-ttu-id="dd123-155">儲存體遷移將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dd123-155">This will be **Null** for storage migration.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="dd123-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-157">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-159">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dd123-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="dd123-160">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="dd123-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dd123-161">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dd123-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-162">**經過時間**</span><span class="sxs-lookup"><span data-stu-id="dd123-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-163">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dd123-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-165">作業已執行的時間間隔，或作業完成時的總執行時間。</span><span class="sxs-lookup"><span data-stu-id="dd123-165">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="dd123-166">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dd123-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-170">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="dd123-170">A display name for the object.</span></span> <span data-ttu-id="dd123-171">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="dd123-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dd123-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-173">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-175">特定廠商的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dd123-175">A vendor-specific error code.</span></span> <span data-ttu-id="dd123-176">如果作業已完成而沒有錯誤，則值必須設為零。</span><span class="sxs-lookup"><span data-stu-id="dd123-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="dd123-177">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dd123-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-181">包含廠商錯誤描述的字串。</span><span class="sxs-lookup"><span data-stu-id="dd123-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="dd123-182">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="dd123-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd123-186">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業**](cim-job.md)」。**ErrorCode**") </span><span class="sxs-lookup"><span data-stu-id="dd123-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="dd123-187">錯誤的摘要描述（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="dd123-187">A summary description of the error, if present.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-188">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="dd123-188">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-189">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-191">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="dd123-191">The current health of the element.</span></span> <span data-ttu-id="dd123-192">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="dd123-192">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="dd123-193">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="dd123-193">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="dd123-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="dd123-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dd123-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-196">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dd123-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-198">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="dd123-198">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="dd123-199">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dd123-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-200">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd123-200">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd123-203">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="dd123-203">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dd123-204">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="dd123-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dd123-205">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dd123-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-206">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="dd123-206">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-207">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dd123-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-209">作業應該執行的次數。</span><span class="sxs-lookup"><span data-stu-id="dd123-209">The number of times that the job should be run.</span></span> <span data-ttu-id="dd123-210">值為1表示作業不是週期性的，而任何非零值則表示作業將重複發生的次數限制。</span><span class="sxs-lookup"><span data-stu-id="dd123-210">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="dd123-211">零表示作業可以處理的次數沒有任何限制，但會在到達 **UntilTime** 之後終止，否則會以手動方式結束作業，以終止作業。</span><span class="sxs-lookup"><span data-stu-id="dd123-211">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="dd123-212">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-212">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-213">**JobState**</span><span class="sxs-lookup"><span data-stu-id="dd123-213">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-214">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-216">**JobState** 是一個整數列舉，表示作業的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="dd123-216">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="dd123-217">它也可以表示這些狀態之間的轉換，例如「正在關機」和「啟動」。</span><span class="sxs-lookup"><span data-stu-id="dd123-217">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="dd123-218">這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="dd123-218">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="dd123-219">值</span><span class="sxs-lookup"><span data-stu-id="dd123-219">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="dd123-220">意義</span><span class="sxs-lookup"><span data-stu-id="dd123-220">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="dd123-221"><dt>**新**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-221"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="dd123-222">作業從未啟動。</span><span class="sxs-lookup"><span data-stu-id="dd123-222">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="dd123-223"><dt>**開始**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-223"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="dd123-224">這項作業會從 2 (新的) 、5 (暫止) 或 11 (服務) 狀態移到執行 (狀態的 4) 。</span><span class="sxs-lookup"><span data-stu-id="dd123-224">The job is moving from the 2 (New), 5(Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="dd123-225"><dt>**正在**</dt>執行 <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-225"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="dd123-226">工作正在執行。</span><span class="sxs-lookup"><span data-stu-id="dd123-226">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="dd123-227">已 <dt>**暫**</dt>止 <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-227"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="dd123-228">作業已停止，但可以順暢的方式重新開機。</span><span class="sxs-lookup"><span data-stu-id="dd123-228">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="dd123-229">正在 <dt>**關閉**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-229"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="dd123-230">工作正在移至 7 (完成) 、8 (終止) 或 9 (已終止) 狀態。</span><span class="sxs-lookup"><span data-stu-id="dd123-230">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="dd123-231"><dt>**完成**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-231"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="dd123-232">作業已正常完成。</span><span class="sxs-lookup"><span data-stu-id="dd123-232">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="dd123-233"><dt>**終止**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-233"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="dd123-234">作業已由「終止」狀態變更要求停止。</span><span class="sxs-lookup"><span data-stu-id="dd123-234">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="dd123-235">作業和其所有基礎進程都已結束，而且只能以新的作業重新開機。</span><span class="sxs-lookup"><span data-stu-id="dd123-235">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="dd123-236">只有當工作為特定作業時，才需要重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="dd123-236">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="dd123-237">已 <dt>**終止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-237"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="dd123-238">作業已由「終止」狀態變更要求停止。</span><span class="sxs-lookup"><span data-stu-id="dd123-238">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="dd123-239">基礎進程可能仍在執行中，而且可能需要進行清除以釋出資源。</span><span class="sxs-lookup"><span data-stu-id="dd123-239">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="dd123-240"><dt>**例外**</dt>狀況 <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-240"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="dd123-241">作業處於異常狀態，可能表示發生錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="dd123-241">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="dd123-242">工作的實際狀態可能會透過工作專屬的物件提供。</span><span class="sxs-lookup"><span data-stu-id="dd123-242">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="dd123-243"><dt>**服務**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-243"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="dd123-244">作業處於支援問題探索、解決或兩者的廠商特定狀態。</span><span class="sxs-lookup"><span data-stu-id="dd123-244">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="dd123-245"><dt>**DMTF 保留**</dt>的 <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-245"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="dd123-246">保留的。</span><span class="sxs-lookup"><span data-stu-id="dd123-246">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="dd123-247"><dt>**廠商保留**</dt>的 <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-247"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="dd123-248">保留的。</span><span class="sxs-lookup"><span data-stu-id="dd123-248">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="dd123-249">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="dd123-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-250">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-252">表示作業狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="dd123-252">A string that represents the job status.</span></span> <span data-ttu-id="dd123-253">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-253">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-254">**JobType**</span><span class="sxs-lookup"><span data-stu-id="dd123-254">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-255">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-257">指出此物件正在追蹤的作業類型。</span><span class="sxs-lookup"><span data-stu-id="dd123-257">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd123-258">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="dd123-258">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="dd123-259">**正在建立遠端虛擬機器** (300) </span><span class="sxs-lookup"><span data-stu-id="dd123-259">**Creating Remote Virtual Machine** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

<span data-ttu-id="dd123-260">**檢查虛擬機器相容性** (301) </span><span class="sxs-lookup"><span data-stu-id="dd123-260">**Checking Virtual Machine Compatibility** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="dd123-261">**檢查虛擬機器和存放裝置相容性** (302) </span><span class="sxs-lookup"><span data-stu-id="dd123-261">**Checking Virtual Machine and Storage Compatibility** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="dd123-262">**檢查儲存體相容性** (303) </span><span class="sxs-lookup"><span data-stu-id="dd123-262">**Checking Storage Compatibility** (303)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

<span data-ttu-id="dd123-263">**檢查儲存體遷移** (304) </span><span class="sxs-lookup"><span data-stu-id="dd123-263">**Checking Storage Migration** (304)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="dd123-264"> (305) **移動虛擬機器**</span><span class="sxs-lookup"><span data-stu-id="dd123-264">**Moving Virtual Machine** (305)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

<span data-ttu-id="dd123-265">**移動虛擬機器和儲存體** (306) </span><span class="sxs-lookup"><span data-stu-id="dd123-265">**Moving Virtual Machine and Storage** (306)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

<span data-ttu-id="dd123-266">**移動儲存體** (307) </span><span class="sxs-lookup"><span data-stu-id="dd123-266">**Moving Storage** (307)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd123-267">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="dd123-267">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-268">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-270">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-270">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<span data-ttu-id="dd123-271">指出 **RunStartInterval** 和 **UntilTime** 屬性中所表示的時間是否代表當地時間或 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="dd123-271">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dl> <dt>

<span data-ttu-id="dd123-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**本地時間** (1) </span><span class="sxs-lookup"><span data-stu-id="dd123-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC 時間** (2 ) </span><span class="sxs-lookup"><span data-stu-id="dd123-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd123-274">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="dd123-274">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-275">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd123-277">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)。**MigrationType**") </span><span class="sxs-lookup"><span data-stu-id="dd123-277">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span></span>
</dt> </dl>

<span data-ttu-id="dd123-278">此工作物件所表示的遷移類型。</span><span class="sxs-lookup"><span data-stu-id="dd123-278">The migration type represented by this job object.</span></span> <span data-ttu-id="dd123-279">這會是針對 [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)類別的 **MigrationType** 屬性所定義的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dd123-279">This will be one of the values defined for the **MigrationType** property of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-280">**名稱**</span><span class="sxs-lookup"><span data-stu-id="dd123-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-281">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd123-283">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="dd123-283">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dd123-284">此作業實例的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="dd123-284">The display name for this instance of a job.</span></span> <span data-ttu-id="dd123-285">此外，顯示名稱可用來做為搜尋或查詢的屬性。</span><span class="sxs-lookup"><span data-stu-id="dd123-285">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="dd123-286">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dd123-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-287">**NewResourceSettingData**</span><span class="sxs-lookup"><span data-stu-id="dd123-287">**NewResourceSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-288">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="dd123-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dd123-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-290">針對即時移轉，這一律會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dd123-290">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="dd123-291">針對儲存體遷移，如果這是 **Null**，則不會移動任何虛擬機器的虛擬硬碟 (vhd) 。</span><span class="sxs-lookup"><span data-stu-id="dd123-291">For a storage migration, if this is **Null**, none of the virtual machine's virtual hard disks (VHDs) will be moved.</span></span> <span data-ttu-id="dd123-292">否則，這會包含 [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) 類別的內嵌實例陣列，代表要移動的 vhd。</span><span class="sxs-lookup"><span data-stu-id="dd123-292">Otherwise, this will contain an array of embedded instances of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class that represent the VHDs to be moved.</span></span> <span data-ttu-id="dd123-293">這些實例的 **連接** 屬性會指定 VHD 的目的地位置。</span><span class="sxs-lookup"><span data-stu-id="dd123-293">The **Connection** property of these instances will specify the destination location of the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-294">**NewSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="dd123-294">**NewSystemSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-297">針對即時移轉，這一律會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dd123-297">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="dd123-298">針對儲存體遷移，如果這是 **Null**，則不會移動虛擬機器的資料根。</span><span class="sxs-lookup"><span data-stu-id="dd123-298">For a storage migration, if this is **Null**, the virtual machine's data roots are not moving.</span></span> <span data-ttu-id="dd123-299">否則，這會包含 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別的內嵌實例，其中 **ExternalDataRoot**、 **SnapshotDataRoot** 和 **SwapFileDataRoot** 屬性會指定新的資料根。</span><span class="sxs-lookup"><span data-stu-id="dd123-299">Otherwise, this will contain an embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class, where the **ExternalDataRoot**, **SnapshotDataRoot**, and **SwapFileDataRoot** properties will specify the new data roots.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-300">**通知**</span><span class="sxs-lookup"><span data-stu-id="dd123-300">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-303">在作業完成或失敗時收到通知的使用者。</span><span class="sxs-lookup"><span data-stu-id="dd123-303">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="dd123-304">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-304">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-305">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="dd123-305">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-306">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-308">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dd123-308">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="dd123-309">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="dd123-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dd123-310">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dd123-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="dd123-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-312">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="dd123-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dd123-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-314">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="dd123-314">The current statuses of the object.</span></span> <span data-ttu-id="dd123-315">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="dd123-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-316">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="dd123-316">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-319">字串，描述當實例的 **RecoveryAction** 屬性為 1 (其他) 時的復原動作。</span><span class="sxs-lookup"><span data-stu-id="dd123-319">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="dd123-320">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-320">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-321">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="dd123-321">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-324">提交作業的使用者。</span><span class="sxs-lookup"><span data-stu-id="dd123-324">The user who submitted the job.</span></span> <span data-ttu-id="dd123-325">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-325">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-326">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="dd123-326">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-327">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd123-329">限定詞： **MinValue** ( 0 ) ， **int32.maxvalue ( 100** ) ， **單位** ( "Percent" ) </span><span class="sxs-lookup"><span data-stu-id="dd123-329">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="dd123-330">作業的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="dd123-330">The completion percentage of the job.</span></span> <span data-ttu-id="dd123-331">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-331">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-332">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="dd123-332">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-333">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-333">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-335">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="dd123-335">Provides high level status information.</span></span> <span data-ttu-id="dd123-336">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="dd123-336">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="dd123-337">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="dd123-337">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dd123-338">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dd123-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-339">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="dd123-339">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-340">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dd123-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-342">作業執行的重要性。</span><span class="sxs-lookup"><span data-stu-id="dd123-342">The importance of a job's execution.</span></span> <span data-ttu-id="dd123-343">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-343">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-344">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="dd123-344">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-345">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dd123-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-347">描述針對失敗的執行作業所要採取的復原動作。</span><span class="sxs-lookup"><span data-stu-id="dd123-347">Describes the recovery action to be taken for an unsuccessfully run job.</span></span> <span data-ttu-id="dd123-348">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-348">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="dd123-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="dd123-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="dd123-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**請勿繼續** (2) </span><span class="sxs-lookup"><span data-stu-id="dd123-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**繼續進行下一個工作** (3) </span><span class="sxs-lookup"><span data-stu-id="dd123-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span> (4) **重新執行作業**</span><span class="sxs-lookup"><span data-stu-id="dd123-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**執行復原工作** (5 ) </span><span class="sxs-lookup"><span data-stu-id="dd123-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd123-355">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="dd123-355">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-356">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="dd123-356">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd123-358">限定詞： **MinValue** (-31 ) 、 **int32.maxvalue ( 31** ) </span><span class="sxs-lookup"><span data-stu-id="dd123-358">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="dd123-359">應處理作業之月份的日期。</span><span class="sxs-lookup"><span data-stu-id="dd123-359">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="dd123-360">根據 **RunDayOfWeek** 的值，此屬性有不同的解釋。</span><span class="sxs-lookup"><span data-stu-id="dd123-360">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="dd123-361">當 **RunDayOfWeek** 為0，而 **RunDay** 為正數時， **RunDay** 會定義處理作業的月份日期。</span><span class="sxs-lookup"><span data-stu-id="dd123-361">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="dd123-362">例如，如果 **RunDayOfWeek** 為0，而 **RunDay** 為12，則會在當月 <sup>的12天</sup> 處理工作。</span><span class="sxs-lookup"><span data-stu-id="dd123-362">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="dd123-363">當 **RunDayOfWeek** 為0，而 **RunDay** 為負數時， **RunDay** 會定義處理工作的當月最後一天之前的天數。</span><span class="sxs-lookup"><span data-stu-id="dd123-363">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="dd123-364">1表示當月最後一天，2表示當月最後一天之前的一天，依此類推。</span><span class="sxs-lookup"><span data-stu-id="dd123-364">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="dd123-365">例如，如果 **RunDayOfWeek** 是0，而 **RunDay** 是1，則會在當月的最後一天處理工作。</span><span class="sxs-lookup"><span data-stu-id="dd123-365">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="dd123-366">當 **RunDayOfWeek** 不是0時， **RunDayOfWeek** 是將處理作業的星期幾（相對於 **RunDay**）。</span><span class="sxs-lookup"><span data-stu-id="dd123-366">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="dd123-367">例如，如果 **RunDay** 為15，而 **RunDayOfWeek** 為 7 (+ 星期六) ，則工作會在每 <sup>月15日</sup> 的第一個星期六或之後處理。</span><span class="sxs-lookup"><span data-stu-id="dd123-367">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="dd123-368">如果 **RunDay** 為20，而 **RunDayOfWeek** 為 7 ( 星期六) ，則會在當月 <sup>的20天</sup> 前或之前的第一個星期六處理工作。</span><span class="sxs-lookup"><span data-stu-id="dd123-368">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="dd123-369">如果 **RunDay** 是1，而 **RunDayOfWeek** 是 1 ( 星期日) ，則會在當月的最後一個星期日處理工作。</span><span class="sxs-lookup"><span data-stu-id="dd123-369">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="dd123-370">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-370">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-371">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="dd123-371">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-372">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="dd123-372">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-374">與 **RunDay** 搭配使用的正整數或負整數，表示處理作業的周中日或月中的日。</span><span class="sxs-lookup"><span data-stu-id="dd123-374">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="dd123-375">如需詳細資訊，請參閱 **RunDay** 屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="dd123-375">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="dd123-376">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-376">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="dd123-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-星期六** ( 7) </span><span class="sxs-lookup"><span data-stu-id="dd123-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-星期五** ( 6) </span><span class="sxs-lookup"><span data-stu-id="dd123-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-星期四** ( 5) </span><span class="sxs-lookup"><span data-stu-id="dd123-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-星期三** ( 4) </span><span class="sxs-lookup"><span data-stu-id="dd123-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-星期二** ( 3) </span><span class="sxs-lookup"><span data-stu-id="dd123-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-星期一** ( 2) </span><span class="sxs-lookup"><span data-stu-id="dd123-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-星期日** ( 1) </span><span class="sxs-lookup"><span data-stu-id="dd123-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0) </span><span class="sxs-lookup"><span data-stu-id="dd123-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**星期日** (1) </span><span class="sxs-lookup"><span data-stu-id="dd123-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**星期一** (2) </span><span class="sxs-lookup"><span data-stu-id="dd123-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**星期二** (3) </span><span class="sxs-lookup"><span data-stu-id="dd123-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**星期三** (4) </span><span class="sxs-lookup"><span data-stu-id="dd123-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**星期四** (5) </span><span class="sxs-lookup"><span data-stu-id="dd123-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**星期五** (6) </span><span class="sxs-lookup"><span data-stu-id="dd123-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**星期六** (7 ) </span><span class="sxs-lookup"><span data-stu-id="dd123-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd123-392">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="dd123-392">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-393">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="dd123-393">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-395">應處理作業的月份。</span><span class="sxs-lookup"><span data-stu-id="dd123-395">The month during which the job should be processed.</span></span> <span data-ttu-id="dd123-396">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-396">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="dd123-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**1 月** (0) </span><span class="sxs-lookup"><span data-stu-id="dd123-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**二月** (1) </span><span class="sxs-lookup"><span data-stu-id="dd123-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**3 月** (2) </span><span class="sxs-lookup"><span data-stu-id="dd123-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**四月** (3) </span><span class="sxs-lookup"><span data-stu-id="dd123-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**5 月** (4) </span><span class="sxs-lookup"><span data-stu-id="dd123-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**6 月** (5) </span><span class="sxs-lookup"><span data-stu-id="dd123-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**7 月** (6) </span><span class="sxs-lookup"><span data-stu-id="dd123-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**8 月** (7) </span><span class="sxs-lookup"><span data-stu-id="dd123-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**9 月** (8) </span><span class="sxs-lookup"><span data-stu-id="dd123-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**10 月** (9) </span><span class="sxs-lookup"><span data-stu-id="dd123-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**11 月** (10) </span><span class="sxs-lookup"><span data-stu-id="dd123-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dd123-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**12 月** (11 ) </span><span class="sxs-lookup"><span data-stu-id="dd123-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd123-409">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="dd123-409">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-410">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dd123-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-412">應處理作業的午夜之後的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="dd123-412">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="dd123-413">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-414">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="dd123-414">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-415">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dd123-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-417">工作的排程開始時間（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="dd123-417">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="dd123-418">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-419">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="dd123-419">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-420">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dd123-420">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-422">作業開始的時間。</span><span class="sxs-lookup"><span data-stu-id="dd123-422">The time that the job began.</span></span> <span data-ttu-id="dd123-423">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-423">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-424">**狀態**</span><span class="sxs-lookup"><span data-stu-id="dd123-424">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-425">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-427">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="dd123-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-428">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dd123-428">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-429">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="dd123-429">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dd123-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-431">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="dd123-431">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="dd123-432">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="dd123-432">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="dd123-433">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="dd123-433">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-434">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dd123-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-436">作業完成執行後的保留時間（以分鐘為單位），這是在該執行中的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="dd123-436">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="dd123-437">無論 **DeleteOnCompletion** 屬性的值為何，此作業都必須保持存在一段時間。</span><span class="sxs-lookup"><span data-stu-id="dd123-437">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="dd123-438">預設為五分鐘。</span><span class="sxs-lookup"><span data-stu-id="dd123-438">The default is five minutes.</span></span> <span data-ttu-id="dd123-439">這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))，而且一律設定為00000000000500.000000：000。</span><span class="sxs-lookup"><span data-stu-id="dd123-439">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="dd123-440">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="dd123-440">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-441">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dd123-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-443">上次變更工作狀態的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="dd123-443">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="dd123-444">如果作業的狀態未變更，而且此屬性已填入，則必須將它設定為0間隔值。</span><span class="sxs-lookup"><span data-stu-id="dd123-444">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="dd123-445">如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。</span><span class="sxs-lookup"><span data-stu-id="dd123-445">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="dd123-446">這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="dd123-446">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-447">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="dd123-447">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-448">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dd123-448">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-449">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-450">提交作業的時間。</span><span class="sxs-lookup"><span data-stu-id="dd123-450">The time that the job was submitted.</span></span> <span data-ttu-id="dd123-451">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-451">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-452">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="dd123-452">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-453">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dd123-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-454">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-455">作業無效或應該停止的時間。</span><span class="sxs-lookup"><span data-stu-id="dd123-455">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="dd123-456">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="dd123-456">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="dd123-457">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="dd123-457">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd123-458">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dd123-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd123-459">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dd123-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd123-460">受影響之虛擬系統的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="dd123-460">The unique name of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd123-461">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd123-461">Requirements</span></span>



| <span data-ttu-id="dd123-462">需求</span><span class="sxs-lookup"><span data-stu-id="dd123-462">Requirement</span></span> | <span data-ttu-id="dd123-463">值</span><span class="sxs-lookup"><span data-stu-id="dd123-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd123-464">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd123-464">Minimum supported client</span></span><br/> | <span data-ttu-id="dd123-465">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd123-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dd123-466">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd123-466">Minimum supported server</span></span><br/> | <span data-ttu-id="dd123-467">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd123-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd123-468">命名空間</span><span class="sxs-lookup"><span data-stu-id="dd123-468">Namespace</span></span><br/>                | <span data-ttu-id="dd123-469">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="dd123-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dd123-470">MOF</span><span class="sxs-lookup"><span data-stu-id="dd123-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd123-471"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd123-472">DLL</span><span class="sxs-lookup"><span data-stu-id="dd123-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd123-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd123-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

