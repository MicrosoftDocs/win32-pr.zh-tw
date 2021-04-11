---
description: 代表 Microsoft Hyper-V 映射管理服務所建立的儲存體作業工作。
ms.assetid: a1517c1f-7fb6-4203-a5ec-2ecdfcbc4e8c
title: Msvm_StorageJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob
- Msvm_StorageJob.KillJob
- Msvm_StorageJob.InstanceID
- Msvm_StorageJob.Caption
- Msvm_StorageJob.Description
- Msvm_StorageJob.ElementName
- Msvm_StorageJob.InstallDate
- Msvm_StorageJob.Name
- Msvm_StorageJob.OperationalStatus
- Msvm_StorageJob.StatusDescriptions
- Msvm_StorageJob.Status
- Msvm_StorageJob.HealthState
- Msvm_StorageJob.CommunicationStatus
- Msvm_StorageJob.DetailedStatus
- Msvm_StorageJob.OperatingStatus
- Msvm_StorageJob.PrimaryStatus
- Msvm_StorageJob.JobStatus
- Msvm_StorageJob.TimeSubmitted
- Msvm_StorageJob.ScheduledStartTime
- Msvm_StorageJob.StartTime
- Msvm_StorageJob.ElapsedTime
- Msvm_StorageJob.JobRunTimes
- Msvm_StorageJob.RunMonth
- Msvm_StorageJob.RunDay
- Msvm_StorageJob.RunDayOfWeek
- Msvm_StorageJob.RunStartInterval
- Msvm_StorageJob.LocalOrUtcTime
- Msvm_StorageJob.UntilTime
- Msvm_StorageJob.Notify
- Msvm_StorageJob.Owner
- Msvm_StorageJob.Priority
- Msvm_StorageJob.PercentComplete
- Msvm_StorageJob.DeleteOnCompletion
- Msvm_StorageJob.ErrorCode
- Msvm_StorageJob.ErrorDescription
- Msvm_StorageJob.ErrorSummaryDescription
- Msvm_StorageJob.RecoveryAction
- Msvm_StorageJob.OtherRecoveryAction
- Msvm_StorageJob.JobState
- Msvm_StorageJob.TimeOfLastStateChange
- Msvm_StorageJob.TimeBeforeRemoval
- Msvm_StorageJob.Cancellable
- Msvm_StorageJob.Child
- Msvm_StorageJob.JobCompletionStatusCode
- Msvm_StorageJob.Parent
- Msvm_StorageJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3014cb9a8201d7baceaf39bb760b17c33844abeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852967"
---
# <a name="msvm_storagejob-class"></a><span data-ttu-id="3fea8-103">Msvm \_ get-storagejob 類別</span><span class="sxs-lookup"><span data-stu-id="3fea8-103">Msvm\_StorageJob class</span></span>

<span data-ttu-id="3fea8-104">代表 Microsoft Hyper-V 映射管理服務所建立的儲存體作業工作。</span><span class="sxs-lookup"><span data-stu-id="3fea8-104">Represents a storage operation job created by the Microsoft Hyper-V Image Management Service.</span></span>

<span data-ttu-id="3fea8-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3fea8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fea8-106">語法</span><span class="sxs-lookup"><span data-stu-id="3fea8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
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
  datetime TimeBeforeRemoval = 00000000000500.000000:000";
  boolean  Cancellable;
  string   Child;
  UINT32   JobCompletionStatusCode;
  string   Parent;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="3fea8-107">成員</span><span class="sxs-lookup"><span data-stu-id="3fea8-107">Members</span></span>

<span data-ttu-id="3fea8-108">**Msvm \_ get-storagejob** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3fea8-108">The **Msvm\_StorageJob** class has these types of members:</span></span>

