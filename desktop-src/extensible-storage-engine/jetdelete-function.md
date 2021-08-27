---
description: 深入瞭解： JetDelete 函數
title: JetDelete 函式
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e5d8fe6cfc4e0521866a12383aa34f7858432d3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477604"
---
# <a name="jetdelete-function"></a>JetDelete 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdelete-function"></a>JetDelete 函式

**JetDelete** 函數會刪除資料庫資料表中的目前記錄。

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>參數

*sesid*

將用於 API 呼叫的資料庫會話內容。

*tableid*

資料庫資料表上的資料指標。 將會刪除目前的資料列。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errCallbackFailed</p> | <p>回呼函式的運作方式失敗。 例如，會攔截回回呼函式中的存取違規，並將其轉譯成 JET_errCallbackFailed。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errIllegalOperation</p> | <p><em>Tableid</em>所指定的資料指標不支援刪除。 請參閱＜備註＞一節。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p><em>Tableid</em>指定的資料指標不在記錄上。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errPermissionDenied</p> | <p>資料庫引擎沒有足夠的許可權可刪除記錄。 如果資料庫檔案以唯讀存取權開啟，就可能發生這種情況。</p> | 
| <p>JET_errRollbackError</p> | <p>更新緩衝區 (看到 <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) 存在，但不是對 JET_coltypLongBinary 類型的資料 JET_coltypLongText 行所做的所有變更，也可能會回復類型的資料行。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>同時從一個以上的執行緒使用相同的會話是不合法的。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errTransReadOnly</p> | <p>交易是唯讀交易，不支援刪除。</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>作業失敗，因為沒有足夠的記憶體可保留有關更新的交易資訊。</p> | 
| <p>JET_errWriteConflict</p> | <p>另一個會話先前已鎖定記錄以進行更新。 此會話嘗試的更新將會失敗。</p> | 



成功時，會將貨幣保留在下一筆記錄的正上方。 如果刪除的記錄是資料表中的最後一個，則會將貨幣留在資料表的結尾 (也就是在新的最後一筆記錄) 之後。 如果刪除的記錄是資料表中唯一的記錄，則會將貨幣設定為開頭。

系統會自動更新適當的索引。

如果已備妥更新 (使用 [JetPrepareUpdate](./jetprepareupdate-function.md)) ，將會取消該更新。 更新緩衝區將會重設。

失敗時，貨幣會維持不變。 如果已備妥更新 (請參閱 [JetPrepareUpdate](./jetprepareupdate-function.md)) ，更新緩衝區可能會重設。

#### <a name="remarks"></a>備註

並非所有資料表都支援刪除資料列。 臨時表通常不支援刪除資料列。 可能會因為許多原因而對臨時表啟用刪除記錄，其中一些原因如下：

  - 建立期間指定了 JET_bitTTUpdatable。

  - 如果大型臨時表是使用 JET_bitTTScrollable 或 JET_bitTTIndexed 所建立，則可以支援刪除。 臨時表變成「大型」的臨界值目前為 64 kb，但在未來的版本中可能會變更。

WindowsXP 和更新版本。 **JetDelete** 可叫用回呼函式，包括 JET_cbtypBeforeDelete 和 JET_cbtypAfterDelete。

請務必瞭解在單一交易內執行大量更新作業的影響。 資料庫引擎必須在版本存放區中追蹤資料庫的每個更新。 版本存放區會保留資料庫中每個記錄或索引項目目之所有不同版本的即時記錄，以供所有使用中的交易看到。 這些版本是用來支援資料庫引擎使用的多版本並行控制，以支援使用快照集隔離的交易。 一旦資料庫引擎耗盡用來儲存這些版本的資源之後，就無法再接受進一步的變更，直到某些交易已結束，才能回收這些資源。 當引擎處於這種狀態時，所有更新都會失敗並 JET_errVersionStoreOutOfMemory。 資料庫引擎用來儲存這些版本的資源，可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 *JET_paramMaxVerPages* 和 *JET_paramGlobalMinVerPages* 來控制。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
