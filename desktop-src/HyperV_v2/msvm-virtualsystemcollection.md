---
description: 代表虛擬系統的集合。
ms.assetid: acf51beb-1103-43a4-8dc5-1a7f2a0482be
title: Msvm_VirtualSystemCollection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCollection
- Msvm_VirtualSystemCollection.CollectionID
- Msvm_VirtualSystemCollection.ElementName
- Msvm_VirtualSystemCollection.LastApplyConsistencyLevel
- Msvm_VirtualSystemCollection.LastApplyVirtualMachineIds
- Msvm_VirtualSystemCollection.LastApplyTime
- Msvm_VirtualSystemCollection.FailedOverReplicationType
- Msvm_VirtualSystemCollection.ReplicationMode
- Msvm_VirtualSystemCollection.ReplicationState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a9746356744f2743a8d6656ef4c61044223be113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386106"
---
# <a name="msvm_virtualsystemcollection-class"></a><span data-ttu-id="b8b7c-103">Msvm \_ VirtualSystemCollection 類別</span><span class="sxs-lookup"><span data-stu-id="b8b7c-103">Msvm\_VirtualSystemCollection class</span></span>

<span data-ttu-id="b8b7c-104">代表虛擬系統的集合。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-104">Represents a collection of virtual systems.</span></span>

