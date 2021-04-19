---
description: 表示複寫關聯性的複寫狀態。
ms.assetid: F11EFF86-5CC9-4310-8254-B310C54B561D
title: Msvm_ReplicationRelationship 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationRelationship
- Msvm_ReplicationRelationship.InstanceID
- Msvm_ReplicationRelationship.ReplicationState
- Msvm_ReplicationRelationship.ReplicationHealth
- Msvm_ReplicationRelationship.FailedOverReplicationType
- Msvm_ReplicationRelationship.LastReplicationType
- Msvm_ReplicationRelationship.LastApplicationConsistentReplicationTime
- Msvm_ReplicationRelationship.LastReplicationTime
- Msvm_ReplicationRelationship.LastApplyTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04665f96f4ec77501ee0b161d816c84943ca2c98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980881"
---
# <a name="msvm_replicationrelationship-class"></a><span data-ttu-id="b3331-103">Msvm \_ ReplicationRelationship 類別</span><span class="sxs-lookup"><span data-stu-id="b3331-103">Msvm\_ReplicationRelationship class</span></span>

<span data-ttu-id="b3331-104">表示複寫關聯性的複寫狀態。</span><span class="sxs-lookup"><span data-stu-id="b3331-104">Represents replication status for a replication relationship.</span></span> <span data-ttu-id="b3331-105">因為每個複本虛擬機器可以有多個複寫，所以您可以使用這個類別來識別每個複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="b3331-105">Because you can have multiple replications for each replica virtual machine, you can use this class to identify each replication relationship.</span></span>

