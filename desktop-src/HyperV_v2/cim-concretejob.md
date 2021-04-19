---
description: CIM 作業類別的具體版本 \_ 。 此類別代表要執行的一般可具現化工作單位，例如批次或列印工作。
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: CIM_ConcreteJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970238"
---
# <a name="cim_concretejob-class"></a><span data-ttu-id="9cecc-104">CIM \_ ConcreteJob 類別</span><span class="sxs-lookup"><span data-stu-id="9cecc-104">CIM\_ConcreteJob class</span></span>

<span data-ttu-id="9cecc-105">[**CIM \_ 作業**](cim-job.md)類別的具體版本。</span><span class="sxs-lookup"><span data-stu-id="9cecc-105">A concrete version of the [**CIM\_Job**](cim-job.md) class.</span></span> <span data-ttu-id="9cecc-106">此類別代表要執行的一般可具現化工作單位，例如批次或列印工作。</span><span class="sxs-lookup"><span data-stu-id="9cecc-106">This class represent a generic instantiable unit of work to run, such as a batch or a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cecc-107">語法</span><span class="sxs-lookup"><span data-stu-id="9cecc-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a><span data-ttu-id="9cecc-108">成員</span><span class="sxs-lookup"><span data-stu-id="9cecc-108">Members</span></span>

<span data-ttu-id="9cecc-109">**CIM \_ ConcreteJob** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9cecc-109">The **CIM\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="9cecc-110">方法</span><span class="sxs-lookup"><span data-stu-id="9cecc-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9cecc-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9cecc-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9cecc-112">方法</span><span class="sxs-lookup"><span data-stu-id="9cecc-112">Methods</span></span>

