---
description: 深入瞭解： JetComputeStats 函數
title: JetComputeStats 函式
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1324722ed0bd239f4c5b26fbd3340d45f325e53c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465815"
---
# <a name="jetcomputestats-function"></a>JetComputeStats 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetcomputestats-function"></a>JetComputeStats 函式

**JetComputeStats** 函式會逐步解說資料表的每個索引，以精確計算索引中的專案數，以及索引中的相異索引鍵數目。 這項資訊，以及配置給索引的資料庫頁面數目和目前的計算時間，都會儲存在資料庫的索引中繼資料中。 之後可以使用資訊作業來抓取此資料。

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

將用於此呼叫的資料指標。 描述要計算統計資料的資料表。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errRollbackError</p> | <p>要求此作業回復所有變更時發生錯誤，但交易回復本身失敗。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，最新的統計資料會儲存在與指定資料指標所描述之資料表的資料庫目錄中。

失敗時，不會對資料庫進行任何類型的更新。

#### <a name="remarks"></a>備註

這項作業可能會耗用資源，因為資料表中的每個索引都必須完整地進行。 [JetGetRecordPosition](./jetgetrecordposition-function.md) 可以用來取得索引中專案數目的粗略估計值，但無法自行估計索引中的相異值數目。

這項作業所計算的資料會開始過期，並在後續更新資料表。

**JetComputeStats** 對資料庫所做的更新會以延遲的方式進行。 這表示沒有任何記錄排清會伴隨此作業，而且 **JetComputeStats** 傳回 JET_errSuccess 後的系統損毀仍會導致這些更新遺失。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetStopService](./jetstopservice-function.md)
