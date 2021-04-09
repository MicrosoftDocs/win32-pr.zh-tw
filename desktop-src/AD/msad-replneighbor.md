---
title: MSAD_ReplNeighbor 類別
description: 表示 DS 複寫 \_ \_ 鄰近結構，其中包含特定命名內容 (NC) 和來源伺服器配對的輸入複寫狀態資訊。
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor 類別 Active Directory
- MSAD_ReplNeighbor 類別 Active Directory，描述
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934420"
---
# <a name="msad_replneighbor-class"></a><span data-ttu-id="59d05-105">MSAD \_ ReplNeighbor 類別</span><span class="sxs-lookup"><span data-stu-id="59d05-105">MSAD\_ReplNeighbor class</span></span>

<span data-ttu-id="59d05-106">表示 [**DS 複寫 \_ \_ 鄰近**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) 結構，其中包含 [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) 函式所傳回之特定命名內容 (NC) 和來源伺服器配對的輸入複寫狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="59d05-106">Represents the [**DS\_REPL\_NEIGHBOR**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) structure, which contains the inbound replication state information for a particular naming context (NC) and source server pair, as returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="59d05-107">語法</span><span class="sxs-lookup"><span data-stu-id="59d05-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a><span data-ttu-id="59d05-108">成員</span><span class="sxs-lookup"><span data-stu-id="59d05-108">Members</span></span>

<span data-ttu-id="59d05-109">**MSAD \_ ReplNeighbor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="59d05-109">The **MSAD\_ReplNeighbor** class has these types of members:</span></span>

-   [<span data-ttu-id="59d05-110">方法</span><span class="sxs-lookup"><span data-stu-id="59d05-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="59d05-111">屬性</span><span class="sxs-lookup"><span data-stu-id="59d05-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="59d05-112">方法</span><span class="sxs-lookup"><span data-stu-id="59d05-112">Methods</span></span>

<span data-ttu-id="59d05-113">**MSAD \_ ReplNeighbor** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="59d05-113">The **MSAD\_ReplNeighbor** class has these methods.</span></span>



| <span data-ttu-id="59d05-114">方法</span><span class="sxs-lookup"><span data-stu-id="59d05-114">Method</span></span>                                                           | <span data-ttu-id="59d05-115">描述</span><span class="sxs-lookup"><span data-stu-id="59d05-115">Description</span></span>                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="59d05-116">**SyncNamingCoNtext**</span><span class="sxs-lookup"><span data-stu-id="59d05-116">**SyncNamingContext**</span></span>](syncnamingcontext-msad-replneighbor.md) | <span data-ttu-id="59d05-117">使用其中一個來源同步處理目的地命名內容。</span><span class="sxs-lookup"><span data-stu-id="59d05-117">Synchronizes a destination naming context with one of its sources.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="59d05-118">屬性</span><span class="sxs-lookup"><span data-stu-id="59d05-118">Properties</span></span>