-   [<span data-ttu-id="3fea8-109">方法</span><span class="sxs-lookup"><span data-stu-id="3fea8-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3fea8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3fea8-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3fea8-111">方法</span><span class="sxs-lookup"><span data-stu-id="3fea8-111">Methods</span></span>

<span data-ttu-id="3fea8-112">**Msvm \_ get-storagejob** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3fea8-112">The **Msvm\_StorageJob** class has these methods.</span></span>



| <span data-ttu-id="3fea8-113">方法</span><span class="sxs-lookup"><span data-stu-id="3fea8-113">Method</span></span>                                                           | <span data-ttu-id="3fea8-114">描述</span><span class="sxs-lookup"><span data-stu-id="3fea8-114">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fea8-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="3fea8-115">**GetError**</span></span>](msvm-storagejob-geterror.md)                     | <span data-ttu-id="3fea8-116">捕獲描述作業失敗原因的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3fea8-116">Retrieves the error that describes the reason why the job failed.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="3fea8-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="3fea8-117">**GetErrorEx**</span></span>](geterrorex-msvm-storagejob.md)                 | <span data-ttu-id="3fea8-118">當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="3fea8-118">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="3fea8-119">但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回一或多個 **Msvm \_ 錯誤** 實例。</span><span class="sxs-lookup"><span data-stu-id="3fea8-119">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span><br/> |
| <span data-ttu-id="3fea8-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="3fea8-120">**KillJob**</span></span>                                                      | <span data-ttu-id="3fea8-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="3fea8-121">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="3fea8-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3fea8-122">**RequestStateChange**</span></span>](msvm-storagejob-requeststatechange.md) | <span data-ttu-id="3fea8-123">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="3fea8-123">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="3fea8-124">屬性</span><span class="sxs-lookup"><span data-stu-id="3fea8-124">Properties</span></span>

