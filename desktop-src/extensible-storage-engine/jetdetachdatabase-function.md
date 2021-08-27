---
description: 深入瞭解： JetDetachDatabase 函數
title: JetDetachDatabase 函式
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a66010b5d056301e368f7221380966adc2f31180
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470463"
---
# <a name="jetdetachdatabase-function"></a>JetDetachDatabase 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdetachdatabase-function"></a>JetDetachDatabase 函式

**JetDetachDatabase** 函式會釋放先前附加至資料庫會話的資料庫檔案。

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*szFilename*

要卸離的資料庫名稱。 如果 *szFilename* 為 **Null** 或空字串，則會卸離附加至 *sesid* 的所有資料庫。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupInProgress</p> | <p>正在備份資料庫，且無法中斷連結。</p> | 
| <p>JET_errDatabaseInUse</p> | <p>資料庫已由 <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>開啟。 必須先關閉資料庫，然後再卸離。</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> 或 <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>) 。</p> | 
| <p>JET_errInTransaction</p> | <p>嘗試在交易中卸離資料庫。</p> | 



#### <a name="remarks"></a>備註

如果已使用 [JetAttachDatabase](./jetattachdatabase-function.md)) 開啟附加的資料庫 (，則必須先將它關閉， [然後再卸](./jetclosedatabase-function.md) 離。

僅限 Windows 2000：下次呼叫[JetInit](./jetinit-function.md)時，未在呼叫[JetTerm](./jetterm-function.md)之前卸離的資料庫將會自動重新連接。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetDetachDatabaseW</strong> (Unicode) 和 <strong>JetDetachDatabaseA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetTerm](./jetterm-function.md)
