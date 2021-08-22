---
description: 深入瞭解： JetUpdate 函數
title: JetUpdate 函式
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e02550fb40987906e21d588263daed9dc68aa5d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478244"
---
# <a name="jetupdate-function"></a>JetUpdate 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetupdate-function"></a>JetUpdate 函式

**JetUpdate** 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。 藉由呼叫 [JetDelete](./jetdelete-function.md)來執行刪除資料表資料列。

**JetUpdate** 是執行插入或更新的最後一個步驟。 此更新的開始方式是呼叫 [JetPrepareUpdate](./jetprepareupdate-function.md) ，然後呼叫 [JetSetColumn](./jetsetcolumn-function.md) 或 [JetSetColumns](./jetsetcolumns-function.md) 一或多次來設定記錄狀態。 最後，會呼叫 **JetUpdate** 來完成更新作業。 只有 **JetUpdate** 或 [JetUpdate2](./jetupdate2-function.md)才會更新索引，而不是在 [JetSetColumn](./jetsetcolumn-function.md) 或 [JetSetColumns](./jetsetcolumns-function.md)期間更新。

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pvBookmark*

插入之資料列的傳回書簽指標。

*cbBookmark*

*PvBookmark* 所指向的緩衝區大小。

*pcbActual*

在 *pvBookmark* 中傳回的插入資料列之書簽的傳回大小。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBufferTooSmall</p> | <p>記錄書簽的指定緩衝區不夠大，無法儲存記錄書簽。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>與 JET_errNullInvalid 相同。</p> | 
| <p>JET_errDiskFull</p> | <p>更新作業需要資料庫檔案成長或記錄檔配置，但是資料庫檔案或記錄檔所在的磁片磁碟機已滿。 或者，資料庫檔案位於 FAT32 格式化的磁片區上，且資料庫檔案已4GBytes，也就是針對 FAT32 的每個檔案限制。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>函式中指定的<em>準備</em>參數不是有效的旗標。</p> | 
| <p>JET_errKeyDuplicate</p> | <p>此記錄的索引鍵是資料表中已經有另一筆記錄的另一個索引鍵重複的索引鍵，且索引不允許重複。</p> | 
| <p>JET_errKeyTruncated</p> | <p>插入或更新的記錄有一或多個索引，而產生的索引鍵會超過允許的大小上限。 因此，作業無法防止金鑰截斷。</p> | 
| <p>JET_errMultiValuedIndexViolation</p> | <p>插入或更新的記錄中有一個索引多值資料行，其中有兩個以上的值，在為索引設定的最大長度索引鍵大小中都相同。 如此一來，該記錄在索引中會有兩個相同的專案無效。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errNullInvalid</p> | <p>要插入之記錄中的一個或多個資料行，或在要取代之記錄的更新狀態為 <strong>Null</strong> ，這違反了這些資料行的定義條件約束。</p> | 
| <p>JET_errNullKeyDisallowed</p> | <p>定義了一或多個索引，不允許 <strong>Null</strong> 索引鍵，而且所取代之記錄的插入或更新狀態違反了此定義的條件約束。</p> | 
| <p>JET_errRecordPrimaryChanged</p> | <p>記錄取代作業已更新 primary key。 主鍵資料行的更新必須透過刪除現有的記錄，並使用所需的資料插入新記錄來完成。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errTransReadOnly</p> | <p>在唯讀交易範圍內嘗試進行更新是不合法的。 「唯讀交易」（read only transaction）是指使用 JET_bitTransactionReadOnly 呼叫 <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> 來啟動的交易。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p>使用 JET_prepCancel 呼叫<a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> ，但資料指標不是處於已備妥的狀態。</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>作業失敗，因為沒有足夠的記憶體可保留有關更新的交易資訊。</p> | 
| <p>JET_errWriteConflict</p> | <p>另一個會話先前已鎖定記錄以進行更新。 此會話嘗試的更新將會失敗。</p> | 



成功時，資料指標上的開啟更新作業已完成。 如果為數據表定義了自動遞增資料行，就會針對插入的記錄設定這個值。 如果為數據表定義了版本資料行，則會為新插入的記錄初始化其值，或在每次取代記錄時遞增。 所有索引（包括叢集和非叢集索引）都會更新。

失敗時，不會對資料庫進行任何變更。 在插入之前和取代回呼函式之前，可能已經呼叫，但是在插入之後和取代的回呼都不會被呼叫，因為後者無法使更新失敗。 資料指標複製緩衝區會留在它的備妥狀態，如此一來，就有機會以累加方式更正造成錯誤的問題，然後重試更新作業。

#### <a name="remarks"></a>備註

您可以註冊回呼函式，以便在插入之前或之後，以及在更新之前或之後呼叫。

[JetSetColumn](./jetsetcolumn-function.md)會強制執行記錄大小限制，而不是 **JetUpdate** 一般。

請務必瞭解在單一交易內執行大量更新作業的影響。 資料庫引擎必須在版本存放區中追蹤資料庫的每個更新。 版本存放區會保留資料庫中每個記錄或索引項目目之所有不同版本的即時記錄，以供所有使用中的交易看到。 這些版本是用來支援資料庫引擎使用的多版本並行控制，以支援使用快照集隔離的交易。 一旦資料庫引擎耗盡用來儲存這些版本的資源之後，就無法再接受進一步的變更，直到某些交易已結束，才能回收這些資源。 當引擎處於這種狀態時，所有更新都會失敗並 JET_errVersionStoreOutOfMemory。 資料庫引擎用來儲存這些版本的資源，可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramMaxVerPages](./resource-parameters.md) 和 [JET_paramGlobalMinVerPages](./resource-parameters.md)來控制。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDelete](./jetdelete-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
