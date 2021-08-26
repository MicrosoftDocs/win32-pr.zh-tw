---
description: 深入瞭解： JetGetSecondaryIndexBookmark 函數
title: JetGetSecondaryIndexBookmark 函式
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a27d34b2622c5fe4ce2c72e3781394457e9cc20
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472517"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetsecondaryindexbookmark-function"></a>JetGetSecondaryIndexBookmark 函式

**JetGetSecondaryIndexBookmark** 函式會在資料指標目前的位置，抓取次要索引項目的特殊書簽。 然後，您可以使用這個書簽，利用 [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)將該資料指標有效率地重新放置到相同的索引項目。 當在包含重複索引鍵或包含相同記錄之多個索引項目的次要索引上重新置放時，這非常有用。

**Windows xp： JetGetSecondaryIndexBookmark** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pvSecondaryKey*

接收次要金鑰的輸出緩衝區。

*cbSecondaryKeyMax*

次要索引鍵之輸出緩衝區的大小上限（以位元組為單位）。

*pcbSecondaryKeyActual*

接收次要金鑰的實際大小（以位元組為單位）。

如果這個參數是 Null，將不會傳回次要索引鍵的實際大小。

如果輸出緩衝區太小，則仍會傳回次要金鑰的實際大小。 這表示這個數位會大於輸出緩衝區的大小。

*pvPrimaryBookmark*

接收主要金鑰書簽的輸出緩衝區。

*cbPrimaryBookmarkMax*

主鍵書簽輸出緩衝區的大小上限（以位元組為單位）。

*pcbPrimaryKeyActual*

接收主要金鑰書簽的實際大小（以位元組為單位）。

如果這個參數為 Null，則不會傳回主要索引鍵書簽的實際大小。

如果輸出緩衝區太小，則仍會傳回主要金鑰書簽的實際大小。 這表示這個數位會大於輸出緩衝區的大小。

*grbit*

保留供未來使用。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBufferTooSmall</p> | <p>作業已順利完成，但其中一個輸出緩衝區太小，無法接收要求的資料。</p><p>輸出緩衝區已填滿適當的書簽。 如果要求，也會傳回書簽的實際大小。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>資料指標目前不在次要索引上。</p><p>當資料指標目前未使用次要索引時，抓取次要索引書簽並沒有意義。 當資料指標不在次要索引上時，應使用<a href="gg269221(v=exchg.10).md">JetGetBookmark</a> 。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>資料指標未放置在記錄上。</p><p>此情況具有許多不同的原因。 例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，會在輸出緩衝區中傳回索引項目在資料指標目前位置的次要索引書簽。 不會變更資料庫狀態。

失敗時，除非傳回 JET_errBufferTooSmall，否則輸出緩衝區的狀態和次要索引書簽的實際大小將會是未定義的。 在傳回 JET_errBufferTooSmall 的事件中，輸出緩衝區會包含最多的次要索引書簽，以容納提供的空間，而次要索引書簽的實際大小將會是正確的。 在任何情況下，都不會變更資料庫狀態。

#### <a name="remarks"></a>備註

書簽通常應該視為不透明的資料區塊。 不應嘗試利用此資料的內部結構。 不過，您可以知道所有 ESENT 書簽的下列屬性：

  - 書簽可唯一識別指定資料表中的記錄。

  - 在記錄的存留期內，記錄的書簽不會變更。

  - 記錄的書簽與包含該記錄之資料表的主要索引索引鍵相同。 如果未在該資料表上定義任何主要索引，database engine 將會為該記錄建立自己的書簽。

  - 您可以使用 memcmp，在來源記錄的資料表中建立主要索引的相對順序，以使用[](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))來比較書簽。 如果未在該資料表上定義任何主要索引，則該資料表中的書簽相對順序將沒有意義。

  - 比較不同資料表中的記錄書簽是無意義的。

  - 書簽一律小於或等於 JET_cbBookmarkMost (256) 位元組的長度，Windows Vista 之前。 在 Windows Vista 和更新版本中，書簽可以更大。 書簽的大小上限等於 JET_paramKeyMost + 1 目前的值。

金鑰通常應該視為不透明的資料區塊。 不應嘗試利用此資料的內部結構。 不過，您可以知道所有 ESENT 機碼的下列屬性：

  - 您可以使用 [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) 來相互比較索引鍵，以在來源索引項目目的資料表中建立原始索引的相對順序。

  - 將索引項目的索引鍵與不同索引的索引鍵進行比較是無意義的。

  - 金鑰一律小於或等於 JET_cbKeyMost (255) 個位元組，Windows Vista 之前的長度。 在 Windows Vista 和更新版本中，金鑰可以更大。 索引鍵的大小上限等於 JET_paramKeyMost 目前的值。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
