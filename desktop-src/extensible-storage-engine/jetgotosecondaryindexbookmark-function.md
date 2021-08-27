---
description: 深入瞭解： JetGotoSecondaryIndexBookmark 函數
title: JetGotoSecondaryIndexBookmark 函式
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84f9b90d617c11e3e304aa375e25a96b446114da
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984580"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgotosecondaryindexbookmark-function"></a>JetGotoSecondaryIndexBookmark 函式

**JetGotoSecondaryIndexBookmark** 函式會將游標放在與指定次要索引書簽相關聯的索引項目目。 次要索引書簽必須與原始抓取的相同資料表上的相同索引一起使用。 您可以使用 **JetGotoSecondaryIndexBookmark** 來取出索引項目的次要索引書簽。

**Windows xp：****JetGotoSecondaryIndexBookmark** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pvSecondaryKey*

緩衝區，其中包含要用來放置游標的次要索引鍵。

*cbSecondaryKey*

緩衝區中次要索引鍵的大小。

*pvPrimaryBookmark*

包含要用來放置游標之主鍵書簽的緩衝區。

*cbPrimaryBookmark*

緩衝區中主鍵書簽的大小。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitBookmarkPermitVirtualCurrency</p> | <p>如果找不到索引項目，就會將游標放在先前找到索引項目的位置。 作業仍會因為 JET_errRecordDeleted 而失敗;不過，您可以移至下一個或上一個索引項目（相對於現在遺漏的索引項目）。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errInvalidBookmark</p> | <p>提供的次要索引書簽無效。 發生此錯誤的原因可能是次要索引鍵為零，或次要金鑰緩衝區指標為 <strong>Null</strong>。 發生此錯誤的原因是</p><ul><li><p>目前的次要索引沒有唯一性條件約束，且所提供書簽的大小為零。</p></li><li><p>書簽緩衝區指標為 <strong>Null</strong>。</p></li></ul> | 
| <p>JET_errNoCurrentIndex</p> | <p>資料指標目前不在次要索引上。 當資料指標目前未使用次要索引時，移至次要索引書簽並沒有意義。 當資料指標不在次要索引上時，應使用<a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> 。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRecordDeleted</p> | <p>找不到與次要索引書簽相關聯的索引項目。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果此函式成功，游標將放置於與指定的次要索引書簽相關聯的索引項目目。 如果已備妥記錄以進行更新，就會取消該更新。 如果索引範圍有效，就會取消該索引範圍。 如果已針對要使用的資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。 不會變更資料庫狀態。

如果此函式失敗，除非傳回 JET_errRecordDeleted 並指定 JET_bitBookmarkPermitVirtualCurrency，否則資料指標的位置會保持不變。 在這種情況下，游標將放置於與指定次要索引書簽相關聯的索引項目目。 資料指標可以相對於該位置移動，但仍不在有效的索引項目上。

如果已備妥記錄以進行更新，就會取消該更新。 如果索引範圍有效，就會取消該索引範圍。 如果已針對要使用的資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。 在任何情況下，都不會變更資料庫狀態。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)
