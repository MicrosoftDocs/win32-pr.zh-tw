---
description: 深入瞭解： JetOSSnapshotEnd 函數
title: JetOSSnapshotEnd 函式
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b57528899b8d78ecee31f6dd54c2ac8decece383
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984431"
---
# <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetossnapshotend-function"></a>JetOSSnapshotEnd 函式

**JetOSSnapshotEnd** 函數會通知引擎快照會話已完成。

**Windows vista：****JetOSSnapshotEnd** 是在 Windows vista 中引進：  

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*snapId*

快照集會話的識別碼。

*grbit*

此呼叫的選項。 這個參數可以有下列值的組合。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>0</p> | <p>快照集會話的成功結束。</p> | 
| <p>JET_bitAbortSnapshot</p> | <p>快照會話已中止。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidGrbit</p> | <p>其中一個要求的選項無效、使用不正確或未執行。</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>快照會話已在進行中。 這是不允許的。</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>快照集會話的識別碼無效。</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>快照會話發生此呼叫之前的內部超時時間。 如此一來，在進行此呼叫之前，IO 作業會恢復正常。</p> | 



如果此函式成功，則快照集會話將會完成，而且會繼續正常的引擎行為。 新的快照集會話稍後可以啟動。

如果此函式失敗，則會傳回 JET_errOSSnapshotTimeOut 傳回碼，而且目前的快照會話會結束，但在快照集期間，不會在內部遵守 IOs 的凍結。 若為所有其他錯誤，則不會變更快照集會話狀態。

#### <a name="remarks"></a>備註

只有在使用 JET_bitContinueAfterThaw 呼叫 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 時，才會呼叫此函式。

您必須完成快照集會話，快照集驗證和記錄截斷才會發生。 將會產生快照集不同步驟的事件記錄檔專案。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[錯誤處理參數](./error-handling-parameters.md)  
[可擴充的儲存體引擎錯誤](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