<span data-ttu-id="3fea8-125">**Msvm \_ get-storagejob** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3fea8-125">The **Msvm\_StorageJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fea8-126">**可取消**</span><span class="sxs-lookup"><span data-stu-id="3fea8-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-127">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3fea8-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-129">指出是否可以取消作業。</span><span class="sxs-lookup"><span data-stu-id="3fea8-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="3fea8-130">這個屬性的值不保證取消作業的要求將會成功。</span><span class="sxs-lookup"><span data-stu-id="3fea8-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-131">**標題**</span><span class="sxs-lookup"><span data-stu-id="3fea8-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-134">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3fea8-134">A short description of the object.</span></span> <span data-ttu-id="3fea8-135">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-136">**子系**</span><span class="sxs-lookup"><span data-stu-id="3fea8-136">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-139">非同步作業失敗時，這個屬性會包含此作業所影響之 VHD 子系的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="3fea8-139">On failure of the asynchronous operation, this property contains the full path of the child of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3fea8-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-141">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-143">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="3fea8-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3fea8-144">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3fea8-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3fea8-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-146">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="3fea8-146">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-147">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3fea8-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-149">指定作業是否應該在完成時自動刪除。</span><span class="sxs-lookup"><span data-stu-id="3fea8-149">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="3fea8-150">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-150">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-151">**說明**</span><span class="sxs-lookup"><span data-stu-id="3fea8-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-154">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3fea8-154">A description of the object.</span></span> <span data-ttu-id="3fea8-155">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3fea8-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-157">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-159">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3fea8-159">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3fea8-160">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3fea8-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3fea8-161">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-162">**經過時間**</span><span class="sxs-lookup"><span data-stu-id="3fea8-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-163">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-165">作業已執行的時間長度。</span><span class="sxs-lookup"><span data-stu-id="3fea8-165">The length of time that the job has been executing.</span></span> <span data-ttu-id="3fea8-166">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3fea8-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-170">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3fea8-170">A display name for the object.</span></span> <span data-ttu-id="3fea8-171">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3fea8-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-173">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-175">特定廠商的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3fea8-175">A vendor-specific error code.</span></span> <span data-ttu-id="3fea8-176">如果作業已完成而沒有錯誤，則值必須設為零。</span><span class="sxs-lookup"><span data-stu-id="3fea8-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="3fea8-177">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3fea8-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-181">包含廠商錯誤描述的字串。</span><span class="sxs-lookup"><span data-stu-id="3fea8-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="3fea8-182">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="3fea8-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-186">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業**](cim-job.md)」。**ErrorCode**") </span><span class="sxs-lookup"><span data-stu-id="3fea8-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-187">錯誤的摘要描述（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="3fea8-187">A summary description of the error, if present.</span></span> <span data-ttu-id="3fea8-188">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-188">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3fea8-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-190">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-192">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="3fea8-192">The current health of the element.</span></span> <span data-ttu-id="3fea8-193">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="3fea8-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="3fea8-194">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3fea8-194">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="3fea8-195">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="3fea8-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-196">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3fea8-196">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-197">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-199">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3fea8-199">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="3fea8-200">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-201">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3fea8-201">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-204">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3fea8-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3fea8-205">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-206">**JobCompletionStatusCode**</span><span class="sxs-lookup"><span data-stu-id="3fea8-206">**JobCompletionStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-207">資料類型： **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3fea8-207">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-209">描述非同步作業完成狀態的 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="3fea8-209">The **HRESULT** code that describes the completion status for the asynchronous operation.</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-210">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="3fea8-210">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-211">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3fea8-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-213">作業應該執行的次數。</span><span class="sxs-lookup"><span data-stu-id="3fea8-213">The number of times that the job should be run.</span></span> <span data-ttu-id="3fea8-214">值為1表示作業不是週期性的，而任何非零值則表示作業將重複發生的次數限制。</span><span class="sxs-lookup"><span data-stu-id="3fea8-214">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="3fea8-215">零表示作業可以處理的次數沒有任何限制，但會在到達 **UntilTime** 之後終止，否則會以手動方式結束作業，以終止作業。</span><span class="sxs-lookup"><span data-stu-id="3fea8-215">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="3fea8-216">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-216">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-217">**JobState**</span><span class="sxs-lookup"><span data-stu-id="3fea8-217">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-218">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-220">作業的操作狀態。</span><span class="sxs-lookup"><span data-stu-id="3fea8-220">The operational state of a job.</span></span> <span data-ttu-id="3fea8-221">它也可以指出這些狀態之間的轉換，例如，6 (關閉) 和 3 (啟動) 。</span><span class="sxs-lookup"><span data-stu-id="3fea8-221">It can also indicate transitions between these states, for example, 6 (Shutting Down) and 3 (Starting).</span></span> <span data-ttu-id="3fea8-222">這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3fea8-222">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="3fea8-223">值</span><span class="sxs-lookup"><span data-stu-id="3fea8-223">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="3fea8-224">意義</span><span class="sxs-lookup"><span data-stu-id="3fea8-224">Meaning</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="3fea8-225"><dt>**新**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-225"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                               | <span data-ttu-id="3fea8-226">作業從未啟動。</span><span class="sxs-lookup"><span data-stu-id="3fea8-226">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="3fea8-227"><dt>**開始**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-227"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                           | <span data-ttu-id="3fea8-228">作業會從「新增」、「已暫停」或「服務」狀態移至「正在執行」狀態。</span><span class="sxs-lookup"><span data-stu-id="3fea8-228">The job is moving from the "New", "Suspended", or "Service" states into the "Running" state.</span></span><br/>                                                                                                                                            |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="3fea8-229"><dt>**正在**</dt>執行 <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-229"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                               | <span data-ttu-id="3fea8-230">工作正在執行。</span><span class="sxs-lookup"><span data-stu-id="3fea8-230">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="3fea8-231">已 <dt>**暫**</dt>止 <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-231"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                       | <span data-ttu-id="3fea8-232">作業已停止，但可以順暢的方式重新開機。</span><span class="sxs-lookup"><span data-stu-id="3fea8-232">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="3fea8-233">正在 <dt>**關閉**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-233"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                       | <span data-ttu-id="3fea8-234">作業正在移至「已完成」、「已終止」或「已終止」狀態。</span><span class="sxs-lookup"><span data-stu-id="3fea8-234">The job is moving to a "Completed", "Terminated", or "Killed" state.</span></span><br/>                                                                                                                                                                    |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="3fea8-235"><dt>**完成**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-235"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                       | <span data-ttu-id="3fea8-236">作業已正常完成。</span><span class="sxs-lookup"><span data-stu-id="3fea8-236">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="3fea8-237"><dt>**終止**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-237"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                                   | <span data-ttu-id="3fea8-238">作業已由「終止」狀態變更要求停止。</span><span class="sxs-lookup"><span data-stu-id="3fea8-238">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="3fea8-239">作業和其所有基礎進程都已結束，而且只能以新的作業重新開機。</span><span class="sxs-lookup"><span data-stu-id="3fea8-239">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="3fea8-240">只有當工作為特定作業時，才需要重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="3fea8-240">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="3fea8-241">已 <dt>**終止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-241"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                                   | <span data-ttu-id="3fea8-242">作業已由「終止」狀態變更要求停止。</span><span class="sxs-lookup"><span data-stu-id="3fea8-242">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="3fea8-243">基礎進程可能仍在執行中，而且可能需要進行清除以釋出資源。</span><span class="sxs-lookup"><span data-stu-id="3fea8-243">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="3fea8-244"><dt>**例外**</dt>狀況 <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-244"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                      | <span data-ttu-id="3fea8-245">作業處於異常狀態，可能表示發生錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="3fea8-245">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="3fea8-246">工作的實際狀態可能會透過工作專屬的物件提供。</span><span class="sxs-lookup"><span data-stu-id="3fea8-246">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="3fea8-247"><dt>**服務**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-247"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                              | <span data-ttu-id="3fea8-248">作業處於支援問題探索、解決或兩者的廠商特定狀態。</span><span class="sxs-lookup"><span data-stu-id="3fea8-248">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="3fea8-249"><dt>**DMTF 保留**</dt>的 <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-249"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>                | <span data-ttu-id="3fea8-250">保留的。</span><span class="sxs-lookup"><span data-stu-id="3fea8-250">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="3fea8-251"><dt>**廠商保留**</dt>的 <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-251"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="3fea8-252">保留的。</span><span class="sxs-lookup"><span data-stu-id="3fea8-252">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="3fea8-253">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="3fea8-253">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-254">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-256">表示作業狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="3fea8-256">A string that represents the job status.</span></span> <span data-ttu-id="3fea8-257">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-257">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-258">**JobType**</span><span class="sxs-lookup"><span data-stu-id="3fea8-258">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-259">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-261">這個 **Msvm \_ get-storagejob** 實例所追蹤的非同步操作類型。</span><span class="sxs-lookup"><span data-stu-id="3fea8-261">The type of asynchronous operation being tracked by this instance of **Msvm\_StorageJob**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3fea8-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3fea8-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>