<span data-ttu-id="59d05-119">**MSAD \_ ReplNeighbor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="59d05-119">The **MSAD\_ReplNeighbor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59d05-120">**AsyncIntersiteTransportDN**</span><span class="sxs-lookup"><span data-stu-id="59d05-120">**AsyncIntersiteTransportDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-123">取得 [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) 物件的 X. 500 路徑，該物件會對應至執行複寫的傳輸。</span><span class="sxs-lookup"><span data-stu-id="59d05-123">Gets the X.500 path of the [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) object that corresponds to the transport over which replication is performed.</span></span> <span data-ttu-id="59d05-124">針對 RPC/IP 複寫，請設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="59d05-124">Set to **NULL** for RPC/IP replication.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-125">**AsyncIntersiteTransportObjGuid**</span><span class="sxs-lookup"><span data-stu-id="59d05-125">**AsyncIntersiteTransportObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-126">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-128">取得對應于 **AsyncIntersiteTransportDN** 屬性之網站間傳輸物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="59d05-128">Gets the GUID of the intersite transport object that corresponds to the **AsyncIntersiteTransportDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-129">**CompressChanges**</span><span class="sxs-lookup"><span data-stu-id="59d05-129">**CompressChanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-132">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 壓縮 \_ 變更** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-132">Gets the value that indicates whether the **DS\_REPL\_NBR\_COMPRESS\_CHANGES** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-133">**DisableScheduledSync**</span><span class="sxs-lookup"><span data-stu-id="59d05-133">**DisableScheduledSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-136">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 停用排程的 \_ \_ 同步** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-136">Gets the value that indicates whether the **DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-137">**網域**</span><span class="sxs-lookup"><span data-stu-id="59d05-137">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-138">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-140">取得已複寫 NC 之網域的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="59d05-140">Gets the canonical name of the domain of the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-141">**DoScheduledSyncs**</span><span class="sxs-lookup"><span data-stu-id="59d05-141">**DoScheduledSyncs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-144">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定「DS 複寫 NBR」的 **\_ \_ \_ \_ 排程 \_ 同步** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-144">Gets the value that indicates whether the **DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-145">**FullSyncInProgress**</span><span class="sxs-lookup"><span data-stu-id="59d05-145">**FullSyncInProgress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-148">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 完整 \_ 同步處理 \_ 中 \_** 的旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-148">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-149">**FullSyncNextPacket**</span><span class="sxs-lookup"><span data-stu-id="59d05-149">**FullSyncNextPacket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-150">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-152">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 完整 \_ 同步處理 \_ 下一個封 \_ 包** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-152">Gets the value that indicates whether the **DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-153">**IgnoreChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="59d05-153">**IgnoreChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-154">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-156">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 忽略 \_ 變更 \_ 通知** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-156">Gets the value that indicates whether the **DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-157">**IsDeletedSourceDsa**</span><span class="sxs-lookup"><span data-stu-id="59d05-157">**IsDeletedSourceDsa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-158">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-160">取得值，這個值表示此連接是否代表已刪除的來源 DC。</span><span class="sxs-lookup"><span data-stu-id="59d05-160">Gets the value that indicates whether this connection represents a source DC that has been deleted.</span></span> <span data-ttu-id="59d05-161">如果此連接代表已刪除的來源 DC，**則為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="59d05-161">**TRUE** if this connection represents a source DC that has been deleted; otherwise, **FALSE**.</span></span> <span data-ttu-id="59d05-162">根據設計，DS 會在刪除來源 DC 之後，持續一段時間複寫這些連接。</span><span class="sxs-lookup"><span data-stu-id="59d05-162">By design, the DS will continue to replicate these connections for some time for some time after the source DC is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-163">**LastSyncResult**</span><span class="sxs-lookup"><span data-stu-id="59d05-163">**LastSyncResult**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-164">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="59d05-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-166">取得上次嘗試複寫的 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="59d05-166">Gets the **HRESULT** error code for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-167">**ModifiedNumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="59d05-167">**ModifiedNumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-168">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="59d05-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-170">取得連續失敗的複寫嘗試次數，不包括預期會失敗的連接。</span><span class="sxs-lookup"><span data-stu-id="59d05-170">Gets the number of consecutive failed replication attempts, not including the connections that are expected to fail.</span></span> <span data-ttu-id="59d05-171">例如，如果 **IsDeletedSourceDsa** 屬性設定為 **TRUE**，則預期會失敗。</span><span class="sxs-lookup"><span data-stu-id="59d05-171">For example, if the **IsDeletedSourceDsa** property is set to **TRUE**, it is expected to fail.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-172">**NamingCoNtextDN**</span><span class="sxs-lookup"><span data-stu-id="59d05-172">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-173">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59d05-175">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59d05-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="59d05-176">取得此連接所複寫之 NC 的 X-y 路徑。</span><span class="sxs-lookup"><span data-stu-id="59d05-176">Gets the X.500 path for the NC that is replicated by this connection.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-177">**NamingCoNtextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="59d05-177">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-178">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-180">取得已複寫 NC 的 GUID。</span><span class="sxs-lookup"><span data-stu-id="59d05-180">Gets the GUID for the replicated NC.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-181">**NeverSynced**</span><span class="sxs-lookup"><span data-stu-id="59d05-181">**NeverSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-182">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-184">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 從未 \_ 同步** 的旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-184">Gets the value that indicates whether the **DS\_REPL\_NBR\_NEVER\_SYNCED** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-185">**NoChangeNotifications**</span><span class="sxs-lookup"><span data-stu-id="59d05-185">**NoChangeNotifications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-186">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-188">取得值，這個值會指出 **ReplicaFlags** 屬性中是否已設定 **DS 複寫 \_ \_ NBR \_ 未設定 \_ 變更 \_ 通知** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-188">Gets the value that indicates whether the **DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-189">**NumConsecutiveSyncFailures**</span><span class="sxs-lookup"><span data-stu-id="59d05-189">**NumConsecutiveSyncFailures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-190">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="59d05-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-192">取得連續失敗的複寫嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="59d05-192">Gets the number of consecutive failed replication attempts.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-193">**ReplicaFlags**</span><span class="sxs-lookup"><span data-stu-id="59d05-193">**ReplicaFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-194">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="59d05-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-196">取得一組旗標，這些旗標會指定複寫資料的屬性和選項。</span><span class="sxs-lookup"><span data-stu-id="59d05-196">Gets the set of flags that specify attributes and options for the replication data.</span></span> <span data-ttu-id="59d05-197">這個屬性可以是零或一或多個下列旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="59d05-197">This property can be zero or a combination of one or more of the following flags.</span></span>

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span data-ttu-id="59d05-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_複寫 \_ NBR 可 \_ 寫入** (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-198"><span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS\_REPL\_NBR\_WRITEABLE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-199">此命名內容的本機複本是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="59d05-199">The local copy of the naming context is writable.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span data-ttu-id="59d05-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_\_ \_ \_ \_ 啟動** (32 (0x20) ) 的複寫 NBR 同步處理</span><span class="sxs-lookup"><span data-stu-id="59d05-200"><span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-201">當目的地伺服器啟動時，會嘗試從這個來源複寫此命名內容。</span><span class="sxs-lookup"><span data-stu-id="59d05-201">Replication of this naming context from this source is attempted when the destination server is booted.</span></span> <span data-ttu-id="59d05-202">此旗標通常僅適用于內部網站鄰居。</span><span class="sxs-lookup"><span data-stu-id="59d05-202">This flag usually only applies to intra-site neighbors.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span data-ttu-id="59d05-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_複寫 \_ NBR \_ 已 \_ 排程 \_ 同步** (64 (0x40) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-203"><span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS\_REPL\_NBR\_DO\_SCHEDULED\_SYNCS** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-204">根據排程來執行複寫。</span><span class="sxs-lookup"><span data-stu-id="59d05-204">Perform replication on a schedule.</span></span> <span data-ttu-id="59d05-205">此旗標通常會設定，除非此命名內容或來源的排程為「永不」，也就是空的排程。</span><span class="sxs-lookup"><span data-stu-id="59d05-205">This flag is usually set unless the schedule for this naming context or source is "never", that is, the empty schedule.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span data-ttu-id="59d05-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_複寫 \_ NBR \_ 使用 \_ 非同步網站 \_ 間 \_ 傳輸** (128 (0x80) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-206"><span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-207">透過站台間訊息服務來間接執行複寫。</span><span class="sxs-lookup"><span data-stu-id="59d05-207">Perform replication indirectly through the Inter-Site Messaging Service.</span></span> <span data-ttu-id="59d05-208">只有透過 SMTP 複寫時，才會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-208">This flag is set only when replicating over SMTP.</span></span> <span data-ttu-id="59d05-209">透過站台間的 RPC/IP 複寫時，不會設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-209">This flag is not set when replicating over inter-site RPC/IP.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span data-ttu-id="59d05-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_複寫 \_ NBR \_ 雙向 \_ \_ 同步** (512 (0x200) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-210"><span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS\_REPL\_NBR\_TWO\_WAY\_SYNC** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-211">如果設定，表示當輸入複寫完成時，目的地伺服器必須告知來源伺服器以相反方向進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="59d05-211">If set, indicates that when inbound replication is complete, the destination server must tell the source server to synchronize in the reverse direction.</span></span> <span data-ttu-id="59d05-212">這項功能會用於撥接的案例，此時兩部伺服器中只有一部可以啟始撥接連線。</span><span class="sxs-lookup"><span data-stu-id="59d05-212">This feature is used in dial-up scenarios where only one of the two servers can initiate a dial-up connection.</span></span> <span data-ttu-id="59d05-213">例如，此選項可用於公司總部和分公司，而分公司則是透過撥號 ISP 連線，透過網際網路連接到公司總部。</span><span class="sxs-lookup"><span data-stu-id="59d05-213">For example, this option could be used in a corporate headquarters and branch office, where the branch office connects to the corporate headquarters over the Internet by means of a dial-up ISP connection.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span data-ttu-id="59d05-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_複寫 \_ NBR 會傳回 \_ \_ 物件 \_** 父系 (2048 (0x800) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-214"><span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS\_REPL\_NBR\_RETURN\_OBJECT\_PARENTS** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-215">這個鄰居所處的狀態是要在子物件之前傳回父物件；</span><span class="sxs-lookup"><span data-stu-id="59d05-215">This neighbor is in a state where it returns parent objects before children objects.</span></span> <span data-ttu-id="59d05-216">當它在父物件之前收到子物件之後，會進入這個狀態。</span><span class="sxs-lookup"><span data-stu-id="59d05-216">It goes into this state after it receives a child object before its parent.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span data-ttu-id="59d05-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_複寫 \_ NBR \_ 完整 \_ 同步 \_ 處理 \_ 進行中** (65536 (0x10000) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-217"><span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_IN\_PROGRESS** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-218">目的伺服器會從來源伺服器執行完整的同步處理；</span><span class="sxs-lookup"><span data-stu-id="59d05-218">The destination server is performing a full synchronization from the source server.</span></span> <span data-ttu-id="59d05-219">完整同步處理不會使用建立更新 (的向量，例如用於篩選更新的 DS 複寫資料 [**\_ \_ 指標**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) 。</span><span class="sxs-lookup"><span data-stu-id="59d05-219">Full synchronizations do not use vectors that create updates (such as [**DS\_REPL\_CURSORS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) for filtering updates.</span></span> <span data-ttu-id="59d05-220">完整同步處理不會當做預設複製通訊協定的一部分使用。</span><span class="sxs-lookup"><span data-stu-id="59d05-220">Full synchronizations are not used as a part of the default replication protocol.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span data-ttu-id="59d05-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_複寫 \_ NBR \_ 完整 \_ 同步處理 \_ 下一個封 \_ 包** (131072 (0x20000) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-221"><span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS\_REPL\_NBR\_FULL\_SYNC\_NEXT\_PACKET** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-222">來源中的最後一個封包表示修改了目的地伺服器尚未建立的物件。</span><span class="sxs-lookup"><span data-stu-id="59d05-222">The last packet from the source indicated a modification of an object that the destination server has not yet created.</span></span> <span data-ttu-id="59d05-223">接下來要要求的封包會指示來源伺服器將已修改物件的所有屬性放入封包中。</span><span class="sxs-lookup"><span data-stu-id="59d05-223">The next packet to be requested instructs the source server to put all attributes of the modified object into the packet.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span data-ttu-id="59d05-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_複寫 \_ NBR \_ 絕對不會 \_ 同步** 處理 (2097152 (0x200000) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-224"><span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS\_REPL\_NBR\_NEVER\_SYNCED** (2097152 (0x200000))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-225">從來沒有從這個來源中順利完成同步處理。</span><span class="sxs-lookup"><span data-stu-id="59d05-225">A synchronization has never been successfully completed from this source.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span data-ttu-id="59d05-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_複寫 \_ NBR \_** 優先 (16777216 (0x1000000) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-226"><span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS\_REPL\_NBR\_PREEMPTED** (16777216 (0x1000000))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-227">複寫引擎已暫時停止處理這個鄰居，以針對此分割區或另一個資料分割來服務另一個較高優先順序的鄰近節點。</span><span class="sxs-lookup"><span data-stu-id="59d05-227">The replication engine has temporarily stopped processing this neighbor in order to service another higher-priority neighbor, either for this partition or for another partition.</span></span> <span data-ttu-id="59d05-228">複寫引擎在完成較高優先權的工作之後，會繼續處理這個鄰居。</span><span class="sxs-lookup"><span data-stu-id="59d05-228">The replication engine will resume processing this neighbor after the higher-priority work is completed.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span data-ttu-id="59d05-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_複寫 NBR 會忽略 (67108864 (0x4000000) ) 的 \_ \_ \_ 變更 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="59d05-229"><span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS\_REPL\_NBR\_IGNORE\_CHANGE\_NOTIFICATIONS** (67108864 (0x4000000))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-230">此鄰居設定為停用以通知為基礎的同步處理。</span><span class="sxs-lookup"><span data-stu-id="59d05-230">This neighbor is set to disable notification-based synchronizations.</span></span> <span data-ttu-id="59d05-231">在站台中，網域控制站會根據變更發生時的告知來彼此進行同步化。</span><span class="sxs-lookup"><span data-stu-id="59d05-231">Within a site, domain controllers synchronize with each other based on notifications when changes occur.</span></span> <span data-ttu-id="59d05-232">這項設定可防止此鄰近節點執行通知所觸發的同步處理。</span><span class="sxs-lookup"><span data-stu-id="59d05-232">This setting prevents this neighbor from performing synchronizations that are triggered by notifications.</span></span> <span data-ttu-id="59d05-233">鄰近節點仍會根據其排程進行同步處理，或回應手動要求的同步處理。</span><span class="sxs-lookup"><span data-stu-id="59d05-233">The neighbor will still do synchronizations based on its schedule, or in response to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span data-ttu-id="59d05-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_複寫 \_ NBR \_ 停用已排程的 \_ \_ 同步** 處理 (134217728 (0x8000000) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-234"><span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS\_REPL\_NBR\_DISABLE\_SCHEDULED\_SYNC** (134217728 (0x8000000))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-235">此鄰居設定為不會根據排程執行同步處理。</span><span class="sxs-lookup"><span data-stu-id="59d05-235">This neighbor is set to not perform synchronizations based on its schedule.</span></span> <span data-ttu-id="59d05-236">此鄰近節點將執行同步處理的唯一方式，是回應變更通知或手動要求的同步處理。</span><span class="sxs-lookup"><span data-stu-id="59d05-236">The only way this neighbor will perform synchronizations is in response to change notifications or to manually requested synchronizations.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span data-ttu-id="59d05-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_複寫 \_ NBR \_ 壓縮 \_** (268435456 (0x10000000) ) 的變更</span><span class="sxs-lookup"><span data-stu-id="59d05-237"><span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS\_REPL\_NBR\_COMPRESS\_CHANGES** (268435456 (0x10000000))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-238">從這個來源接收的變更會被壓縮。</span><span class="sxs-lookup"><span data-stu-id="59d05-238">Changes received from this source are to be compressed.</span></span> <span data-ttu-id="59d05-239">通常只有當來源伺服器位於不同的網站時，才會發生壓縮。</span><span class="sxs-lookup"><span data-stu-id="59d05-239">Compression usually occurs only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span data-ttu-id="59d05-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_複寫 \_ NBR \_ 沒有 \_ \_** (536870912 (0x20000000) ) 的變更通知</span><span class="sxs-lookup"><span data-stu-id="59d05-240"><span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS\_REPL\_NBR\_NO\_CHANGE\_NOTIFICATIONS** (536870912 (0x20000000))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-241">不應該從這個來源接收變更告知。</span><span class="sxs-lookup"><span data-stu-id="59d05-241">No change notifications should be received from this source.</span></span> <span data-ttu-id="59d05-242">通常只有在來源伺服器位於不同的網站時才會設定。</span><span class="sxs-lookup"><span data-stu-id="59d05-242">Usually set only if the source server is in a different site.</span></span>

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span data-ttu-id="59d05-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_複寫 \_ NBR \_ 部分 \_ 屬性 \_ 設定** (1073741824 (0x40000000) ) </span><span class="sxs-lookup"><span data-stu-id="59d05-243"><span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS\_REPL\_NBR\_PARTIAL\_ATTRIBUTE\_SET** (1073741824 (0x40000000))</span></span>


</dt> <dd>

<span data-ttu-id="59d05-244">這個鄰居所處的狀態是要重建此複本的內容，因為部分屬性集已經有變更。</span><span class="sxs-lookup"><span data-stu-id="59d05-244">This neighbor is in a state where it is rebuilding the contents of this replica because of a change in the partial attribute set.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="59d05-245">**SourceDsaAddress**</span><span class="sxs-lookup"><span data-stu-id="59d05-245">**SourceDsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-246">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-248">取得來源 DC 的 DNS 位址。</span><span class="sxs-lookup"><span data-stu-id="59d05-248">Gets the DNS address of the source DC.</span></span>

> [!Note]  
> <span data-ttu-id="59d05-249">此字串包含修改過的 GUID，而不是常用的標準 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="59d05-249">This string contains a modified GUID, not the commonly used canonical DNS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="59d05-250">**SourceDsaCN**</span><span class="sxs-lookup"><span data-stu-id="59d05-250">**SourceDsaCN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-251">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-253">取得代表來源 DC 之 DSA 的物件路徑元件。</span><span class="sxs-lookup"><span data-stu-id="59d05-253">Gets the object path component for the DSA that represents the source DC.</span></span> <span data-ttu-id="59d05-254">這個字串通常類似于電腦名稱稱，但不一定相同。</span><span class="sxs-lookup"><span data-stu-id="59d05-254">This string is often similar to the computer name but is not always identical.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-255">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="59d05-255">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-256">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-256">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-258">取得代表來源 DC 的 DSA 的 X. 500 路徑。</span><span class="sxs-lookup"><span data-stu-id="59d05-258">Gets the X.500 path for the DSA that represents the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-259">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="59d05-259">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-260">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-262">取得來源伺服器在上次複寫時所使用的調用識別碼。</span><span class="sxs-lookup"><span data-stu-id="59d05-262">Gets the invocation ID that was used by the source server as of the last replication.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-263">**SourceDsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="59d05-263">**SourceDsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-264">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59d05-266">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59d05-266">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="59d05-267">取得目錄服務代理程式 (DSA) 的 GUID，代表 (DC) 的來源網域控制站。</span><span class="sxs-lookup"><span data-stu-id="59d05-267">Gets the GUID for the directory service agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="59d05-268">**SourceDsaSite**</span><span class="sxs-lookup"><span data-stu-id="59d05-268">**SourceDsaSite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-269">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="59d05-269">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-271">取得包含來源 DC 的網站。</span><span class="sxs-lookup"><span data-stu-id="59d05-271">Gets the site that contains the source DC.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-272">**SyncOnStartup**</span><span class="sxs-lookup"><span data-stu-id="59d05-272">**SyncOnStartup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-273">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-275">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定啟動旗標 **上的 DS 複寫 \_ \_ NBR \_ 同步 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="59d05-275">Gets the value that indicates whether the **DS\_REPL\_NBR\_SYNC\_ON\_STARTUP** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-276">**TimeOfLastSyncAttempt**</span><span class="sxs-lookup"><span data-stu-id="59d05-276">**TimeOfLastSyncAttempt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-277">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="59d05-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-279">取得上次複寫嘗試的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="59d05-279">Gets the timestamp for the last replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-280">**TimeOfLastSyncSuccess**</span><span class="sxs-lookup"><span data-stu-id="59d05-280">**TimeOfLastSyncSuccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-281">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="59d05-281">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-283">取得上一次成功複寫嘗試的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="59d05-283">Gets the timestamp for the last successful replication attempt.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-284">**TwoWaySync**</span><span class="sxs-lookup"><span data-stu-id="59d05-284">**TwoWaySync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-285">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-287">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 雙向 \_ \_ 同步** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-287">Gets the value that indicates whether the **DS\_REPL\_NBR\_TWO\_WAY\_SYNC** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-288">**UseAsyncIntersiteTransport**</span><span class="sxs-lookup"><span data-stu-id="59d05-288">**UseAsyncIntersiteTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-289">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-291">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 使用 \_ 非同步網站 \_ 間 \_ 傳輸** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-291">Gets the value that indicates whether the **DS\_REPL\_NBR\_USE\_ASYNC\_INTERSITE\_TRANSPORT** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-292">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="59d05-292">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-293">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="59d05-293">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-295">取得上一次成功完成複寫週期結束時的 **USNLastObjChangeSynced** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="59d05-295">Gets the **USNLastObjChangeSynced** property value at the end of the last successful completed replication cycle.</span></span> <span data-ttu-id="59d05-296">如果沒有成功完成複寫迴圈，則為零。</span><span class="sxs-lookup"><span data-stu-id="59d05-296">Zero if there were no successfully completed replication cycles.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-297">**USNLastObjChangeSynced**</span><span class="sxs-lookup"><span data-stu-id="59d05-297">**USNLastObjChangeSynced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-298">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="59d05-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-300">取得所收到的最後一個物件更新之 [**未**](/windows/desktop/ADSchema/a-usnchanged) 變更的屬性值。</span><span class="sxs-lookup"><span data-stu-id="59d05-300">Gets the [**unchanged**](/windows/desktop/ADSchema/a-usnchanged) attribute value of the last object update that was received.</span></span>

</dd> <dt>

<span data-ttu-id="59d05-301">**可寫入**</span><span class="sxs-lookup"><span data-stu-id="59d05-301">**Writeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59d05-302">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59d05-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59d05-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="59d05-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59d05-304">取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 NBR 可 \_ \_ \_ 寫入** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59d05-304">Gets the value that indicates whether the **DS\_REPL\_NBR\_WRITEABLE** flag has been set in the **ReplicaFlags** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59d05-305">規格需求</span><span class="sxs-lookup"><span data-stu-id="59d05-305">Requirements</span></span>



| <span data-ttu-id="59d05-306">需求</span><span class="sxs-lookup"><span data-stu-id="59d05-306">Requirement</span></span> | <span data-ttu-id="59d05-307">值</span><span class="sxs-lookup"><span data-stu-id="59d05-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59d05-308">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59d05-308">Minimum supported client</span></span><br/> | <span data-ttu-id="59d05-309">都不支援</span><span class="sxs-lookup"><span data-stu-id="59d05-309">None supported</span></span><br/>                                                               |
| <span data-ttu-id="59d05-310">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59d05-310">Minimum supported server</span></span><br/> | <span data-ttu-id="59d05-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59d05-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59d05-312">命名空間</span><span class="sxs-lookup"><span data-stu-id="59d05-312">Namespace</span></span><br/>                | <span data-ttu-id="59d05-313">根 \\ MicrosoftActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="59d05-313">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="59d05-314">MOF</span><span class="sxs-lookup"><span data-stu-id="59d05-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59d05-315"><dt>Replprov.dll mof</dt></span><span class="sxs-lookup"><span data-stu-id="59d05-315"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="59d05-316">DLL</span><span class="sxs-lookup"><span data-stu-id="59d05-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59d05-317"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59d05-317"><dt>Replprov.dll</dt></span></span> </dl> |



 

