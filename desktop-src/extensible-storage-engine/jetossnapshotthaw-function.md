---
description: 深入瞭解： JetOSSnapshotThaw 函數
title: JetOSSnapshotThaw 函式
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9be4bcff435fe30186b3b7585c79e3066987cc5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479054"
---
# <a name="jetossnapshotthaw-function"></a>JetOSSnapshotThaw 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetossnapshotthaw-function"></a>JetOSSnapshotThaw 函式

**JetOSSnapshotThaw** 函式會通知引擎，它可以在凍結期間和成功的快照集之後繼續正常 IO 作業。

**Windows xp：****JetOSSnapshotThaw** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*snapId*

快照集會話的識別碼。

*grbit*

此參數已保留供日後使用，且唯一支援的有效值為0。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>快照集會話無效，或 <em>grbit</em> 參數無效。</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>快照會話發生此呼叫之前的內部超時時間。 因此，在進行此呼叫之前，IO 作業會恢復正常。</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>快照集會話的識別碼無效。</p> | 



如果此函式成功，快照集會話就會結束，而且會繼續正常的引擎行為。 新的快照集會話稍後可以啟動。

如果此函式失敗，則目前的快照會話會結束，但在快照集期間，不會在內部遵守 IOs 的凍結。

#### <a name="remarks"></a>備註

將會產生快照集不同步驟的事件記錄檔專案。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)
