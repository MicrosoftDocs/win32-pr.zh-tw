---
description: 深入瞭解： JetSetColumnDefaultValue 函數
title: JetSetColumnDefaultValue 函式
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b4c624e985cbbef41d3e2a96133af97de6ea250e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984381"
---
# <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetcolumndefaultvalue-function"></a>JetSetColumnDefaultValue 函式

**JetSetColumnDefaultValue** 函數可以用來變更現有資料行的預設值。

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*dbid*

此呼叫所要使用的資料庫。

*szTableName*

包含將受影響之資料行的資料表名稱。

*szColumnName*

將變更其預設值的資料行名稱。

*pvData*

包含新預設值的輸入緩衝區。

*cbData*

包含新預設值的輸入緩衝區大小。

*grbit*

保留供未來使用。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>與 JET_errNullInvalid 相同。</p> | 
| <p>JET_errColumnInUse</p> | <p>索引目前正在使用這個指定的資料行。</p><p><strong>JetSetColumnDefaultValue</strong> 無法變更索引定義中所參考之資料行的預設值。 這是因為這樣做可能會變更索引的內容。</p> | 
| <p>JET_errColumnNotFound</p> | <p>這個資料表的指定資料行不存在。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>指定的資料庫識別碼無效。</p> | 
| <p>JET_errInvalidName</p> | <p>其中一個指定的物件名稱無效。 所有物件名稱都必須符合同一組規則。 這些規則如下：</p><ul><li><p>物件名稱必須由 ASCII 字元組成。</p></li><li><p>物件名稱的長度必須至少有一個字元。</p></li><li><p>物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</p></li><li><p>物件名稱不能以空格開頭。</p></li><li><p>物件名稱不能包含 ASCII 控制字元 (0x00 到 0x1F) 。</p></li><li><p>物件名稱不能包含驚嘆號 (！ ) 、句號 (. ) 、左括弧 ( [) 或右括弧 (] ) 字元。</p></li><li><p>一旦經過驗證之後，就只會將字串的部分寫入第一個空格 (如果有任何) 將用於物件名稱。 這表示物件名稱不能包含空格。</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errNullInvalid</p> | <p>無法將資料行設定為 Null。 這發生于 <strong>JetSetColumnDefaultValue</strong> 的時機：</p><ul><li><p><em>cbData</em> 為零。</p></li><li><p><strong>pvData</strong> 為 Null。</p></li></ul><p>因此，您無法將資料行的預設值 () 回 Null 或長度為零的值。</p> | 
| <p>JET_errObjectNotFound</p> | <p>此資料庫的指定資料表不存在。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTableInUse</p> | <p>這個指定的資料表正由另一個會話所使用。</p><p><strong>JetSetColumnDefaultValue</strong>需要資料表的獨佔存取權，才能針對 Windows Server 2003 之前的版本，變更資料行的預設值。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errTransReadOnly</p> | <p>在唯讀交易範圍內嘗試進行更新是不合法的。 「唯讀交易」（read only transaction）是指使用 JET_bitTransactionReadOnly 呼叫 <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> 來啟動的交易。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errWriteConflict</p> | <p>另一個會話先前已鎖定記錄以進行更新。 此會話嘗試的更新將會失敗。</p> | 



成功時，指定資料庫中指定之資料表的指定資料行預設值會永久變更為新的預設值。

失敗時，將不會變更資料庫狀態。

#### <a name="remarks"></a>備註

您無法變更範本資料表中之資料行的預設值。

資料庫引擎會以無訊息方式將長文字和長二進位資料行的資料行預設值截斷為255個位元組。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetSetColumnDefaultValueW</strong> (Unicode) 和 <strong>JetSetColumnDefaultValueA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[JetStopService](./jetstopservice-function.md)
