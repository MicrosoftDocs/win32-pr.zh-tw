---
description: 深入瞭解： JetCommitTransaction2 函數
title: JetCommitTransaction2 函式
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6080380fd8326504e7b1182b439571e3904f0d53
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986061"
---
# <a name="jetcommittransaction2-function"></a>JetCommitTransaction2 函式


_**適用于：** Windows |Windows伺服器_

**JetCommitTransaction2** 函式會在目前的儲存點期間認可對資料庫狀態所做的變更，並將其遷移至先前的儲存點。 如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。

**JetCommitTransaction2** 函式是在 Windows 8 作業系統中引進的。

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*grbit*

一組位，指定下表所列的零或多個值。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitCommitLazyFlush</p> | <p>交易會正常認可，但此 API 不會等到交易被排清到交易記錄檔，然後再傳回給呼叫者。 這可大幅減少認可作業的持續時間，代價是持久性。 在下一次呼叫 <a href="gg294068(v=exchg.10).md">JetInit</a> 函式期間，任何未在損毀之前排清到記錄檔的交易都會自動中止。</p><p>如果指定 JET_bitWaitLastLevel0Commit 或 JET_bitWaitAllLevel0Commit，則會忽略此選項。</p><p>如果這個 <strong>JetCommitTransaction2</strong> 呼叫不符合此會話的第一次呼叫 <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> 函數，則會忽略此選項。 這是因為在最外層儲存點上發生的最後一個動作，就是整個交易實際上是否認可到磁片的決定因素。</p> | 
| <p>JET_bitWaitAllLevel0Commit</p> | <p>所有先前由尚未排清至交易記錄檔的會話所認可的交易，都會立即進行清除。 此 API 會等到交易已排清之後，再返回呼叫端。</p><p>即使會話目前不在交易中，也可以使用此選項。</p><p>此選項不能與任何其他選項搭配使用。</p><p>從 Windows Server 2003 開始，Windows Server 作業系統的版本中有提供此選項。</p> | 
| <p>JET_bitWaitLastLevel0Commit</p> | <p>如果會話先前已認可任何交易，而且它們尚未排清到交易記錄檔，則應該立即排清它們。 此 API 會等到交易已排清之後，再返回呼叫端。 如果應用程式先前已使用 JET_bitCommitLazyFlush 認可數筆交易，而現在想要將所有交易排清到磁片上，這項功能就很有用。</p><p>即使會話目前不在交易中，也可以使用此選項。</p><p>此選項不能與任何其他選項搭配使用。</p> | 



*cmsecDurableCommit*

認可延遲交易的持續時間。

*pCommitID*

與此認可記錄相關聯的認可識別碼。

### <a name="return-value"></a>傳回值

此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。 如需可能的可延伸儲存體引擎 (ESE) 錯誤的詳細資訊，請參閱[可擴展的儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p>此錯誤只會由 Windows XP 起的 Windows 作業系統版本傳回。</p> | 
| <p>JET_errInvalidgrbit</p> | <p>其中一個要求的選項無效或未執行。 當發生下列情況時， <strong>JetCommitTransaction2</strong> 函式會傳回這個錯誤：</p><ul><li><p>指定了不合法的 <em>grbit</em> 。</p></li><li><p>JET_bitWaitLastLevel0Commit 已與另一個 <em>grbit</em>一起指定。</p></li><li><p>JET_bitWaitAllLevel0Commit 已與另一個 <em>grbit</em>一起指定。</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errNotInTransaction</p> | <p>作業失敗，因為指定的會話不在交易中。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p>此錯誤只會由 Windows XP 起的 Windows 作業系統版本傳回。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，將會認可指定會話目前儲存點期間對資料庫所做的任何變更，而且儲存點將會結束。 如果會話的最後一個儲存點已結束，則交易會選擇性地排清至交易記錄檔，而且會話將會結束交易。

失敗時，會話的交易式狀態將保持不變。 不會變更資料庫狀態。 應用程式應該呼叫 [JetRollback](./jetrollback-function.md) 函數來中止交易。

#### <a name="remarks"></a>備註

必須呼叫 **JetCommitTransaction2** 或 [JetRollback](./jetrollback-function.md) ，以比對指定會話的每個 [JetBeginTransaction](./jetbegintransaction-function.md) 呼叫。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows 8。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2012。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