<span data-ttu-id="9cecc-113">**CIM \_ ConcreteJob** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9cecc-113">The **CIM\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="9cecc-114">方法</span><span class="sxs-lookup"><span data-stu-id="9cecc-114">Method</span></span>                                                           | <span data-ttu-id="9cecc-115">描述</span><span class="sxs-lookup"><span data-stu-id="9cecc-115">Description</span></span>                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="9cecc-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="9cecc-116">**GetError**</span></span>](cim-concretejob-geterror.md)                     | <span data-ttu-id="9cecc-117">抓取實體作業之操作狀態的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="9cecc-117">Retrieves error information for the operational status of a concrete job.</span></span><br/> |
| [<span data-ttu-id="9cecc-118">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9cecc-118">**RequestStateChange**</span></span>](cim-concretejob-requeststatechange.md) | <span data-ttu-id="9cecc-119">要求實體作業的指定狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9cecc-119">Requests the specified state change to a concrete job.</span></span><br/>                    |



 

### <a name="properties"></a><span data-ttu-id="9cecc-120">屬性</span><span class="sxs-lookup"><span data-stu-id="9cecc-120">Properties</span></span>

<span data-ttu-id="9cecc-121">**CIM \_ ConcreteJob** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9cecc-121">The **CIM\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9cecc-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9cecc-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cecc-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cecc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cecc-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cecc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9cecc-125">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) </span><span class="sxs-lookup"><span data-stu-id="9cecc-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="9cecc-126">在包含的命名空間範圍內，以獨特且不透明的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9cecc-126">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="9cecc-127">為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*</span><span class="sxs-lookup"><span data-stu-id="9cecc-127">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="9cecc-128">*OrgID* 必須包含受著作權、商標或其他唯一名稱（由定義 **InstanceID** 的商務實體所擁有），或是由可辨識的全域授權單位所指派的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="9cecc-128">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="9cecc-129">此模式類似于架構類別名稱的結構。</span><span class="sxs-lookup"><span data-stu-id="9cecc-129">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="9cecc-130">此外，若要確保唯一性， **InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。</span><span class="sxs-lookup"><span data-stu-id="9cecc-130">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="9cecc-131">因此， *OrgID* 不能包含冒號 ( '： ' ) 。</span><span class="sxs-lookup"><span data-stu-id="9cecc-131">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="9cecc-132">*LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。</span><span class="sxs-lookup"><span data-stu-id="9cecc-132">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="9cecc-133">如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。</span><span class="sxs-lookup"><span data-stu-id="9cecc-133">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="9cecc-134">若為分散式管理工作強制 (DMTF) 定義的實例，則必須搭配 *OrgID* 設定為 CIM 使用模式。</span><span class="sxs-lookup"><span data-stu-id="9cecc-134">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="9cecc-135">**JobState**</span><span class="sxs-lookup"><span data-stu-id="9cecc-135">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cecc-136">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9cecc-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9cecc-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cecc-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cecc-138">作業的操作狀態，以及這些狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="9cecc-138">The operational state of the job, and the transition between those states.</span></span>

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span data-ttu-id="9cecc-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**新** (2) </span><span class="sxs-lookup"><span data-stu-id="9cecc-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**New** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-140">作業從未啟動。</span><span class="sxs-lookup"><span data-stu-id="9cecc-140">the job has never been started.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9cecc-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="9cecc-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-142">作業正在從「新增」、「已暫停」或「服務」狀態移至「正在執行」狀態。</span><span class="sxs-lookup"><span data-stu-id="9cecc-142">The job is moving from the 'New', 'Suspended', or 'Service' states into the 'Running' state.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9cecc-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (4) </span><span class="sxs-lookup"><span data-stu-id="9cecc-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-144">工作正在執行。</span><span class="sxs-lookup"><span data-stu-id="9cecc-144">The Job is running.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="9cecc-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>已 **暫** 止 (5) </span><span class="sxs-lookup"><span data-stu-id="9cecc-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-146">作業已停止，但可以順暢的方式重新開機。</span><span class="sxs-lookup"><span data-stu-id="9cecc-146">The Job is stopped, but can be restarted in a seamless manner.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="9cecc-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (6) </span><span class="sxs-lookup"><span data-stu-id="9cecc-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-148">作業正在移至「已完成」、「已終止」或「已終止」狀態。</span><span class="sxs-lookup"><span data-stu-id="9cecc-148">The job is moving to a 'Completed', 'Terminated', or 'Killed' state.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="9cecc-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (7) </span><span class="sxs-lookup"><span data-stu-id="9cecc-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-150">作業已正常完成。</span><span class="sxs-lookup"><span data-stu-id="9cecc-150">The job has completed normally.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="9cecc-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**終止** (8) </span><span class="sxs-lookup"><span data-stu-id="9cecc-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-152">作業已由「終止」狀態變更要求停止。</span><span class="sxs-lookup"><span data-stu-id="9cecc-152">The job has been stopped by a 'Terminate' state change request.</span></span> <span data-ttu-id="9cecc-153">作業和其所有基礎進程都已結束，而且可以重新開機 (這只是做為新工作的工作專屬) 。</span><span class="sxs-lookup"><span data-stu-id="9cecc-153">The job and all its underlying processes are ended and can be restarted (this is job-specific) only as a new job.</span></span>

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span data-ttu-id="9cecc-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>已 **終止** (9) </span><span class="sxs-lookup"><span data-stu-id="9cecc-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Killed** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-155">作業已由 ' Kill ' 狀態變更要求停止。</span><span class="sxs-lookup"><span data-stu-id="9cecc-155">The job has been stopped by a 'Kill' state change request.</span></span> <span data-ttu-id="9cecc-156">基礎進程可能已在執行中，而且可能需要清除才能釋出資源。</span><span class="sxs-lookup"><span data-stu-id="9cecc-156">Underlying processes might have been left running, and cleanup might be required to free up resources.</span></span>

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span data-ttu-id="9cecc-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**例外** 狀況 (10) </span><span class="sxs-lookup"><span data-stu-id="9cecc-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exception** (10)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-158">作業處於異常狀態，可能表示發生錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="9cecc-158">The Job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="9cecc-159">實際狀態可能會顯示在工作特定的物件。</span><span class="sxs-lookup"><span data-stu-id="9cecc-159">Actual status might be displayed though job-specific objects.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9cecc-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**服務** (11) </span><span class="sxs-lookup"><span data-stu-id="9cecc-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-161">作業處於支援問題探索、解決或兩者的廠商特定狀態</span><span class="sxs-lookup"><span data-stu-id="9cecc-161">The Job is in a vendor-specific state that supports problem discovery, or resolution, or both</span></span>

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span data-ttu-id="9cecc-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**查詢暫** 止 (12) </span><span class="sxs-lookup"><span data-stu-id="9cecc-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query Pending** (12)</span></span>


