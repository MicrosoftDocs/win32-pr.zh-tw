---
description: 深入瞭解： JetGetThreadStats 函數
title: JetGetThreadStats 函式
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87f3bed1dcd9fd43a67c96cbcb53d2496a976afa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474084"
---
# <a name="jetgetthreadstats-function"></a>JetGetThreadStats 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetthreadstats-function"></a>JetGetThreadStats 函式

**JetGetThreadStats** 函式會從資料庫引擎取得目前線程的效能資訊。 您可以使用多個呼叫來收集統計資料，以反映這些呼叫之間的資料庫引擎在此執行緒上的活動。

**Windows vista：****JetGetThreadStats** 是 Windows vista 引進。  

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>參數

*pvResult*

接收執行緒統計資料的輸出緩衝區。 在成功呼叫之後，緩衝區會包含 [JET_THREADSTATS](./jet-threadstats-structure.md) 結構。

*cbMax*

輸出緩衝區的大小上限（以位元組為單位）。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBufferTooSmall</p> | <p>因為提供的輸出緩衝區太小而無法包含要求的資料，所以作業失敗。 當輸出緩衝區太小而無法包含 database engine 所支援之<a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a>結構的最小版本時， <strong>JetGetThreadStats</strong>函數會傳回這個錯誤。</p> | 



成功時，輸出緩衝區將包含 [JET_THREADSTATS](./jet-threadstats-structure.md) 結構，其中包含目前線程的資料庫引擎統計資料。

失敗時，輸出緩衝區的狀態是未定義的。

#### <a name="remarks"></a>備註

此 API 的兩個連續呼叫所提供的資訊，主要是用來計算目前線程上任何其他資料庫引擎作業的費用。 一般來說，這是藉由在讀取統計資料之前和之後減去，然後從 before count 減去 after count 來取得所執行作業的淨計數來完成。

例如，應用程式可以呼叫 **JetGetThreadStats** 一次，以取得目前線程之統計資料的初始讀取。 然後可以呼叫 [JetMove](./jetmove-function.md) 函式，並將 [ *魚尾紋* ] 參數設定為 JET_MoveNext，以移至索引上的下一個索引項目。 然後，它可以再次呼叫 **JetGetThreadStats** ，以取得執行緒統計資料的另一個讀取。 然後，它可以從第一次讀取時減去 cPageReferenced 計數器。 結果會是資料庫引擎參考用來執行 [JetMove](./jetmove-function.md) 作業的資料庫頁面數目。

每個執行緒的統計資料會在該執行緒的存留期內累積。 如果從主機進程卸載資料庫引擎的 DLL，則會重設統計資料。

未來可能會展開 [JET_THREADSTATS](./jet-threadstats-structure.md) 結構，以包含更多統計資料。 新的統計資料會加入至結構的結尾，而且可以使用增加的輸出緩衝區大小來抓取。 有更多的 cbStruct 值可以推斷出額外的統計資料。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_THREADSTATS](./jet-threadstats-structure.md)  
[JetMove](./jetmove-function.md)
