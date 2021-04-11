---
description: CIM \_ 作業類別代表系統的工作單位，例如列印工作。 作業與進程不同，因為可以排程工作。
ms.assetid: a689230e-2a62-4f0d-9961-9bbc055d3c6e
ms.tgt_platform: multiple
title: 'CIM_Job 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.Caption
- CIM_Job.Description
- CIM_Job.InstallDate
- CIM_Job.Name
- CIM_Job.Status
- CIM_Job.ElapsedTime
- CIM_Job.JobStatus
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.StartTime
- CIM_Job.TimeSubmitted
- CIM_Job.UntilTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd527474309802a4c6d2315d8a9e61b6733e70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110840"
---
# <a name="cim_job-class-cimwin32-wmi-providers"></a><span data-ttu-id="4850d-104">CIM_Job 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="4850d-104">CIM_Job class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4850d-105">**CIM \_ 作業** 類別代表系統的工作單位，例如列印工作。</span><span class="sxs-lookup"><span data-stu-id="4850d-105">The **CIM\_Job** class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="4850d-106">作業與進程不同，因為可以排程工作。</span><span class="sxs-lookup"><span data-stu-id="4850d-106">A job is distinct from a process because a job can be scheduled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4850d-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="4850d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4850d-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="4850d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4850d-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4850d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4850d-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4850d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4850d-111">語法</span><span class="sxs-lookup"><span data-stu-id="4850d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C564-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
};
```

## <a name="members"></a><span data-ttu-id="4850d-112">成員</span><span class="sxs-lookup"><span data-stu-id="4850d-112">Members</span></span>

<span data-ttu-id="4850d-113">**CIM \_ 作業** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4850d-113">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="4850d-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4850d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4850d-115">屬性</span><span class="sxs-lookup"><span data-stu-id="4850d-115">Properties</span></span>

<span data-ttu-id="4850d-116">**CIM \_ 作業** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4850d-116">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4850d-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="4850d-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4850d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4850d-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="4850d-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4850d-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="4850d-121">A short textual description of the object.</span></span>

<span data-ttu-id="4850d-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4850d-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4850d-123">**說明**</span><span class="sxs-lookup"><span data-stu-id="4850d-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4850d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4850d-126">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="4850d-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4850d-127">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="4850d-127">A textual description of the object.</span></span>

<span data-ttu-id="4850d-128">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4850d-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4850d-129">**經過時間**</span><span class="sxs-lookup"><span data-stu-id="4850d-129">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-130">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4850d-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4850d-132">作業已執行的時間長度。</span><span class="sxs-lookup"><span data-stu-id="4850d-132">Length of time the job has been executing.</span></span>

</dd> <dt>

<span data-ttu-id="4850d-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4850d-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-134">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4850d-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4850d-136">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="4850d-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4850d-137">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="4850d-137">Indicates when the object was installed.</span></span> <span data-ttu-id="4850d-138">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="4850d-138">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4850d-139">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4850d-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4850d-140">**JobStatus**</span><span class="sxs-lookup"><span data-stu-id="4850d-140">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4850d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4850d-143">表示作業狀態的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="4850d-143">Free-form string that represents the job status.</span></span>

</dd> <dt>

<span data-ttu-id="4850d-144">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4850d-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4850d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4850d-147">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="4850d-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4850d-148">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="4850d-148">Label by which the object is known.</span></span> <span data-ttu-id="4850d-149">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4850d-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4850d-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4850d-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4850d-151">**通知**</span><span class="sxs-lookup"><span data-stu-id="4850d-151">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4850d-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4850d-154">當作業完成或失敗時，使用者會收到通知。</span><span class="sxs-lookup"><span data-stu-id="4850d-154">User is notified upon job completion or failure.</span></span>

</dd> <dt>

<span data-ttu-id="4850d-155">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="4850d-155">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4850d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4850d-158">提交工作的使用者。</span><span class="sxs-lookup"><span data-stu-id="4850d-158">User who submitted the job.</span></span>

</dd> <dt>

<span data-ttu-id="4850d-159">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="4850d-159">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4850d-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4850d-162">作業執行的重要性。</span><span class="sxs-lookup"><span data-stu-id="4850d-162">Importance of a job's execution.</span></span>

</dd> <dt>

<span data-ttu-id="4850d-163">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4850d-163">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-164">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4850d-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4850d-166">作業開始的時間。</span><span class="sxs-lookup"><span data-stu-id="4850d-166">Time that the job began.</span></span>

</dd> <dt>

<span data-ttu-id="4850d-167">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4850d-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4850d-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4850d-170">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="4850d-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4850d-171">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="4850d-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="4850d-172">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="4850d-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4850d-173">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="4850d-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4850d-174">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="4850d-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4850d-175">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="4850d-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4850d-176">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="4850d-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4850d-177">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="4850d-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4850d-178">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4850d-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4850d-179">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="4850d-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4850d-180">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4850d-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4850d-181">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4850d-182">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4850d-183">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4850d-184">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4850d-185">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4850d-186">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4850d-187">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4850d-188">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4850d-189">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="4850d-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4850d-190">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4850d-191">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="4850d-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4850d-192">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="4850d-192">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-193">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4850d-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4850d-195">提交作業的時間。</span><span class="sxs-lookup"><span data-stu-id="4850d-195">Time that the job was submitted.</span></span>

</dd> <dt>

<span data-ttu-id="4850d-196">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="4850d-196">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4850d-197">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4850d-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4850d-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4850d-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4850d-199">作業無效或應該停止的時間。</span><span class="sxs-lookup"><span data-stu-id="4850d-199">Time at which the job is invalid or should be stopped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4850d-200">備註</span><span class="sxs-lookup"><span data-stu-id="4850d-200">Remarks</span></span>

<span data-ttu-id="4850d-201">**Cim \_ 作業** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4850d-201">The **CIM\_Job** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="4850d-202">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="4850d-202">WMI does not implement this class.</span></span> <span data-ttu-id="4850d-203">針對衍生自 **CIM \_ 工作** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="4850d-203">For classes derived from **CIM\_Job**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4850d-204">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="4850d-204">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4850d-205">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4850d-205">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4850d-206">規格需求</span><span class="sxs-lookup"><span data-stu-id="4850d-206">Requirements</span></span>



| <span data-ttu-id="4850d-207">需求</span><span class="sxs-lookup"><span data-stu-id="4850d-207">Requirement</span></span> | <span data-ttu-id="4850d-208">值</span><span class="sxs-lookup"><span data-stu-id="4850d-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4850d-209">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4850d-209">Minimum supported client</span></span><br/> | <span data-ttu-id="4850d-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4850d-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4850d-211">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4850d-211">Minimum supported server</span></span><br/> | <span data-ttu-id="4850d-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4850d-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4850d-213">命名空間</span><span class="sxs-lookup"><span data-stu-id="4850d-213">Namespace</span></span><br/>                | <span data-ttu-id="4850d-214">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4850d-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4850d-215">MOF</span><span class="sxs-lookup"><span data-stu-id="4850d-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4850d-216"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4850d-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4850d-217">DLL</span><span class="sxs-lookup"><span data-stu-id="4850d-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4850d-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4850d-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4850d-219">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4850d-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4850d-220">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="4850d-220">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

