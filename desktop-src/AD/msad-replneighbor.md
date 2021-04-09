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
# <a name="msad_replneighbor-class"></a>MSAD \_ ReplNeighbor 類別

表示 [**DS 複寫 \_ \_ 鄰近**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) 結構，其中包含 [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) 函式所傳回之特定命名內容 (NC) 和來源伺服器配對的輸入複寫狀態資訊。

## <a name="syntax"></a>語法

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

## <a name="members"></a>成員

**MSAD \_ ReplNeighbor** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MSAD \_ ReplNeighbor** 類別具有這些方法。



| 方法                                                           | 描述                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**SyncNamingCoNtext**](syncnamingcontext-msad-replneighbor.md) | 使用其中一個來源同步處理目的地命名內容。<br/> |



 

### <a name="properties"></a>屬性

**MSAD \_ ReplNeighbor** 類別具有這些屬性。

<dl> <dt>

**AsyncIntersiteTransportDN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得 [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) 物件的 X. 500 路徑，該物件會對應至執行複寫的傳輸。 針對 RPC/IP 複寫，請設定為 **Null** 。

</dd> <dt>

**AsyncIntersiteTransportObjGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得對應于 **AsyncIntersiteTransportDN** 屬性之網站間傳輸物件的 GUID。

</dd> <dt>

**CompressChanges**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 壓縮 \_ 變更** 旗標。

</dd> <dt>

**DisableScheduledSync**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 停用排程的 \_ \_ 同步** 旗標。

</dd> <dt>

**網域**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得已複寫 NC 之網域的正式名稱。

</dd> <dt>

**DoScheduledSyncs**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定「DS 複寫 NBR」的 **\_ \_ \_ \_ 排程 \_ 同步** 旗標。

</dd> <dt>

**FullSyncInProgress**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 完整 \_ 同步處理 \_ 中 \_** 的旗標。

</dd> <dt>

**FullSyncNextPacket**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 完整 \_ 同步處理 \_ 下一個封 \_ 包** 旗標。

</dd> <dt>

**IgnoreChangeNotifications**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 忽略 \_ 變更 \_ 通知** 旗標。

</dd> <dt>

**IsDeletedSourceDsa**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值表示此連接是否代表已刪除的來源 DC。 如果此連接代表已刪除的來源 DC，**則為 TRUE** ;否則 **為 FALSE**。 根據設計，DS 會在刪除來源 DC 之後，持續一段時間複寫這些連接。

</dd> <dt>

**LastSyncResult**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得上次嘗試複寫的 **HRESULT** 錯誤碼。

</dd> <dt>

**ModifiedNumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得連續失敗的複寫嘗試次數，不包括預期會失敗的連接。 例如，如果 **IsDeletedSourceDsa** 屬性設定為 **TRUE**，則預期會失敗。

</dd> <dt>

**NamingCoNtextDN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得此連接所複寫之 NC 的 X-y 路徑。

</dd> <dt>

**NamingCoNtextObjGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得已複寫 NC 的 GUID。

</dd> <dt>

**NeverSynced**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 從未 \_ 同步** 的旗標。

</dd> <dt>

**NoChangeNotifications**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出 **ReplicaFlags** 屬性中是否已設定 **DS 複寫 \_ \_ NBR \_ 未設定 \_ 變更 \_ 通知** 旗標。

</dd> <dt>

**NumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得連續失敗的複寫嘗試次數。

</dd> <dt>

**ReplicaFlags**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得一組旗標，這些旗標會指定複寫資料的屬性和選項。 這個屬性可以是零或一或多個下列旗標的組合。

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_複寫 \_ NBR 可 \_ 寫入** (16 (0x10) ) 


</dt> <dd>

此命名內容的本機複本是可寫入的。

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_\_ \_ \_ \_ 啟動** (32 (0x20) ) 的複寫 NBR 同步處理


</dt> <dd>

當目的地伺服器啟動時，會嘗試從這個來源複寫此命名內容。 此旗標通常僅適用于內部網站鄰居。

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_複寫 \_ NBR \_ 已 \_ 排程 \_ 同步** (64 (0x40) ) 


</dt> <dd>

根據排程來執行複寫。 此旗標通常會設定，除非此命名內容或來源的排程為「永不」，也就是空的排程。

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_複寫 \_ NBR \_ 使用 \_ 非同步網站 \_ 間 \_ 傳輸** (128 (0x80) ) 


</dt> <dd>

透過站台間訊息服務來間接執行複寫。 只有透過 SMTP 複寫時，才會設定這個旗標。 透過站台間的 RPC/IP 複寫時，不會設定這個旗標。

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_複寫 \_ NBR \_ 雙向 \_ \_ 同步** (512 (0x200) ) 


</dt> <dd>

如果設定，表示當輸入複寫完成時，目的地伺服器必須告知來源伺服器以相反方向進行同步處理。 這項功能會用於撥接的案例，此時兩部伺服器中只有一部可以啟始撥接連線。 例如，此選項可用於公司總部和分公司，而分公司則是透過撥號 ISP 連線，透過網際網路連接到公司總部。

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_複寫 \_ NBR 會傳回 \_ \_ 物件 \_** 父系 (2048 (0x800) ) 