<span data-ttu-id="3fea8-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD 建立** (1) </span><span class="sxs-lookup"><span data-stu-id="3fea8-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD Creation** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3fea8-264">建立虛擬硬碟 (VHD) 映射。</span><span class="sxs-lookup"><span data-stu-id="3fea8-264">Creating a virtual hard disk (VHD) image.</span></span>

</dd> <dt>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>

<span data-ttu-id="3fea8-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span> (2) 的 **軟碟建立**</span><span class="sxs-lookup"><span data-stu-id="3fea8-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Floppy Creation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3fea8-266"> (.VFD) 建立虛擬磁片映射。</span><span class="sxs-lookup"><span data-stu-id="3fea8-266">Creating a virtual floppy disk image (VFD).</span></span>

</dd> <dt>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>

<span data-ttu-id="3fea8-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**壓縮** (3) </span><span class="sxs-lookup"><span data-stu-id="3fea8-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compaction** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3fea8-268">壓縮 VHD 映射的大小。</span><span class="sxs-lookup"><span data-stu-id="3fea8-268">Compacting the size of a VHD image.</span></span>

</dd> <dt>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>

<span data-ttu-id="3fea8-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**擴充** (4) </span><span class="sxs-lookup"><span data-stu-id="3fea8-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansion** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3fea8-270">擴充 VHD 映射的大小。</span><span class="sxs-lookup"><span data-stu-id="3fea8-270">Expanding the size of a VHD image.</span></span>