<span data-ttu-id="b8b7c-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b7c-106">語法</span><span class="sxs-lookup"><span data-stu-id="b8b7c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCollection : CIM_CollectionOfMSEs
{
  string   CollectionID;
  string   ElementName;
  uint16   LastApplyConsistencyLevel;
  String   LastApplyVirtualMachineIds[];
  DateTime LastApplyTime;
  uint16   FailedOverReplicationType;
  uint16   ReplicationMode;
  uint16   ReplicationState;
};
```

## <a name="members"></a><span data-ttu-id="b8b7c-107">成員</span><span class="sxs-lookup"><span data-stu-id="b8b7c-107">Members</span></span>

<span data-ttu-id="b8b7c-108">**Msvm \_ VirtualSystemCollection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b8b7c-108">The **Msvm\_VirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="b8b7c-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b8b7c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8b7c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b8b7c-110">Properties</span></span>

<span data-ttu-id="b8b7c-111">**Msvm \_ VirtualSystemCollection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-111">The **Msvm\_VirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8b7c-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b7c-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b7c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-115">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CollectionID" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b8b7c-116">集合物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="b8b7c-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b7c-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b7c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ElementName" ) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="b8b7c-121">集合的使用者定義名稱。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-121">An user-defined name for the collection.</span></span> <span data-ttu-id="b8b7c-122">請注意，這不一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-122">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="b8b7c-123">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-123">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b7c-124">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b7c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b7c-126">針對虛擬系統集合執行的容錯移轉類型。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-126">Type of failover that was performed for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="b8b7c-127">在 Windows 10 1703 版中新增。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-127">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b8b7c-128">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-128">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="b8b7c-129">**一般** (1) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-129">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="b8b7c-130">**規劃** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-130">**Planned** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b7c-131">**LastApplyConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-131">**LastApplyConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b7c-132">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b7c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b7c-134">上次套用差異的一致性層級。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-134">Consistency level of the last applied delta.</span></span>

> [!Note]  
> <span data-ttu-id="b8b7c-135">在 Windows 10 1703 版中新增。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-135">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8b7c-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="b8b7c-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**應用程式一致** (1) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-137"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b8b7c-138">上次套用的差異表示虛擬系統處於應用程式一致狀態的時間點。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-138">The last applied delta indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="b8b7c-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>損 **毀一致** (2) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-139"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b8b7c-140">上次套用的差異表示虛擬系統處於損毀一致狀態的時間點。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-140">The last applied delta indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span data-ttu-id="b8b7c-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**群組損毀一致** (3) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-141"><span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Group Crash Consistent** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b8b7c-142">上次套用的差異表示群組處於損毀一致狀態的時間點。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-142">The last applied delta indicates a point in time when the group was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b7c-143">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-143">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b7c-144">資料類型： **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-144">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b7c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b7c-146">針對虛擬系統集合進行復原時，上次套用複寫的時間。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-146">The time at which the last replication is applied on recovery for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="b8b7c-147">在 Windows 10 1703 版中新增。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-147">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="b8b7c-148">**LastApplyVirtualMachineIds**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-148">**LastApplyVirtualMachineIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b7c-149">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8b7c-149">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b7c-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b7c-151">在最後一個套用迴圈中成功套用的虛擬機器識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-151">Array of Virtual Machine Ids which were successfully applied in last apply cycle.</span></span>

> [!Note]  
> <span data-ttu-id="b8b7c-152">在 Windows 10 1703 版中新增。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-152">Added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="b8b7c-153">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-153">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b7c-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b7c-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b7c-156">虛擬系統集合的複寫類型。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-156">Replication type for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="b8b7c-157">在 Windows 10 1703 版中新增。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-157">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b8b7c-158">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-158">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="b8b7c-159">**主要** (1) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-159">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="b8b7c-160">**複本** (2) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-160">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="b8b7c-161">**測試複本** (3) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-161">**Test Replica** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b7c-162">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-162">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b7c-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b7c-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8b7c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b7c-165">虛擬系統集合的複寫狀態。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-165">Replication state for the virtual system collection.</span></span>

> [!Note]  
> <span data-ttu-id="b8b7c-166">在 Windows 10 1703 版中新增。</span><span class="sxs-lookup"><span data-stu-id="b8b7c-166">Added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b8b7c-167">**停用** (0) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-167">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="b8b7c-168">**準備好** 複寫 (1) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-168">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="b8b7c-169">**等候完成初始** 複寫 (2) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-169">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="b8b7c-170">複寫 **(3**) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-170">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

<span data-ttu-id="b8b7c-171">**容錯移轉起始** (4) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-171">**Failover initiated** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="b8b7c-172">已 **復原** (5) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-172">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="b8b7c-173">**認可** (6) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-173">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="b8b7c-174">已 **暫** 止 (7) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-174">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b8b7c-175">**重大** (8) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-175">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="b8b7c-176">**等候啟動重新同步** (9) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-176">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="b8b7c-177">重新 **同步** 處理 (10) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-177">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

<span data-ttu-id="b8b7c-178">**規劃的容錯移轉 InitiatedRepurpose initiatedTest 容錯移轉 initiatedPartially 已啟用** (11) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-178">**Planned failover initiatedRepurpose initiatedTest failover initiatedPartially enabled** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

<span data-ttu-id="b8b7c-179">**部分停用** 的 (12) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-179">**Partially disabled** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

<span data-ttu-id="b8b7c-180">**部分復原** (13) </span><span class="sxs-lookup"><span data-stu-id="b8b7c-180">**Partially recovered** (13)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b8b7c-181">(14)</span><span class="sxs-lookup"><span data-stu-id="b8b7c-181">(14)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b8b7c-182">(15)</span><span class="sxs-lookup"><span data-stu-id="b8b7c-182">(15)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b8b7c-183">(16)</span><span class="sxs-lookup"><span data-stu-id="b8b7c-183">(16)</span></span>


<span data-ttu-id="b8b7c-184"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b8b7c-184"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b8b7c-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8b7c-185">Requirements</span></span>



| <span data-ttu-id="b8b7c-186">需求</span><span class="sxs-lookup"><span data-stu-id="b8b7c-186">Requirement</span></span> | <span data-ttu-id="b8b7c-187">值</span><span class="sxs-lookup"><span data-stu-id="b8b7c-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b7c-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8b7c-188">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b7c-189">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8b7c-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b8b7c-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8b7c-190">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b7c-191">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b8b7c-191">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b8b7c-192">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8b7c-192">Namespace</span></span><br/>                | <span data-ttu-id="b8b7c-193">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b8b7c-193">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b8b7c-194">MOF</span><span class="sxs-lookup"><span data-stu-id="b8b7c-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8b7c-195"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b8b7c-195"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8b7c-196">DLL</span><span class="sxs-lookup"><span data-stu-id="b8b7c-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8b7c-197"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8b7c-197"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8b7c-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8b7c-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b7c-199">**CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="b8b7c-199">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

