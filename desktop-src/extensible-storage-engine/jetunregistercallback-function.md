---
description: 深入瞭解： JetUnregisterCallback 函數
title: JetUnregisterCallback 函式
TOCTitle: JetUnregisterCallback Function
ms:assetid: de5c7afa-07e1-4687-989b-b56125a9712e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294116(v=EXCHG.10)
ms:contentKeyID: 32765730
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUnregisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5cb60d8b0d06ff6af9d950c53d8bdf8f4eedb774
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466243"
---
# <a name="jetunregistercallback-function"></a>JetUnregisterCallback 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetunregistercallback-function"></a>JetUnregisterCallback 函式

**JetUnregisterCallback** 函式可讓應用程式設定 database engine，以在先前透過 [JetRegisterCallback](./jetregistercallback-function.md)要求時停止發出通知給應用程式。

**Windows xp：****JetUnregisterCallback** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetUnregisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_HANDLE hCallbackId
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*cbtyp*

由應用程式不再希望接收通知的回呼原因所組成的位元遮罩。

若要建立此位元遮罩，請直接或將有效的回呼原因從 [JET_CBTYP](./jet-cbtyp.md) 列舉。

*hCallbackId*

[JetRegisterCallback](./jetregistercallback-function.md)所傳回之已註冊回呼的控制碼。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果此函式成功，則會使用與指定資料指標相關聯的資料表，取消註冊指定的回呼，以找出指定的回呼原因。 不會變更資料庫狀態。

如果此函式失敗，將不會取消註冊指定的回呼。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

指定的位元遮罩應該完全符合註冊回呼時所指定的位元遮罩。 資料庫引擎目前不支援移除這些通知的子集，而且在嘗試這項功能時不會傳回錯誤。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetStopService](./jetstopservice-function.md)
