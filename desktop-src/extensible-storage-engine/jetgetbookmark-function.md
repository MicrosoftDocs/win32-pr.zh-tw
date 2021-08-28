---
description: 深入瞭解： JetGetBookmark 函數
title: JetGetBookmark 函式
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b75e40205dc25d467a010499ef0083c7ad87c47
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477964"
---
# <a name="jetgetbookmark-function"></a>JetGetBookmark 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetbookmark-function"></a>JetGetBookmark 函式

**JetGetBookmark** 函式會在資料指標目前位置的索引項目目相關聯的記錄中，抓取與該記錄相關聯的書簽。 然後，您可以使用這個書簽，將該資料指標重新放置到使用 [JetGoToBookmark](./jetgotobookmark-function.md)的相同記錄。

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pvBookmark*

接收書簽的輸出緩衝區。

*cbMax*

輸出緩衝區的大小上限（以位元組為單位）。

*pcbActual*

書簽的實際大小（以位元組為單位）。

如果這個參數為 **Null** ，則不會傳回書簽的實際大小。

如果輸出緩衝區太小，則仍會傳回書簽的實際大小。 這表示這個數位會大於輸出緩衝區的大小。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBufferTooSmall</p> | <p>作業已順利完成，但輸出緩衝區太小，無法接收整個書簽。 輸出緩衝區已填滿適當的書簽。 如果要求，也會傳回書簽的實際大小。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong>此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>資料指標未放置在記錄上。 此情況具有許多不同的原因。 例如，如果游標位於目前索引的最後一筆記錄之後，就會發生這種情況。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p><strong>Windows XP：</strong>此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果此函式成功，則會在輸出緩衝區中傳回與資料指標目前位置的索引項目目相關聯之記錄的書簽。 不會變更資料庫狀態。

如果此函式失敗，除非傳回 JET_errBufferTooSmall，否則輸出緩衝區的狀態和書簽的實際大小將會是未定義的。 在傳回 JET_errBufferTooSmall 的事件中，輸出緩衝區將會包含所提供空間中最多的書簽，而且書簽的實際大小將會正確。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

書簽通常應該視為不透明的資料區塊。 不應嘗試利用此資料的內部結構。 但是，下列條件適用于所有的 ESENT 書簽：

  - 書簽可唯一識別指定資料表中的記錄。

  - 在記錄的存留期內，記錄的書簽不會變更。

  - 記錄的書簽與包含該記錄之資料表的主要索引索引鍵相同。 如果未在該資料表上定義任何主要索引，database engine 將會為該記錄建立自己的書簽。

  - 您可以使用 [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) 函式來相互比較書簽，以便在來源記錄的資料表上建立主要索引的相對順序。 如果未在該資料表上定義任何主要索引，則使用該資料表中書簽的相對順序並沒有意義。

  - 比較不同資料表中的記錄書簽是無意義的。

  - 在 Windows Vista 之前，書簽一律小於或等於 JET_cbBookmarkMost (256) 位元組長度。
    
**Windows Vista：** 在 Windows Vista 和更新版本中，書簽可以大於 JET_cbBookmarkMost (256) 位元組。 書簽的大小上限等於 JET_paramKeyMost + 1 目前的值。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
