---
description: 深入瞭解： JetResizeDatabase 函數
title: JetResizeDatabase 函式
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dd7faf1a28d6cafe7b33e4df49f32c631bb699e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477524"
---
# <a name="jetresizedatabase-function"></a>JetResizeDatabase 函式


_**適用于：** Windows |Windows伺服器_

**JetResizeDatabase** 函式會擴充或縮減目前開啟之資料庫的大小。

**JetResizeDatabase** 函式是在 Windows 8 作業系統中引進的。

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*dbid*

將擴充的資料庫。

*Cpg*

要求的資料庫大小（以頁面為限）。

*pcpgActual*

在 API 呼叫之後，接收資料庫大小（以頁面為限）的數位指標。 如果 API 呼叫失敗， *pcpgActual* 參數的內容會是未定義的。

*grbit*

一組位，指定下表所列的零或多個值。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitResizeDatabaseOnlyGrow</p> | <p>只增加資料庫。 如果調整大小呼叫會壓縮資料庫，則不執行任何動作。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。 如需可能的可延伸儲存體引擎 (ESE) 錯誤的詳細資訊，請參閱[可擴展的儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errDiskFull</p> | <p>磁片區上的可用空間不足，無法執行成長作業。</p> | 
| <p>JET_errDiskIO</p> | <p><a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>函數傳回檔案相關的錯誤。 如需可能傳回之其他檔案相關錯誤的詳細資訊，請參閱 <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>。</p> | 



#### <a name="remarks"></a>備註

如果在插入大量資料之前呼叫 **JetResizeDatabase** 函數，則會在一項作業中成長資料庫檔案。 這樣可以減少資料庫檔案在檔案系統層級上的片段，也可以減少資料庫檔案必須成長的次數。 成長資料庫檔案一次可能會比將其成長數次快。

若要設定未開啟之資料庫的大小，請參閱 [JetSetDatabaseSize](./jetsetdatabasesize-function.md)。

檔案大小可能不符合 *pcpgReal* 參數中所傳回的頁面數目。 *PcpgReal* 參數中可能不會計算兩個額外的保留頁面。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows 8。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2012。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