</dd> <dt>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>

<span data-ttu-id="3fea8-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**合併** (5) </span><span class="sxs-lookup"><span data-stu-id="3fea8-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Merging** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3fea8-272">將多個 VHD 映射合併成單一映射。</span><span class="sxs-lookup"><span data-stu-id="3fea8-272">Merging multiple VHD images into a single image.</span></span>

</dd> <dt>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>

<span data-ttu-id="3fea8-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**轉換** (6) </span><span class="sxs-lookup"><span data-stu-id="3fea8-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3fea8-274">轉換虛擬硬碟映射的類型。</span><span class="sxs-lookup"><span data-stu-id="3fea8-274">Converting the type of a virtual hard disk image.</span></span>

</dd> <dt>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>

<span data-ttu-id="3fea8-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**回送掛接** (7) </span><span class="sxs-lookup"><span data-stu-id="3fea8-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Loopback Mount** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3fea8-276">裝載父磁碟分割上的虛擬硬碟</span><span class="sxs-lookup"><span data-stu-id="3fea8-276">Mounting the virtual hard disk on the parent partition</span></span>

</dd> <dt>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>

<span data-ttu-id="3fea8-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**取得 VHD 資訊** (8) </span><span class="sxs-lookup"><span data-stu-id="3fea8-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Get VHD Info** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3fea8-278">在管理作業系統上掛接 VHD。</span><span class="sxs-lookup"><span data-stu-id="3fea8-278">Mounting the VHD on the management operating system.</span></span>

</dd> <dt>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>

