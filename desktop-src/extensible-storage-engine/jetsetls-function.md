---
description: 深入瞭解： JetSetLS 函數
title: JetSetLS 函式
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c94e5dc01d2aff69b699894f88287122cb9530cf
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984281"
---
# <a name="jetsetls-function"></a>JetSetLS 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetls-function"></a>JetSetLS 函式

**JetSetLS** 函數可讓應用程式將稱為本機儲存體的內容控制碼與資料指標或與該資料指標相關聯的資料表產生關聯。 應用程式可以使用此內容控制碼來儲存與資料指標或資料表相關聯的輔助資料。 當內容控制碼必須釋放時，應用程式稍後會使用執行時間回呼來通知。 這樣就可以將動態配置的狀態與資料指標或資料表產生關聯。

**Windows xp：****JetSetLS** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*ls*

要與資料指標或資料表相關聯的內容控制碼。

當指定 JET_bitLSReset 時，會忽略這個參數的實際值，並使用 JET_LSNil。

*grbit*

位群組，其中包含要用於此呼叫的選項，包括下列零或多個。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitLSCursor</p> | <p>此選項表示內容控制碼應該與指定的資料指標相關聯。</p><p>如果沒有指定 JET_bitLSCursor 或 JET_bitLSTable，則會假設 JET_bitLSCursor。</p><p>搭配 JET_bitLSTable 使用此選項是不合法的。 如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</p> | 
| <p>JET_bitLSReset</p> | <p>此選項表示應該忽略指定的內容控制碼，並將所選物件的內容控制碼重設為 JET_LSNil。</p><p>請務必注意，此動作不會導致回呼清除所選物件的先前內容控制碼值。 您可以使用 <a href="gg269234(v=exchg.10).md">JetGetLS</a> 搭配 JET_bitLSReset 來完成先前內容控制碼的適當清除。 如需詳細資訊，請參閱 <a href="gg269234(v=exchg.10).md">JetGetLS</a> 。</p> | 
| <p>JET_bitLSTable</p> | <p>此選項表示內容控制碼應該與指定資料指標相關聯的資料表相關聯。</p><p>搭配 JET_bitLSCursor 使用此選項是不合法的。 如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInvalidgrbit</p> | <p>其中一個要求的選項無效、使用不正確或未執行。 當同時指定 JET_bitLSCursor 和 JET_bitLSTable 時， <strong>JetSetLS</strong> 可能會發生這種情況。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errLSAlreadySet</p> | <p>給定的內容控制碼無法與要求的物件建立關聯，因為它已經有與其相關聯的內容控制碼。</p> | 
| <p>JET_errLSCallbackNotSpecified</p> | <p>給定的內容控制碼無法與要求的物件建立關聯，因為尚未針對與會話相關聯的實例設定執行時間回呼。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，指定的內容控制碼已成功與要求的物件相關聯。 不會變更資料庫狀態。

失敗時，不會變更所要求物件的狀態。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

資料指標或資料表的本機儲存體應該視為暫時性快取。 應用程式應該會先嘗試使用 [JetGetLS](./jetgetls-function.md)來取出內容控制碼。 如果未將值設定 (也就是 JET_LSNil) 則應用程式應該建立新的內容，並使用 **JetSetLS** 將它載入至快取。 應用程式可以使用 JET_bitLSReset 呼叫 [JetGetLS](./jetgetls-function.md) 來清除快取。 如果資料庫引擎清除快取，則會產生執行時間回呼，讓應用程式有機會清除該內容。 回呼型別會針對與資料指標相關聯的內容控制碼 JET_cbtypFreeCursorLS，以及與資料表相關聯之內容控制碼的 JET_cbtypFreeTableLS。 無論是哪一種情況，內容控制碼都會以 pvArg1 的形式傳遞。 如需詳細資訊，請參閱 [JET_CALLBACK](./jet-callback-callback-function.md) 。

您必須針對與指定會話相關聯的實例適當地設定執行時間回呼，才能使用本機儲存體。 您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramRuntimeCallback](./callback-parameters.md)來設定此回呼。 如需詳細資訊，請參閱系統參數中的 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 和 [JET_paramRuntimeCallback](./callback-parameters.md) 。

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
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLS](./jetgetls-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