<span data-ttu-id="b3331-106">下列語法已從 MOF 程式碼簡化，並包含這些繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3331-106">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3331-107">語法</span><span class="sxs-lookup"><span data-stu-id="b3331-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationRelationship : CIM_ManagedSystemElement
{
  string   InstanceID;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  datetime LastApplicationConsistentReplicationTime;
  datetime LastReplicationTime;
  datetime LastApplyTime;
};
```

## <a name="members"></a><span data-ttu-id="b3331-108">成員</span><span class="sxs-lookup"><span data-stu-id="b3331-108">Members</span></span>

<span data-ttu-id="b3331-109">**Msvm \_ ReplicationRelationship** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b3331-109">The **Msvm\_ReplicationRelationship** class has these types of members:</span></span>

-   [<span data-ttu-id="b3331-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b3331-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3331-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b3331-111">Properties</span></span>

<span data-ttu-id="b3331-112">**Msvm \_ ReplicationRelationship** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b3331-112">The **Msvm\_ReplicationRelationship** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3331-113">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="b3331-113">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3331-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b3331-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b3331-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3331-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3331-116">針對複寫關聯性所執行的容錯移轉類型。</span><span class="sxs-lookup"><span data-stu-id="b3331-116">The type of failover that was performed for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b3331-117">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="b3331-117">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="b3331-118">**一般** (1) </span><span class="sxs-lookup"><span data-stu-id="b3331-118">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="b3331-119">**應用程式一致** (2) </span><span class="sxs-lookup"><span data-stu-id="b3331-119">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="b3331-120">**規劃** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="b3331-120">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b3331-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b3331-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3331-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b3331-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3331-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3331-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3331-124">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) </span><span class="sxs-lookup"><span data-stu-id="b3331-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="b3331-125">識別複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="b3331-125">Identifies replication relationship.</span></span> <span data-ttu-id="b3331-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b3331-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="b3331-127">這個屬性的格式如下：</span><span class="sxs-lookup"><span data-stu-id="b3331-127">This property has this format:</span></span>

<span data-ttu-id="b3331-128">**Microsoft： <vmid> \\ HVR \\<0/1>**</span><span class="sxs-lookup"><span data-stu-id="b3331-128">**Microsoft:<vmid>\\HVR\\<0/1>**</span></span>

<span data-ttu-id="b3331-129">0表示主要和1表示 [擴充](#extended-replication)複寫。</span><span class="sxs-lookup"><span data-stu-id="b3331-129">0 indicates primary and 1 indicates [extended replication](#extended-replication).</span></span>

</dd> <dt>

<span data-ttu-id="b3331-130">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="b3331-130">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3331-131">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b3331-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b3331-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3331-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3331-133">複寫關聯性復原時，收到最後一個應用程式一致複寫的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b3331-133">The date and time at which the last application consistent replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="b3331-134">**LastApplyTime**</span><span class="sxs-lookup"><span data-stu-id="b3331-134">**LastApplyTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3331-135">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b3331-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b3331-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3331-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3331-137">複寫關聯性的復原所套用的上次複寫日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b3331-137">The date and time at which the last replication is applied on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="b3331-138">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="b3331-138">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3331-139">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b3331-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b3331-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3331-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3331-141">複寫關聯性復原時，接收上次複寫的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b3331-141">The date and time at which the last replication is received on recovery for the replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="b3331-142">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="b3331-142">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3331-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b3331-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b3331-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3331-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3331-145">針對複寫關聯性所接收之最後一個複寫的類型。</span><span class="sxs-lookup"><span data-stu-id="b3331-145">The type of the last replication that was received for the replication relationship.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b3331-146">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="b3331-146">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="b3331-147">**一般** (1) </span><span class="sxs-lookup"><span data-stu-id="b3331-147">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="b3331-148">**應用程式一致** (2) </span><span class="sxs-lookup"><span data-stu-id="b3331-148">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="b3331-149">**規劃** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="b3331-149">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b3331-150">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="b3331-150">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3331-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b3331-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b3331-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3331-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3331-153">複寫關聯性的複寫健全狀況。</span><span class="sxs-lookup"><span data-stu-id="b3331-153">Replication health for the replication relationship.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b3331-154">**不適用** (0) </span><span class="sxs-lookup"><span data-stu-id="b3331-154">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="b3331-155">**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="b3331-155">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b3331-156">**警告** (2) </span><span class="sxs-lookup"><span data-stu-id="b3331-156">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b3331-157">**重大** (3) </span><span class="sxs-lookup"><span data-stu-id="b3331-157">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b3331-158">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="b3331-158">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3331-159">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b3331-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b3331-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b3331-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3331-161">複寫關聯性的複寫狀態。</span><span class="sxs-lookup"><span data-stu-id="b3331-161">Replication state for the replication relationship.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b3331-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (0) </span><span class="sxs-lookup"><span data-stu-id="b3331-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="b3331-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**準備好** 複寫 (1) </span><span class="sxs-lookup"><span data-stu-id="b3331-163"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="b3331-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**等候完成初始** 複寫 (2) </span><span class="sxs-lookup"><span data-stu-id="b3331-164"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="b3331-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>複寫 **(3**) </span><span class="sxs-lookup"><span data-stu-id="b3331-165"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="b3331-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**同步複寫完成** (4) </span><span class="sxs-lookup"><span data-stu-id="b3331-166"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="b3331-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>已 **復原** (5) </span><span class="sxs-lookup"><span data-stu-id="b3331-167"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="b3331-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**認可** (6) </span><span class="sxs-lookup"><span data-stu-id="b3331-168"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="b3331-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>已 **暫** 止 (7) </span><span class="sxs-lookup"><span data-stu-id="b3331-169"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b3331-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (8) </span><span class="sxs-lookup"><span data-stu-id="b3331-170"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="b3331-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**等候啟動重新同步** (9) </span><span class="sxs-lookup"><span data-stu-id="b3331-171"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="b3331-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>重新 **同步** 處理 (10) </span><span class="sxs-lookup"><span data-stu-id="b3331-172"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="b3331-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**重新同步** 處理已暫停 (11) </span><span class="sxs-lookup"><span data-stu-id="b3331-173"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="b3331-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**正在進行容錯移轉** (12) </span><span class="sxs-lookup"><span data-stu-id="b3331-174"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="b3331-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**正在進行容錯回復** (13) </span><span class="sxs-lookup"><span data-stu-id="b3331-175"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="b3331-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>容錯 **回復完成** (14) </span><span class="sxs-lookup"><span data-stu-id="b3331-176"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="b3331-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**磁片更新進行中** (15) </span><span class="sxs-lookup"><span data-stu-id="b3331-177"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b3331-178">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="b3331-178">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="b3331-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**磁片更新嚴重** (16) </span><span class="sxs-lookup"><span data-stu-id="b3331-179"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b3331-180">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="b3331-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b3331-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (17) </span><span class="sxs-lookup"><span data-stu-id="b3331-181"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b3331-182">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="b3331-182">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="b3331-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**進行複寫的** 重設用途 (18) </span><span class="sxs-lookup"><span data-stu-id="b3331-183"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b3331-184">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="b3331-184">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="b3331-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>已 **準備同步** 複寫 (19) </span><span class="sxs-lookup"><span data-stu-id="b3331-185"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b3331-186">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="b3331-186">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="b3331-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**針對群組反向複寫做好準備** (20) </span><span class="sxs-lookup"><span data-stu-id="b3331-187"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b3331-188">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="b3331-188">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="b3331-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill 進行中** (21) </span><span class="sxs-lookup"><span data-stu-id="b3331-189"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="b3331-190">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="b3331-190">This property was added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3331-191">備註</span><span class="sxs-lookup"><span data-stu-id="b3331-191">Remarks</span></span>

### <a name="extended-replication"></a><span data-ttu-id="b3331-192">延伸複寫</span><span class="sxs-lookup"><span data-stu-id="b3331-192">Extended replication</span></span>

<span data-ttu-id="b3331-193">Windows 8 中的 Hyper-v 複寫功能可讓您在主要網站上的 Hyper-v 伺服器上執行的虛擬機器，有效率地複寫至次要網站上的另一部 Hyper-v 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b3331-193">The Hyper-V replication feature in Windows 8 allows virtual machines that run on a Hyper-V server at the primary site to be efficiently replicated to another Hyper-V server at the secondary site.</span></span>

<span data-ttu-id="b3331-194">Windows 8.1 中的 Hyper-v 複寫功能可讓使用者將複寫關聯性從次要網站延伸至第三個網站。</span><span class="sxs-lookup"><span data-stu-id="b3331-194">The Hyper-V replication feature in Windows 8.1 enables a user to extend the replication relationship from the secondary site onwards to a third site.</span></span> <span data-ttu-id="b3331-195">第三個網站可以是預先布建為復原伺服器或外部複寫提供者的 Hyper-v 主機。</span><span class="sxs-lookup"><span data-stu-id="b3331-195">The third site can be a Hyper-V host pre-provisioned as a recovery server or external replication provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3331-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3331-196">Requirements</span></span>



| <span data-ttu-id="b3331-197">需求</span><span class="sxs-lookup"><span data-stu-id="b3331-197">Requirement</span></span> | <span data-ttu-id="b3331-198">值</span><span class="sxs-lookup"><span data-stu-id="b3331-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3331-199">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3331-199">Minimum supported client</span></span><br/> | <span data-ttu-id="b3331-200">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3331-200">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b3331-201">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3331-201">Minimum supported server</span></span><br/> | <span data-ttu-id="b3331-202">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3331-202">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b3331-203">命名空間</span><span class="sxs-lookup"><span data-stu-id="b3331-203">Namespace</span></span><br/>                | <span data-ttu-id="b3331-204">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b3331-204">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b3331-205">MOF</span><span class="sxs-lookup"><span data-stu-id="b3331-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3331-206"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b3331-206"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3331-207">DLL</span><span class="sxs-lookup"><span data-stu-id="b3331-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3331-208"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3331-208"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b3331-209">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3331-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3331-210">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="b3331-210">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="b3331-211">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="b3331-211">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