<span data-ttu-id="3fea8-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span> (9) **驗證 VHD 映射**</span><span class="sxs-lookup"><span data-stu-id="3fea8-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Validate VHD Image** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3fea8-280">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-280">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-281">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-283">指出 **RunStartInterval** 和 **UntilTime** 屬性中所表示的時間是否代表當地時間或 UTC 時間。</span><span class="sxs-lookup"><span data-stu-id="3fea8-283">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="3fea8-284">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-284">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="3fea8-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**本地時間** (1) </span><span class="sxs-lookup"><span data-stu-id="3fea8-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC 時間** (2 ) </span><span class="sxs-lookup"><span data-stu-id="3fea8-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3fea8-287">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3fea8-287">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-290">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="3fea8-290">The label by which the object is known.</span></span> <span data-ttu-id="3fea8-291">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-292">**通知**</span><span class="sxs-lookup"><span data-stu-id="3fea8-292">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-295">在作業完成或失敗時收到通知的使用者。</span><span class="sxs-lookup"><span data-stu-id="3fea8-295">The user who is notified upon job completion or failure.</span></span> <span data-ttu-id="3fea8-296">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-296">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-297">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3fea8-297">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-298">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-300">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3fea8-300">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3fea8-301">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3fea8-301">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3fea8-302">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-303">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3fea8-303">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-304">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3fea8-304">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-306">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="3fea8-306">The current statuses of the object.</span></span> <span data-ttu-id="3fea8-307">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-308">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="3fea8-308">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-311">字串，描述當實例的 **RecoveryAction** 屬性為 1 (其他) 時的復原動作。</span><span class="sxs-lookup"><span data-stu-id="3fea8-311">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="3fea8-312">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-312">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-313">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="3fea8-313">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-314">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-316">提交作業的使用者。</span><span class="sxs-lookup"><span data-stu-id="3fea8-316">The user who submitted the job.</span></span> <span data-ttu-id="3fea8-317">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-317">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-318">**父系**</span><span class="sxs-lookup"><span data-stu-id="3fea8-318">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-321">非同步作業失敗時，這個屬性會包含此作業所影響之 VHD 父系的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="3fea8-321">On failure of the asynchronous operation, this property contains the file path to the parent of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-322">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="3fea8-322">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-323">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-325">限定詞： **MinValue** ( 0 ) ， **int32.maxvalue ( 100** ) ， **單位** ( "Percent" ) </span><span class="sxs-lookup"><span data-stu-id="3fea8-325">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-326">作業的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="3fea8-326">The completion percentage of the job.</span></span> <span data-ttu-id="3fea8-327">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-327">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-328">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3fea8-328">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-329">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-329">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-331">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="3fea8-331">Provides high level status information.</span></span> <span data-ttu-id="3fea8-332">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="3fea8-332">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3fea8-333">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3fea8-333">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3fea8-334">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-335">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="3fea8-335">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-336">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3fea8-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-338">作業執行的重要性。</span><span class="sxs-lookup"><span data-stu-id="3fea8-338">The importance of a job's execution.</span></span> <span data-ttu-id="3fea8-339">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-339">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-340">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="3fea8-340">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-341">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3fea8-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-343">描述未成功執行的作業所要採取的復原動作。</span><span class="sxs-lookup"><span data-stu-id="3fea8-343">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="3fea8-344">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-344">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="3fea8-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3fea8-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3fea8-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**請勿繼續** (2) </span><span class="sxs-lookup"><span data-stu-id="3fea8-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**繼續進行下一個工作** (3) </span><span class="sxs-lookup"><span data-stu-id="3fea8-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span> (4) **重新執行作業**</span><span class="sxs-lookup"><span data-stu-id="3fea8-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**執行復原工作** (5 ) </span><span class="sxs-lookup"><span data-stu-id="3fea8-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3fea8-351">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="3fea8-351">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-352">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="3fea8-352">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-354">限定詞： **MinValue** (-31 ) 、 **int32.maxvalue ( 31** ) </span><span class="sxs-lookup"><span data-stu-id="3fea8-354">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-355">應處理作業之月份的日期。</span><span class="sxs-lookup"><span data-stu-id="3fea8-355">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="3fea8-356">根據 **RunDayOfWeek** 的值，此屬性有不同的解釋。</span><span class="sxs-lookup"><span data-stu-id="3fea8-356">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="3fea8-357">當 **RunDayOfWeek** 為0，而 **RunDay** 為正數時， **RunDay** 會定義處理作業的月份日期。</span><span class="sxs-lookup"><span data-stu-id="3fea8-357">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="3fea8-358">例如，如果 **RunDayOfWeek** 為0，而 **RunDay** 為12，則會在當月 <sup>的12天</sup> 處理工作。</span><span class="sxs-lookup"><span data-stu-id="3fea8-358">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="3fea8-359">當 **RunDayOfWeek** 為0，而 **RunDay** 為負數時， **RunDay** 會定義處理工作的當月最後一天之前的天數。</span><span class="sxs-lookup"><span data-stu-id="3fea8-359">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="3fea8-360">1表示當月最後一天，2表示當月最後一天之前的一天，依此類推。</span><span class="sxs-lookup"><span data-stu-id="3fea8-360">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="3fea8-361">例如，如果 **RunDayOfWeek** 是0，而 **RunDay** 是1，則會在當月的最後一天處理工作。</span><span class="sxs-lookup"><span data-stu-id="3fea8-361">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="3fea8-362">當 **RunDayOfWeek** 不是0時， **RunDayOfWeek** 是將處理作業的星期幾（相對於 **RunDay**）。</span><span class="sxs-lookup"><span data-stu-id="3fea8-362">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="3fea8-363">例如，如果 **RunDay** 為15，而 **RunDayOfWeek** 為 7 (+ 星期六) ，則工作會在每 <sup>月15日</sup> 的第一個星期六或之後處理。</span><span class="sxs-lookup"><span data-stu-id="3fea8-363">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="3fea8-364">如果 **RunDay** 為20，而 **RunDayOfWeek** 為 7 ( 星期六) ，則會在當月 <sup>的20天</sup> 前或之前的第一個星期六處理工作。</span><span class="sxs-lookup"><span data-stu-id="3fea8-364">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="3fea8-365">如果 **RunDay** 是1，而 **RunDayOfWeek** 是 1 ( 星期日) ，則會在當月的最後一個星期日處理工作。</span><span class="sxs-lookup"><span data-stu-id="3fea8-365">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="3fea8-366">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-366">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-367">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="3fea8-367">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-368">資料類型： **sint8**</span><span class="sxs-lookup"><span data-stu-id="3fea8-368">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-370">與 **RunDay** 搭配使用的正整數或負整數，表示處理作業的周中日或月中的日。</span><span class="sxs-lookup"><span data-stu-id="3fea8-370">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="3fea8-371">如需詳細資訊，請參閱 **RunDay** 屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="3fea8-371">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="3fea8-372">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-372">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="3fea8-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-星期六** ( 7) </span><span class="sxs-lookup"><span data-stu-id="3fea8-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-星期五** ( 6) </span><span class="sxs-lookup"><span data-stu-id="3fea8-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-星期四** ( 5) </span><span class="sxs-lookup"><span data-stu-id="3fea8-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-星期三** ( 4) </span><span class="sxs-lookup"><span data-stu-id="3fea8-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-星期二** ( 3) </span><span class="sxs-lookup"><span data-stu-id="3fea8-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-星期一** ( 2) </span><span class="sxs-lookup"><span data-stu-id="3fea8-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-星期日** ( 1) </span><span class="sxs-lookup"><span data-stu-id="3fea8-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0) </span><span class="sxs-lookup"><span data-stu-id="3fea8-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**星期日** (1) </span><span class="sxs-lookup"><span data-stu-id="3fea8-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**星期一** (2) </span><span class="sxs-lookup"><span data-stu-id="3fea8-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**星期二** (3) </span><span class="sxs-lookup"><span data-stu-id="3fea8-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**星期三** (4) </span><span class="sxs-lookup"><span data-stu-id="3fea8-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**星期四** (5) </span><span class="sxs-lookup"><span data-stu-id="3fea8-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**星期五** (6) </span><span class="sxs-lookup"><span data-stu-id="3fea8-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**星期六** (7 ) </span><span class="sxs-lookup"><span data-stu-id="3fea8-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3fea8-388">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="3fea8-388">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-389">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="3fea8-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-391">應處理作業的月份。</span><span class="sxs-lookup"><span data-stu-id="3fea8-391">The month during which the job should be processed.</span></span> <span data-ttu-id="3fea8-392">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="3fea8-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**1 月** (0) </span><span class="sxs-lookup"><span data-stu-id="3fea8-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**二月** (1) </span><span class="sxs-lookup"><span data-stu-id="3fea8-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**3 月** (2) </span><span class="sxs-lookup"><span data-stu-id="3fea8-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**四月** (3) </span><span class="sxs-lookup"><span data-stu-id="3fea8-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**5 月** (4) </span><span class="sxs-lookup"><span data-stu-id="3fea8-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**6 月** (5) </span><span class="sxs-lookup"><span data-stu-id="3fea8-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**7 月** (6) </span><span class="sxs-lookup"><span data-stu-id="3fea8-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**8 月** (7) </span><span class="sxs-lookup"><span data-stu-id="3fea8-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**9 月** (8) </span><span class="sxs-lookup"><span data-stu-id="3fea8-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**10 月** (9) </span><span class="sxs-lookup"><span data-stu-id="3fea8-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**11 月** (10) </span><span class="sxs-lookup"><span data-stu-id="3fea8-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**12 月** (11 ) </span><span class="sxs-lookup"><span data-stu-id="3fea8-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3fea8-405">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="3fea8-405">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-406">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-408">應處理作業的午夜之後的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="3fea8-408">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="3fea8-409">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-409">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-410">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-410">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-411">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-411">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-412">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-413">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-414">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-414">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-415">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-417">作業開始的時間。</span><span class="sxs-lookup"><span data-stu-id="3fea8-417">The time that the job began.</span></span> <span data-ttu-id="3fea8-418">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-419">**狀態**</span><span class="sxs-lookup"><span data-stu-id="3fea8-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-420">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3fea8-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-422">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3fea8-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3fea8-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-424">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3fea8-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-426">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="3fea8-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3fea8-427">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-428">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="3fea8-428">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-429">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-431">作業完成執行後的保留時間（以分鐘為單位），這是在該執行中的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="3fea8-431">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="3fea8-432">無論 **DeleteOnCompletion** 屬性的值為何，此作業都必須保持存在一段時間。</span><span class="sxs-lookup"><span data-stu-id="3fea8-432">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="3fea8-433">預設為五分鐘。</span><span class="sxs-lookup"><span data-stu-id="3fea8-433">The default is five minutes.</span></span> <span data-ttu-id="3fea8-434">這個屬性繼承自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))，而且一律設定為00000000000500.000000：000。</span><span class="sxs-lookup"><span data-stu-id="3fea8-434">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-435">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3fea8-435">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-436">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-436">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-438">上次修改虛擬機器狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="3fea8-438">The time at which the virtual machine's state was last modified.</span></span> <span data-ttu-id="3fea8-439">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3fea8-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-440">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="3fea8-440">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-441">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-443">提交作業的時間。</span><span class="sxs-lookup"><span data-stu-id="3fea8-443">The time that the job was submitted.</span></span> <span data-ttu-id="3fea8-444">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-444">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="3fea8-445">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-445">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fea8-446">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3fea8-446">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3fea8-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3fea8-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fea8-448">作業無效或應該停止的時間。</span><span class="sxs-lookup"><span data-stu-id="3fea8-448">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="3fea8-449">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-449">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fea8-450">備註</span><span class="sxs-lookup"><span data-stu-id="3fea8-450">Remarks</span></span>