</dt> <dd>

<span data-ttu-id="9cecc-163">等候用戶端解析查詢。</span><span class="sxs-lookup"><span data-stu-id="9cecc-163">Waiting for a client to resolve a query.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9cecc-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (13. 32767) </span><span class="sxs-lookup"><span data-stu-id="9cecc-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (13..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="9cecc-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="9cecc-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9cecc-166">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9cecc-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cecc-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9cecc-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9cecc-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cecc-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9cecc-169">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="9cecc-169">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9cecc-170">實例的使用者易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9cecc-170">The user-friendly name of the instance.</span></span> <span data-ttu-id="9cecc-171">此外，使用者易記名稱可用來做為搜尋或查詢的屬性。</span><span class="sxs-lookup"><span data-stu-id="9cecc-171">In addition, the user-friendly name can be used as a property for a search or query.</span></span>

> [!Note]  
> <span data-ttu-id="9cecc-172">名稱在命名空間中不一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="9cecc-172">The name does not have to be unique within the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="9cecc-173">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="9cecc-173">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cecc-174">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9cecc-174">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9cecc-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9cecc-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9cecc-176">限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9cecc-176">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9cecc-177">表示已完成的作業保留時間長度。</span><span class="sxs-lookup"><span data-stu-id="9cecc-177">Indicates how long a completed job is retained.</span></span> <span data-ttu-id="9cecc-178">預設值為 "00000000000500.000000： 000" (五分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="9cecc-178">The default value is "00000000000500.000000:000" (five minutes).</span></span>

</dd> <dt>

<span data-ttu-id="9cecc-179">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9cecc-179">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cecc-180">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9cecc-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9cecc-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9cecc-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9cecc-182">上次變更工作狀態的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="9cecc-182">The date or time when the state of the job last changed.</span></span>

> [!Note]  
> <span data-ttu-id="9cecc-183">如果作業的狀態未變更，而且此屬性已填入，則必須將它設定為零間隔值。</span><span class="sxs-lookup"><span data-stu-id="9cecc-183">If the state of the Job has not changed and this property is populated, then it must be set to a zero interval value.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9cecc-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cecc-184">Requirements</span></span>



| <span data-ttu-id="9cecc-185">需求</span><span class="sxs-lookup"><span data-stu-id="9cecc-185">Requirement</span></span> | <span data-ttu-id="9cecc-186">值</span><span class="sxs-lookup"><span data-stu-id="9cecc-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cecc-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9cecc-187">Minimum supported client</span></span><br/> | <span data-ttu-id="9cecc-188">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9cecc-188">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9cecc-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9cecc-189">Minimum supported server</span></span><br/> | <span data-ttu-id="9cecc-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9cecc-190">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9cecc-191">命名空間</span><span class="sxs-lookup"><span data-stu-id="9cecc-191">Namespace</span></span><br/>                | <span data-ttu-id="9cecc-192">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9cecc-192">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9cecc-193">MOF</span><span class="sxs-lookup"><span data-stu-id="9cecc-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cecc-194"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9cecc-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cecc-195">DLL</span><span class="sxs-lookup"><span data-stu-id="9cecc-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cecc-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9cecc-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9cecc-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cecc-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cecc-198">**CIM \_ 作業**</span><span class="sxs-lookup"><span data-stu-id="9cecc-198">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

