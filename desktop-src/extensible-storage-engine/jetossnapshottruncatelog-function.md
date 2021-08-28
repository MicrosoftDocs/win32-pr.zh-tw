---
description: 深入瞭解： JetOSSnapshotTruncateLog 函數
title: JetOSSnapshotTruncateLog 函式
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4da8e76b1c735f6249f1d7e3893acd1db1743b65
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985861"
---
# <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetossnapshottruncatelog-function"></a>JetOSSnapshotTruncateLog 函式

**JetOSSnapshotTruncateLog** 函數會針對屬於快照會話一部分的所有實例啟用記錄截斷。

**Windows vista：****JetOSSnapshotTruncateLog** 是 Windows vista 引進。  

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
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
| <p>JET_bitAllDatabasesSnapshot</p> | <p>附加所有資料庫，讓儲存引擎可以計算並進行記錄截斷。</p> | 
| <p>0 (零)</p> | <p>不會發生截斷。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidGrbit</p> | <p><em>Grbit</em>參數無效。</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>快照會話不是處於截斷可能發生的狀態。 可能的原因包括：</p><ul><li><p>呼叫是在快照集會話超時之後完成</p></li><li><p>此會話已指定為複製快照集</p></li></ul> | 



成功時，如果可能的話，會截斷快照會話中一個或所有實例的記錄檔。

#### <a name="remarks"></a>備註

只有在使用 JET_bitContinueAfterThaw 選項建立快照集時，才應該呼叫這個函數。 否則，在 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 呼叫之後，快照集會話就會結束。

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
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
