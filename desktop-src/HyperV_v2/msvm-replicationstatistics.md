---
description: 提供虛擬機器的複寫統計資料。
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Msvm_ReplicationStatistics 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991878"
---
# <a name="msvm_replicationstatistics-class"></a><span data-ttu-id="148b1-103">Msvm \_ ReplicationStatistics 類別</span><span class="sxs-lookup"><span data-stu-id="148b1-103">Msvm\_ReplicationStatistics class</span></span>

<span data-ttu-id="148b1-104">提供虛擬機器的複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="148b1-104">Provides replication statistics for a virtual machine.</span></span> <span data-ttu-id="148b1-105">這些統計資料涵蓋 [**Msvm \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md)類別的 **MonitoringStartTime** 和 **MonitoringInterval** 屬性所指定的持續時間。</span><span class="sxs-lookup"><span data-stu-id="148b1-105">These statistics cover the duration specified by the **MonitoringStartTime** and **MonitoringInterval** properties of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class.</span></span>

<span data-ttu-id="148b1-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="148b1-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="148b1-107">語法</span><span class="sxs-lookup"><span data-stu-id="148b1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a><span data-ttu-id="148b1-108">成員</span><span class="sxs-lookup"><span data-stu-id="148b1-108">Members</span></span>

<span data-ttu-id="148b1-109">**Msvm \_ ReplicationStatistics** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="148b1-109">The **Msvm\_ReplicationStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="148b1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="148b1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="148b1-111">屬性</span><span class="sxs-lookup"><span data-stu-id="148b1-111">Properties</span></span>

<span data-ttu-id="148b1-112">**Msvm \_ ReplicationStatistics** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="148b1-112">The **Msvm\_ReplicationStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="148b1-113">**ApplicationConsistentSnapshotFailureCount**</span><span class="sxs-lookup"><span data-stu-id="148b1-113">**ApplicationConsistentSnapshotFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="148b1-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-116">VSS 快照集失敗的總數。</span><span class="sxs-lookup"><span data-stu-id="148b1-116">The total number of VSS snapshot failures.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="148b1-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="148b1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-120">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="148b1-120">A short description of the object.</span></span> <span data-ttu-id="148b1-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="148b1-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-122">**說明**</span><span class="sxs-lookup"><span data-stu-id="148b1-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="148b1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-125">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="148b1-125">A description of the object.</span></span> <span data-ttu-id="148b1-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="148b1-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="148b1-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="148b1-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-130">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="148b1-130">A display name for the object.</span></span> <span data-ttu-id="148b1-131">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="148b1-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-132">**EndStatisticTime**</span><span class="sxs-lookup"><span data-stu-id="148b1-132">**EndStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-133">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="148b1-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-135">Hyper-v 複本服務停止收集複寫統計資料的時間（UTC）。</span><span class="sxs-lookup"><span data-stu-id="148b1-135">The time, in UTC, when the Hyper-V Replica service stopped gathering replication statistics data.</span></span> <span data-ttu-id="148b1-136">此時，新的複寫統計資料迴圈隨即啟動。</span><span class="sxs-lookup"><span data-stu-id="148b1-136">At this time, a new replication statistics cycle starts.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="148b1-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="148b1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="148b1-140">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="148b1-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="148b1-141">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="148b1-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="148b1-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="148b1-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-143">**LastTestFailoverTime**</span><span class="sxs-lookup"><span data-stu-id="148b1-143">**LastTestFailoverTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-144">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="148b1-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-146">指出上次為復原伺服器上已啟用複寫的虛擬機器建立測試複本系統的時間。</span><span class="sxs-lookup"><span data-stu-id="148b1-146">Indicates the last time a test replica system was created for a replication enabled virtual machine on the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-147">**MaxReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="148b1-147">**MaxReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-148">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="148b1-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-150">完成單一複寫週期所需的最大時間量（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="148b1-150">The maximum amount of time taken to complete a single replication cycle, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-151">**MaxReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="148b1-151">**MaxReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-152">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="148b1-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-154">傳輸至復原主機系統的複寫資料上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="148b1-154">Maximum replication data transferred to the recovery host system, in bytes.</span></span> <span data-ttu-id="148b1-155">這代表在此間隔中，透過單一週期傳送的複寫資料大小上限。</span><span class="sxs-lookup"><span data-stu-id="148b1-155">This represents the maximum size of replication data sent over a single cycle for this interval.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-156">**NetworkFailureCount**</span><span class="sxs-lookup"><span data-stu-id="148b1-156">**NetworkFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="148b1-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-159">具有復原主機系統的複寫通道所遇到的網路錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="148b1-159">The total number of network errors encountered for the replication channel with recovery host system.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-160">**PendingReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="148b1-160">**PendingReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-161">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="148b1-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-163">暫止複寫的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="148b1-163">The size of the data for a pending replication, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-164">**ReplicationFailureCount**</span><span class="sxs-lookup"><span data-stu-id="148b1-164">**ReplicationFailureCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="148b1-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-167">複寫失敗的總數。</span><span class="sxs-lookup"><span data-stu-id="148b1-167">The total number of replication failures.</span></span> <span data-ttu-id="148b1-168">這包括複寫操作的錯誤。</span><span class="sxs-lookup"><span data-stu-id="148b1-168">This includes errors for replication operation.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-169">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="148b1-169">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="148b1-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-172">虛擬機器的複寫健全狀況。</span><span class="sxs-lookup"><span data-stu-id="148b1-172">The replication health for the virtual machine.</span></span> <span data-ttu-id="148b1-173">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="148b1-173">This will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="148b1-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (0) </span><span class="sxs-lookup"><span data-stu-id="148b1-174"><span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not applicable** (0)</span></span>
</dt> <dt>

