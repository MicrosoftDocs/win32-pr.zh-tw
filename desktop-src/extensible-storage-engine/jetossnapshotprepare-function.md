---
description: 深入瞭解： JetOSSnapshotPrepare 函數
title: JetOSSnapshotPrepare 函式
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 010cafd19ffde09b3083dd3cb6e6a69fa2268f11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470325"
---
# <a name="jetossnapshotprepare-function"></a>JetOSSnapshotPrepare 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetossnapshotprepare-function"></a>JetOSSnapshotPrepare 函式

**JetOSSnapshotPrepare** 函式會開始快照集會話的準備工作。 快照集會話是一個短暫的時間間隔，在此時間間隔中，引擎不會將任何寫入 Io 發出至磁片，因此引擎可以在由快照寫入器驅動) 時，參與磁片區快照集會話 (。

**Windows xp：****JetOSSnapshotPrepare** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*psnapId*

要啟動之快照集會話的識別碼。

*grbit*

此呼叫的選項。 這個參數可以有下列值的組合。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>0</p> | <p>一般快照集。</p> | 
| <p>JET_bitIncrementalSnapshot</p> | <p>只會取得記錄檔。</p> | 
| <p>JET_bitCopySnapshot</p> | <p>複製快照集 (一般或累加) ，而不會截斷記錄。</p> | 
| <p>JET_bitContinueAfterThaw</p> | <p>快照會話會在 <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> 之後發生，而且需要 <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> 函式呼叫。</p> | 
| <p>JET_bitExplicitPrepare</p> | <p>預設不會準備任何實例。</p><p><strong>Windows 7：</strong> JET_bitExplicitPrepare 會在 Windows 7 中引進。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>快照集識別碼指標為 Null 或 <em>grbit</em> 參數無效。</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>快照集會話已在進行中，而且在任何指定的時間，作業不允許有多個快照集會話。</p> | 



如果此函式成功，則快照集會話將能夠在任何時間與 IO 凍結階段啟動。 將會傳回會話的識別碼，而且必須在快照集會話的後續呼叫中使用。

現在會將執行中的引擎實例視為快照會話的一部分。

**Windows Vista：** 若要指定不同的實例子集，可以呼叫 [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) 。

一般 API 順序呼叫是： **JetOSSnapshotPrepare**，並選擇性地接著一或多個 [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)呼叫，然後再接著 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)。 當凍結開始之後，就可以使用 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)來終止。 在準備之後的任何時間，快照集會話都可以使用 [JetOSSnapshotAbort](./jetossnapshotabort-function.md)突然終止。

如果在 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md)之後指定了 JET_bitContinueAfterThaw，快照會話將維持 (，不過 i/o 將繼續) 。 這會啟用快照集的驗證，並在需要時，使用 [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) 啟用記錄截斷，而且需要呼叫 [JetOSSnapshotEnd](./jetossnapshotend-function.md)。

如果此函式失敗，則不會發生引擎狀態的變更。

#### <a name="remarks"></a>備註

將會產生快照集不同步驟的事件記錄檔專案。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)  
[JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md)
