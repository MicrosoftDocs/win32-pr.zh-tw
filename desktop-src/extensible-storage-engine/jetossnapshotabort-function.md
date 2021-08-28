---
description: 深入瞭解： JetOSSnapshotAbort 函數
title: JetOSSnapshotAbort 函式
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08e56bc95798559453c383549570f9470b55fa82
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474414"
---
# <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort 函式

**JetOSSnapshotAbort** 函式會通知引擎，在凍結期間結束為失敗的快照集之後，它可以繼續正常 IO 作業。

**Windows server 2003：****JetOSSnapshotAbort** 是 Windows Server 2003 引進。  

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*snapId*

快照集會話的識別碼。

*grbit*

此呼叫的選項。 此參數已保留供日後使用，且唯一支援的有效值為 0 (零) 。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>快照集會話無效，或 grbit 參數無效。</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>快照集會話的識別碼無效。</p> | 



如果此函式成功，則快照集會話將會結束，而且會繼續正常的引擎行為。 新的快照集會話可以在稍後的時間點啟動。

如果此函式失敗，快照集會話將不會中止。

#### <a name="remarks"></a>備註

應該呼叫此函式，而不是 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) ，以通知引擎快照集已因與引擎無關的原因而中止。 稍後可以使用此資訊來協助發出快照會話的事件記錄檔訊息，或協助判斷其他適當的動作。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