</dt> <dd>

這個鄰居所處的狀態是要在子物件之前傳回父物件； 當它在父物件之前收到子物件之後，會進入這個狀態。

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_複寫 \_ NBR \_ 完整 \_ 同步 \_ 處理 \_ 進行中** (65536 (0x10000) ) 


</dt> <dd>

目的伺服器會從來源伺服器執行完整的同步處理； 完整同步處理不會使用建立更新 (的向量，例如用於篩選更新的 DS 複寫資料 [**\_ \_ 指標**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) 。 完整同步處理不會當做預設複製通訊協定的一部分使用。

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_複寫 \_ NBR \_ 完整 \_ 同步處理 \_ 下一個封 \_ 包** (131072 (0x20000) ) 


</dt> <dd>

來源中的最後一個封包表示修改了目的地伺服器尚未建立的物件。 接下來要要求的封包會指示來源伺服器將已修改物件的所有屬性放入封包中。

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_複寫 \_ NBR \_ 絕對不會 \_ 同步** 處理 (2097152 (0x200000) ) 


</dt> <dd>

從來沒有從這個來源中順利完成同步處理。

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_複寫 \_ NBR \_** 優先 (16777216 (0x1000000) ) 


</dt> <dd>

複寫引擎已暫時停止處理這個鄰居，以針對此分割區或另一個資料分割來服務另一個較高優先順序的鄰近節點。 複寫引擎在完成較高優先權的工作之後，會繼續處理這個鄰居。

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_複寫 NBR 會忽略 (67108864 (0x4000000) ) 的 \_ \_ \_ 變更 \_ 通知**


</dt> <dd>

此鄰居設定為停用以通知為基礎的同步處理。 在站台中，網域控制站會根據變更發生時的告知來彼此進行同步化。 這項設定可防止此鄰近節點執行通知所觸發的同步處理。 鄰近節點仍會根據其排程進行同步處理，或回應手動要求的同步處理。

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_複寫 \_ NBR \_ 停用已排程的 \_ \_ 同步** 處理 (134217728 (0x8000000) ) 


</dt> <dd>

此鄰居設定為不會根據排程執行同步處理。 此鄰近節點將執行同步處理的唯一方式，是回應變更通知或手動要求的同步處理。

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_複寫 \_ NBR \_ 壓縮 \_** (268435456 (0x10000000) ) 的變更


</dt> <dd>

從這個來源接收的變更會被壓縮。 通常只有當來源伺服器位於不同的網站時，才會發生壓縮。

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_複寫 \_ NBR \_ 沒有 \_ \_** (536870912 (0x20000000) ) 的變更通知


</dt> <dd>

不應該從這個來源接收變更告知。 通常只有在來源伺服器位於不同的網站時才會設定。

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_複寫 \_ NBR \_ 部分 \_ 屬性 \_ 設定** (1073741824 (0x40000000) ) 


</dt> <dd>

這個鄰居所處的狀態是要重建此複本的內容，因為部分屬性集已經有變更。

</dd> </dl>

</dd> <dt>

**SourceDsaAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得來源 DC 的 DNS 位址。

> [!Note]  
> 此字串包含修改過的 GUID，而不是常用的標準 DNS 名稱。

 

</dd> <dt>

**SourceDsaCN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得代表來源 DC 之 DSA 的物件路徑元件。 這個字串通常類似于電腦名稱稱，但不一定相同。

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得代表來源 DC 的 DSA 的 X. 500 路徑。

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得來源伺服器在上次複寫時所使用的調用識別碼。

</dd> <dt>

**SourceDsaObjGuid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得目錄服務代理程式 (DSA) 的 GUID，代表 (DC) 的來源網域控制站。

</dd> <dt>

**SourceDsaSite**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得包含來源 DC 的網站。

</dd> <dt>

**SyncOnStartup**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定啟動旗標 **上的 DS 複寫 \_ \_ NBR \_ 同步 \_ \_** 。

</dd> <dt>

**TimeOfLastSyncAttempt**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得上次複寫嘗試的時間戳記。

</dd> <dt>

**TimeOfLastSyncSuccess**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得上一次成功複寫嘗試的時間戳記。

</dd> <dt>

**TwoWaySync**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 雙向 \_ \_ 同步** 旗標。

</dd> <dt>

**UseAsyncIntersiteTransport**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 \_ \_ NBR \_ 使用 \_ 非同步網站 \_ 間 \_ 傳輸** 旗標。

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得上一次成功完成複寫週期結束時的 **USNLastObjChangeSynced** 屬性值。 如果沒有成功完成複寫迴圈，則為零。

</dd> <dt>

**USNLastObjChangeSynced**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得所收到的最後一個物件更新之 [**未**](/windows/desktop/ADSchema/a-usnchanged) 變更的屬性值。

</dd> <dt>

**可寫入**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出是否已在 **ReplicaFlags** 屬性中設定 **DS 複寫 NBR 可 \_ \_ \_ 寫入** 旗標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.dll mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

