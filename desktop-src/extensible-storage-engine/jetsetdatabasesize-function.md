---
description: 深入瞭解： JetSetDatabaseSize 函數
title: JetSetDatabaseSize 函式
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27799dbdbc21af4421713828633199d1c1a18973
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466220"
---
# <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize 函式

**JetSetDatabaseSize** 函式會設定未開啟之資料庫檔案的大小。

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>參數

*sesid*

識別要用於 API 呼叫的資料庫會話內容。

*szDatabaseName*

識別要改變其大小的資料庫檔案名。

*Cpg*

在頁面中指定所需的資料庫大小。

*pcpgReal*

在 API 呼叫之後，接收資料庫大小（以頁面為限）的數位指標。 如果 API 呼叫失敗， *pcpgReal* 的內容會是未定義的。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errDatabaseInconsistent<br />JET_errDatabaseDirtyShutdown</p> | <p>JET_errDatabaseInconsistent 和 JET_errDatabaseDirtyShutdown 是相同的數值。 要調整其大小的資料庫必須處於正常關機狀態，也就是所謂的一致狀態。 不一致的資料庫並未損毀，但需要重新執行記錄檔。</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p><em>szDatabaseName</em> 不得為空的非 Null 字串。</p> | 
| <p>JET_errDiskFull</p> | <p>磁片區上的可用空間不足，無法執行成長作業。 <strong>JetSetDatabaseSize</strong> 可能也會傳回許多與檔案相關的錯誤，包括但不限於：</p><ul><li><p>JET_errDiskIO</p></li><li><p>JET_errFileNotFound</p></li><li><p>JET_errInvalidPath</p></li><li><p>JET_errFileAccessDenied</p></li><li><p>JET_errOutOfFileHandles</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>可能會傳回此錯誤的其中一個原因是 <em>cpg</em> 符合資料庫大小下限。 目前的最小資料庫大小為256頁。</p> | 
| <p>JET_errOutOfMemory</p> | <p>系統的記憶體資源不足。</p> | 



#### <a name="remarks"></a>備註

如果在插入大量資料之前呼叫 **JetSetDatabaseSize** ，資料庫檔案將會在一項作業中成長。 這樣可以減少資料庫檔案在檔案系統層級上的片段，也可以減少資料庫檔案必須成長的次數。 成長資料庫檔案一次可能會比將其成長數次快。

目前只支援成長盤案。 若要壓縮檔案，請使用 esentutl.exe 公用程式的磁碟重組功能。

如果 *cpg* 小於資料庫的目前大小，則會忽略此作業。 如果 *cpg* 小於最小資料庫大小 (目前256頁) ，它將會傳回 JET_errInvalidParameter。

若要設定開啟的資料庫大小，請參閱 [JetGrowDatabase](./jetgrowdatabase-function.md)。

檔案大小可能不符合 *pcpgReal* 中傳回的頁面數目。 有兩個額外的保留頁面可能不會在 *pcpgReal* 中計算。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetSetDatabaseSizeW</strong> (Unicode) 和 <strong>JetSetDatabaseSizeA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetGrowDatabase](./jetgrowdatabase-function.md)
