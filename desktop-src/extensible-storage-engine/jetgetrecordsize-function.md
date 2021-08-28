---
description: 深入瞭解： JetGetRecordSize 函數
title: JetGetRecordSize 函式
TOCTitle: JetGetRecordSize Function
ms:assetid: a28567ed-c732-4509-9f8d-6f8104f62a86
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294045(v=EXCHG.10)
ms:contentKeyID: 32765644
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f42defeefa4d01648d34b971cce994fbebf8f0e8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481294"
---
# <a name="jetgetrecordsize-function"></a>JetGetRecordSize 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetrecordsize-function"></a>JetGetRecordSize 函式

**JetGetRecordSize** 函數會從所需的位置抓取記錄大小資訊。

**Windows vista： JetGetRecordSize** 是 Windows vista 引進。

```cpp
    JET_ERR JET_API JetGetRecordSize(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

識別將用於 API 呼叫的資料庫會話內容。

*tableid*

識別將用於 API 呼叫的資料表或資料指標。 資料指標必須放置在記錄上，或已備妥更新。

*precsize*

[JET_RECSIZE](./jet-recsize-structure.md)結構之輸出緩衝區的指標。

*grbit*

這是下列一或多個值。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitRecordSizeInCopyBuffer</p> | <p>這會抓取已準備進行更新的複製緩衝區中記錄的大小。 否則， <em>tableid</em> 或資料指標必須放置在記錄上，而且將會使用該記錄。</p> | 
| <p>JET_bitRecordSizeRunningTotal</p> | <p>當指定這個位時，在填滿內容之前， <a href="gg294072(v=exchg.10).md">JET_RECSIZE</a> 不會歸零，可有效地做為已造訪或已更新之多筆記錄的統計資料累積。</p> | 
| <p>JET_bitRecordSizeLocal</p> | <p>這會導致 API 忽略非內建函式的 Long 值。 例如，只會使用頁面上的本機記錄。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidGrbit</p> | <p>其中一個要求的選項無效或未執行。 當指定了不合法的<em>grbit</em>時， <strong>JetGetRecordSize</strong>函數會傳回這個錯誤。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回 JET_errInstanceUnavailable。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>同時從一個以上的執行緒使用相同的會話是不合法的。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回 JET_errInstanceUnavailable。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>如果資料指標的定位不正確，就可能發生這種情況。</p> | 
| <p>JET_errRecordDeleted</p> | <p>如果資料指標未放置於交易中，如果另一個執行緒從這個會話下刪除記錄，就會發生這種情況。</p> | 
| <p>JET_errInvalidParameter</p> | <p>如果傳遞的是 <strong>Null</strong><em>precsize</em> ，則可以傳回。</p> | 



#### <a name="remarks"></a>備註

[JET_RECSIZE](./jet-recsize-structure.md)的 **cbOverhead** 欄位中累積的金鑰大小會受到 JET_bitRecordSizeInCopyBuffer 的影響。 如果指定了此位，則在 **cbOverhead** 欄位中累積的索引鍵大小會是完整的金鑰大小。 如果未使用此位，則累積的金鑰大小將不會包含任何因金鑰首碼壓縮而儲存的大小。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_TABLEID](./jet-tableid.md)