<span data-ttu-id="3fea8-451">存取 **Msvm \_ get-storagejob** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="3fea8-451">Access to the **Msvm\_StorageJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3fea8-452">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="3fea8-452">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fea8-453">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fea8-453">Requirements</span></span>



| <span data-ttu-id="3fea8-454">需求</span><span class="sxs-lookup"><span data-stu-id="3fea8-454">Requirement</span></span> | <span data-ttu-id="3fea8-455">值</span><span class="sxs-lookup"><span data-stu-id="3fea8-455">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fea8-456">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fea8-456">Minimum supported client</span></span><br/> | <span data-ttu-id="3fea8-457">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fea8-457">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3fea8-458">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fea8-458">Minimum supported server</span></span><br/> | <span data-ttu-id="3fea8-459">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fea8-459">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fea8-460">命名空間</span><span class="sxs-lookup"><span data-stu-id="3fea8-460">Namespace</span></span><br/>                | <span data-ttu-id="3fea8-461">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3fea8-461">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3fea8-462">MOF</span><span class="sxs-lookup"><span data-stu-id="3fea8-462">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fea8-463"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-463"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fea8-464">DLL</span><span class="sxs-lookup"><span data-stu-id="3fea8-464">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fea8-465"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fea8-465"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fea8-466">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fea8-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fea8-467">**CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="3fea8-467">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="3fea8-468">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3fea8-468">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3fea8-469">儲存類別</span><span class="sxs-lookup"><span data-stu-id="3fea8-469">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

