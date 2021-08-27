---
description: 深入瞭解： JetRegisterCallback 函數
title: JetRegisterCallback 函式
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ef90466b736facf5bd9fefee31c0449964d003b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985801"
---
# <a name="jetregistercallback-function"></a>JetRegisterCallback 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetregistercallback-function"></a>JetRegisterCallback 函式

**JetRegisterCallback** 函式可讓應用程式設定 database engine，以對應用程式發出特定事件的通知。 這些通知會與特定的資料表相關聯，而且只有在包含資料表的實例使用 [JetTerm](./jetterm-function.md)關閉時，才會維持有效。

**Windows xp： JetRegisterCallback** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*cbtyp*

由應用程式希望接收通知的回呼原因所組成的位元遮罩。

若要建立此位元遮罩，請將 [JET_CBTYP](./jet-cbtyp.md) 列舉中的有效回呼原因直接或一起建立。

*pCallback*

應用程式回呼函數的函式指標。

*pvCoNtext*

指定將給予應用程式回呼函式的內容指標。

*phCallbackId*

傳回可稍後用來取消註冊使用 [JetUnregisterCallback](./jetunregistercallback-function.md)之指定回呼函數的控制碼。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 <strong>JetRegisterCallback</strong>會在下列情況傳回此錯誤：</p><ul><li><p><em>cbtyp</em> 為零，</p></li><li><p><em>pCallback</em> 為 Null。</p></li><li><p><em>phCallbackId</em> 為 Null。</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，會使用與指定資料指標相關聯的資料表，針對給定的回呼原因註冊指定的回呼。 不會變更資料庫狀態。

失敗時，將不會註冊回呼。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

這個方法提供一種方法，讓應用程式將 volatile 回呼與資料庫中的資料表產生關聯。 如果應用程式希望將保存的回呼與資料庫中的資料表產生關聯，則應該使用[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)將回呼傳遞給[JET_TABLECREATE](./jet-tablecreate-structure.md) 。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetTerm](./jetterm-function.md)  
[JetUnregisterCallback](./jetunregistercallback-function.md)
