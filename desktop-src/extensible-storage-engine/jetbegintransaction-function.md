---
description: 深入瞭解： JetBeginTransaction 函數
title: JetBeginTransaction 函式
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 991f80ab346ae039c6222a508374de806d0faf2c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479264"
---
# <a name="jetbegintransaction-function"></a>JetBeginTransaction 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetbegintransaction-function"></a>JetBeginTransaction 函式

**JetBeginTransaction** 函式會讓會話進入交易並建立新的儲存點。 您可以在單一會話上多次呼叫此函數，以建立額外的儲存點。 您可以使用這些儲存點，選擇性地保留或捨棄資料庫狀態的變更。

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errTransTooDeep</p> | <p>無法啟動新的交易，因為會話已經是 database engine 允許的最大儲存點深度。</p> | 



成功時，所提供的會話將會在交易內。 如果會話先前是在交易內，則會建立新的儲存點。

失敗時，會話的交易式狀態將保持不變。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

資料庫引擎會為其交易提供快照集隔離模型。 這表示，當會話第一次進入交易狀態時，會話會在交易開始時看到整個資料庫凍結。 會話不需要讀取任何資料，因為它一律可以存取該資料的適當版本。 這表示正在更新資料的會話絕不會封鎖不同的會話讀取該資料。

使用快照集隔離的另一種含意是用於更新的鎖定模型。 資料庫引擎會將指定資料片段的寫入鎖定，獎勵給要求它的第一個會話。 當交易已完全認可或中止，讓會話不再存在於交易中時，就會釋放此寫入鎖定。 當會話保留寫入鎖定時，任何其他要求相同寫入鎖定的會話都不會封鎖，直到有寫入鎖定為止。 相反地，第二個會話將會在 JET_errWriteConflict 時立即失敗。 若要解決此衝突，第二個會話必須完全中止 (或認可) 其交易，請等候一小段時間讓第一個會話認可或中止交易，然後再重新開機所有。

為了支援快照集隔離，資料庫引擎會將所有修改過之資料的所有版本儲存在記憶體中，因為在第一次啟動任何會話的最舊使用中交易時。 這對您的應用程式有重要的影響。 造成大量版本在記憶體中建立的任何行為，可能會導致實例耗盡其最大版本存放區大小 (如需詳細資訊) ，請參閱[系統參數](./extensible-storage-engine-system-parameters.md) [JET_paramMaxVerPages](./resource-parameters.md) 。 這類行為包括（但不限於）單一交易中的大量更新和執行中的交易。 因此，請務必正確地為應用程式的預期交易載入設定版本存放區大小。 也請務必小心限制在單一交易中執行的更新數目。 此外，在高負載案例下，盡可能將交易的時間縮短得很短。

強烈建議應用程式在呼叫可捕獲或更新資料的 ESE Api 時，一律在交易內容中。 如果未這麼做，database engine 就會將此類型的每個 ESE API 呼叫自動包裝在交易中，以代表應用程式。 在某些情況下，這些非常簡短的交易成本可以快速增加。

引擎的預設行為是在呼叫 **JetBeginTransaction** 的第一次呼叫時，將會話限制在相同的執行緒上，直到發出 [JetCommitTransaction](./jetcommittransaction-function.md) 或 [JetRollback](./jetrollback-function.md) 的相符呼叫為止。 您可以使用 [JetSetSessionCoNtext](./jetsetsessioncontext-function.md) 和 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md)設定自訂會話內容，來變更此行為以移除這項限制。

資料庫引擎也支援交易式架構修改。 例如，您可以開始新的交易、建立資料表、新增幾個資料行、建立一個或兩個索引，然後中止交易。 剛才加入的架構元素將會從資料庫中移除。 您也可以在相同的交易中混用架構修改和一般資料庫更新。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetResetSessionCoNtext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionCoNtext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
