---
description: 深入瞭解： JetOSSnapshotFreeze 函數
title: JetOSSnapshotFreeze 函式
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 854e38f91b894b1f7cc486a15afcfe857aaa31d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473964"
---
# <a name="jetossnapshotfreeze-function"></a>JetOSSnapshotFreeze 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetossnapshotfreeze-function"></a>JetOSSnapshotFreeze 函式

**JetOSSnapshotFreeze** 函式會啟動快照集。 當快照集進行中時，引擎無法進行寫入磁片的活動。

**Windows xp：****JetOSSnapshotFreeze** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*snapId*

快照集會話的識別碼。

*pcInstanceInfo*

目前正在引擎中執行的實例數目，這些實例是快照集會話的一部分。

*paInstanceInfo*

結構的陣列，每個正在執行的實例（屬於快照會話的一部分）都有一個，描述實例和所屬的資料庫。

*grbit*

此呼叫的選項。 此參數已保留供日後使用，且唯一支援的有效值為0。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供給輸出參數的指標為 Null、快照集會話無效，或 <em>grbit</em> 參數無效。</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>快照會話不是處於適當的狀態，無法開始凍結 (例如，在) 之前，此會話上先前的凍結失敗。</p> | 
| <p>JET_errOSSnapshotNotAllowed</p> | <p>引擎未處於可以執行快照集的狀態。 有一或多個串流備份已在進行中，或有一或多個實例正在進行復原步驟或正在終止。</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>快照集會話的識別碼無效。</p> | 
| <p>JET_errOutOfMemory</p> | <p>因為記憶體不足，所以函數失敗。</p> | 
| <p>JET_errOutOfThreads</p> | <p>函數失敗，因為執行凍結的新執行緒無法啟動。</p> | 



如果此函式成功，則不會有針對資料庫檔案或屬於已凍結實例一部分的記錄檔發出的任何寫入 Io。 此外，系統會適當地填滿實例資訊，而且必須在稍後透過呼叫 [JetFreeBuffer](./jetfreebuffer-function.md) 以及傳回之實例資訊陣列的指標來釋放。

如果此函式失敗，則引擎會正常運作，而 IOs 會正常運作。 如果凍結失敗，就不需要呼叫 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 。 此外，將不會填入實例資訊，因此不需要釋放此資源。

#### <a name="remarks"></a>備註

在凍結期間，將不會有任何發行至附加資料庫或交易記錄的寫入 Io，雖然可能會有寫入的 IOs 發行至暫存資料庫或串流檔案。

資料庫和記錄檔在凍結期間的狀態 () 磁片區快照集映射中的檔案狀態，這樣一來，如果稍後再還原這些檔案，就可以正常復原。

因為在凍結期間內沒有寫入作業，所以對引擎的一般 API 呼叫可能會在該間隔內停止。 如果發生凍結，用戶端應用程式必須能夠處理可能需要較長時間的 API 呼叫。

由於上述的可能效果，有一個內部的超時時間，在此時間之後，即使未呼叫執行解凍或中止的 Api，快照會話仍會停止凍結階段。 您可以使用 [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) 系統參數變更超時的值。 請注意，一般凍結間隔的範圍為10秒，預設超時時間大約是60秒。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetOSSnapshotFreezeW</strong> (Unicode) 和 <strong>JetOSSnapshotFreezeA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