<span data-ttu-id="148b1-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="148b1-175"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok** (1)</span></span>
</dt> <dt>

<span data-ttu-id="148b1-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (2) </span><span class="sxs-lookup"><span data-stu-id="148b1-176"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (2)</span></span>
</dt> <dt>

<span data-ttu-id="148b1-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**重大** (3) </span><span class="sxs-lookup"><span data-stu-id="148b1-177"><span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critical** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="148b1-178">**ReplicationLatency**</span><span class="sxs-lookup"><span data-stu-id="148b1-178">**ReplicationLatency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-179">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="148b1-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-181">將資料傳輸至復原主機系統時的複寫延遲總計（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="148b1-181">Total replication latency while transferring the data to the recovery host system, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-182">**ReplicationMissCount**</span><span class="sxs-lookup"><span data-stu-id="148b1-182">**ReplicationMissCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-183">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="148b1-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-185">遺漏的複寫週期數。</span><span class="sxs-lookup"><span data-stu-id="148b1-185">The number of missed replication cycles.</span></span> <span data-ttu-id="148b1-186">這可能是因為工作負載過重、網路問題或複寫錯誤所導致。</span><span class="sxs-lookup"><span data-stu-id="148b1-186">This can be because of heavy workload, network issues, or replication errors.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-187">**ReplicationSize**</span><span class="sxs-lookup"><span data-stu-id="148b1-187">**ReplicationSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-188">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="148b1-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-190">傳輸至復原主機系統的複寫資料總量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="148b1-190">The total amount of replication data transferred to the recovery host system, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-191">**ReplicationSuccessCount**</span><span class="sxs-lookup"><span data-stu-id="148b1-191">**ReplicationSuccessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-192">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="148b1-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-194">虛擬機器的成功複寫總數。</span><span class="sxs-lookup"><span data-stu-id="148b1-194">The total number of successful replications for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="148b1-195">**StartStatisticTime**</span><span class="sxs-lookup"><span data-stu-id="148b1-195">**StartStatisticTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="148b1-196">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="148b1-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="148b1-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="148b1-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="148b1-198">Hyper-v 複本服務開始收集複寫統計資料的時間（UTC）。</span><span class="sxs-lookup"><span data-stu-id="148b1-198">The time, in UTC, when the Hyper-V Replica service started gathering replication statistics data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="148b1-199">規格需求</span><span class="sxs-lookup"><span data-stu-id="148b1-199">Requirements</span></span>



| <span data-ttu-id="148b1-200">需求</span><span class="sxs-lookup"><span data-stu-id="148b1-200">Requirement</span></span> | <span data-ttu-id="148b1-201">值</span><span class="sxs-lookup"><span data-stu-id="148b1-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="148b1-202">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="148b1-202">Minimum supported client</span></span><br/> | <span data-ttu-id="148b1-203">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="148b1-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="148b1-204">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="148b1-204">Minimum supported server</span></span><br/> | <span data-ttu-id="148b1-205">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="148b1-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="148b1-206">命名空間</span><span class="sxs-lookup"><span data-stu-id="148b1-206">Namespace</span></span><br/>                | <span data-ttu-id="148b1-207">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="148b1-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="148b1-208">MOF</span><span class="sxs-lookup"><span data-stu-id="148b1-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="148b1-209"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="148b1-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="148b1-210">DLL</span><span class="sxs-lookup"><span data-stu-id="148b1-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="148b1-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="148b1-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

