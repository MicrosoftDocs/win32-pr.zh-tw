---
description: 深入瞭解： JetRollback 函數
title: JetRollback 函式
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e23bd408ec88109a0f77635ac53e89003df9a992
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985551"
---
# <a name="jetrollback-function"></a>JetRollback 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetrollback-function"></a>JetRollback 函式

**JetRollback** 函式會復原對資料庫狀態所做的變更，並返回到最後一個儲存點。 **JetRollback** 也會關閉儲存點期間開啟的任何資料指標。 如果最外層的儲存點復原，會話將會結束交易。

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*grbit*

位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitRollbackAll</p> | <p>此選項會要求所有儲存點在所有儲存點都復原時，對資料庫狀態所進行的所有變更。 因此，會話將會結束交易。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errNotInTransaction</p> | <p>作業失敗，因為指定的會話不在交易中。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errRollbackError</p> | <p>因為發生嚴重錯誤，所以無法復原變更。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，指定會話目前儲存點期間對資料庫所做的任何變更都會復原，而且儲存點將會結束。 如果會話的最後一個儲存點已結束，則會話會結束交易。

失敗時，會話的交易式狀態將保持不變。 不會變更資料庫狀態。 復原期間的失敗會視為嚴重的資料庫錯誤。

#### <a name="remarks"></a>備註

必須呼叫 [JetCommitTransaction](./jetcommittransaction-function.md) 或 **JetRollback** ，以比對指定會話的每個 [JetBeginTransaction](./jetbegintransaction-function.md) 呼叫。

如果 (使用 [JetOpenTable](./jetopentable-function.md)開啟任何資料指標，例如在要復原的儲存點期間) ，則會關閉該資料指標。

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
