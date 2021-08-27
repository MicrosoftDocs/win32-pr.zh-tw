---
description: 深入瞭解： JetRenameColumn 函數
title: JetRenameColumn 函式
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c60418a0723214b2d2312ebe67a4f47184814e0a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470235"
---
# <a name="jetrenamecolumn-function"></a>JetRenameColumn 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetrenamecolumn-function"></a>JetRenameColumn 函式

**JetRenameColumn** 函數可以用來變更資料表中現有資料行的名稱。

**Windows xp：****JetRenameColumn** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*szName*

要重新命名之資料行的目前名稱。

*szNameNew*

將重新命名之資料行的新名稱。

*grbit*

此參數必須為0。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errColumnNotFound</p> | <p>這個資料表的指定資料行不存在。</p> | 
| <p>JET_errInvalidName</p> | <p>其中一個指定的物件名稱無效。 所有物件名稱都必須符合同一組規則。 這些規則如下：</p><ul><li><p>物件名稱必須由 ASCII 字元組成。</p></li><li><p>物件名稱的長度必須至少有一個字元。</p></li><li><p>物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</p></li><li><p>物件名稱的開頭不可以是空格-物件名稱不能包含 ASCII 控制字元， (0x00 到 0x1F) 。</p></li><li><p>物件名稱不能包含驚嘆號 (！ ) 、句號 (. ) 、左括弧 ( [) 或右括弧 (] ) 字元。</p></li><li><p>一旦經過驗證之後，就只會將字串的部分寫入第一個空格 (如果有任何) 將用於物件名稱。 這實際上是指物件名稱不能包含空格。</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 在下列情況下， <strong>JetRenameColumn</strong> 可能會發生：</p><ul><li><p><em>>szname</em> 為 Null。</p></li><li><p><em>szNameNew</em> 為 Null。</p></li></ul> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInTransaction</p> | <p>只有當會話目前不在交易中時，才可以執行這項作業。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errTransReadOnly</p> | <p>無法在唯讀交易範圍內完成更新。 唯讀交易是指使用 JET_bitTransactionReadOnly 呼叫 <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> 來啟動的交易。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 



成功時，與資料指標相關聯之資料表中指定的資料行名稱會永久變更為新的名稱。 任何參考該資料行的索引也會更新。

失敗時，將不會變更資料庫狀態。

#### <a name="remarks"></a>備註

資料行重新命名作業不尋常，因為與其他架構作業不同的是，它不會做為交易來執行。 當給定資料表中的資料行在某個會話中重新命名時，任何其他使用該資料表的會話都會立即看到變更，即使它們是在交易中，也會導致該會話無法看到執行重新命名作業的會話所做的任何其他變更。

重新命名作業不會影響資料行的資料行識別碼。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetRenameColumnW</strong> (Unicode) 和 <strong>JetRenameColumnA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
