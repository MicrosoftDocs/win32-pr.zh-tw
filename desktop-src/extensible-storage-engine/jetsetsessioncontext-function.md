---
description: 深入瞭解： JetSetSessionCoNtext 函數
title: JetSetSessionCoNtext 函式
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61df6b5396a5bffcef4f7e32e9a2c32477d019e0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465285"
---
# <a name="jetsetsessioncontext-function"></a>JetSetSessionCoNtext 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetsessioncontext-function"></a>JetSetSessionCoNtext 函式

**JetSetSessionCoNtext** 函式會使用指定的內容控制碼，將會話與目前的執行緒產生關聯。 此關聯會覆寫指定會話的交易必須完全在相同執行緒上執行的預設引擎需求。

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*ulCoNtext*

將與此會話相關聯的唯一識別碼。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或多個參數值的組合產生了非預期的結果。 <strong>JetSetSessionCoNtext</strong>會在下列情況下傳回此錯誤：</p><ul><li><p><em>ulCoNtext</em> 為 Null</p></li><li><p><em>ulCoNtext</em> 為-1</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionCoNtextAlreadySet</p> | <p>會話無法與目前的執行緒建立關聯，因為它已經與執行緒相關聯。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果此函式成功，會話將會與目前的執行緒相關聯。 不會變更資料庫狀態。

如果此函式失敗，會話狀態會維持不變。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

在交易期間，會話通常會系結至特定的執行緒。 此行為的設計目的是協助應用程式偵測和防止在多個執行緒之間共用單一會話的概念不良。 有時候，這種簡單的檢查無法用於應用程式的架構。 例如，如果應用程式使用執行緒集區來裝載伺服器端物件，而且交易跨越對指定物件的多個伺服器呼叫，則這項保護可能會導致某些呼叫失敗，但 JET_errSessionSharingViolation 即使使用模式正確也一樣。 這種情況常見於 COM 物件伺服器。

**JetSetSessionCoNtext** 和 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md) 藉由讓此會話共用檢查更有彈性，來解決此問題。 當應用程式開始使用特定會話進行一連串的 ESE API 呼叫時，它會先將會話內容設定為指定的值。 此動作會將會話與呼叫執行緒產生關聯。 在給定的範例中，此內容可以是包含 JET 會話控制碼之物件的位址。 一旦進行了 ESE API 呼叫，應用程式就會重設會話內容。 此動作會解除會話與呼叫執行緒的之間的操作。 即使會話有使用中的交易，也可以由另一個執行緒使用物件和其會話。

請務必注意，必須先呼叫 **JetSetSessionCoNtext** ，才能在該會話上開啟交易，否則關聯將無法運作。

**JetSetSessionCoNtext** 具備執行緒安全。 多個執行緒可以嘗試同時在相同的會話上設定執行緒內容，而且只有一個會獲勝。 此事實可供應用程式用來從集區配置會話，而不會儲存其配置的外部狀態。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetResetSessionCoNtext](./jetresetsessioncontext-function.md)  
[JET_SESID](./jet-sesid.md)  
[JetStopService](./jetstopservice-function.md)
