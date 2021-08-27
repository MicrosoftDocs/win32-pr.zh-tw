---
description: 深入瞭解： JetGotoBookmark 函數
title: JetGotoBookmark 函式
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54a6370badcdd83e1beed4cc50f42a52eab797ba
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984641"
---
# <a name="jetgotobookmark-function"></a>JetGotoBookmark 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgotobookmark-function"></a>JetGotoBookmark 函式

**JetGotoBookmark** 函式會將游標放置在與指定書簽相關聯之記錄的索引項目目。 書簽可以搭配資料表上定義的任何索引使用。 您可以使用 [JetGetBookmark](./jetgetbookmark-function.md)來取出記錄的書簽。

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pvBookmark*

包含要用來放置游標之書簽的緩衝區。

*cbBookmark*

緩衝區中書簽的大小。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong>  此傳回值是在 Windows XP 中引進。</p> | 
| <p>JET_errInvalidBookmark</p> | <p>提供的書簽無效。 發生這種情況的原因可能是書簽的大小為零，或書簽緩衝區指標為 <strong>Null</strong>。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>資料指標位於次要索引上，而且找不到與書簽相關聯之記錄的索引項目。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與該會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRecordDeleted</p> | <p>找不到與書簽相關聯的記錄。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p><strong>Windows XP：</strong>  此傳回值是在 Windows XP 中引進。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果此函式成功，游標將放置在與指定書簽相關聯之記錄的索引項目上。 如果已備妥記錄以進行更新，就會取消該更新。 如果索引範圍有效，就會取消該索引範圍。 如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。 不會變更資料庫狀態。

如果此函式失敗，則資料指標的位置會保持不變。 如果已備妥記錄以進行更新，就會取消該更新。 如果索引範圍有效，就會取消該索引範圍。 如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

使用書簽將游標放在索引上的方式有兩種。 第一個是使用書簽直接在記錄上定位。 當目前的資料指標索引為主要索引時，就會發生這種情況。 這項技術的運作方式是因為 ESENT 書簽與相關記錄的主鍵相同。

使用書簽的第二種方式是將它放在次要索引的專案上，其對應于與該書簽相關聯的記錄。 在這個過程中，引擎會使用主要索引上的書簽來查閱實際記錄。 然後，它會使用記錄資料和次要索引定義，將索引鍵計算到指向記錄的次要索引。 然後，它會將游標放在該索引鍵的索引項目上。 如果資料指標目前位於一個或多個多重值索引鍵資料行的次要索引上，則資料指標將定位於對應于每個索引鍵資料行之第一個多重值的索引項目目。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)
