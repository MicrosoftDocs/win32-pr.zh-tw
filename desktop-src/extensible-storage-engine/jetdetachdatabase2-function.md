---
description: 深入瞭解： JetDetachDatabase2 函數
title: JetDetachDatabase2 函式
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9141646c96d9318667cd11b41aade03363cab230
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474114"
---
# <a name="jetdetachdatabase2-function"></a>JetDetachDatabase2 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdetachdatabase2-function"></a>JetDetachDatabase2 函式

**JetDetachDatabase2** 函式會釋放先前附加至資料庫會話的資料庫檔案。

**Windows xp：****JetDetachDatabase2** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*szFilename*

要卸離的資料庫名稱。 如果 *szFilename* 為 **Null** 或空字串，則會卸離附加至 *sesid* 的所有資料庫。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitForceCloseAndDetach</p> | <p>強制關閉和卸離資料庫。 如果不支援 JET_bitForceCloseAndDetach，將會傳回 JET_errForceDetachNotAllowed。</p> | 
| <p>JET_bitForceDetach</p> | <p>強制卸離資料庫。 如果不支援 JET_bitForceDetach，將會傳回 JET_errForceDetachNotAllowed。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupInProgress</p> | <p>正在備份資料庫，且無法中斷連結。</p> | 
| <p>JET_errDatabaseInUse</p> | <p>資料庫已由 <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>開啟。 必須先關閉資料庫，然後再卸離。</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> 或 <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>) 。</p> | 
| <p>JET_errForceDetachNotAllowed</p> | <p>不支援 JET_bitForceDetach。</p> | 
| <p>JET_errInTransaction</p> | <p>嘗試在交易中卸離資料庫。</p> | 



#### <a name="remarks"></a>備註

如果已使用 [JetAttachDatabase](./jetattachdatabase-function.md)) 開啟附加的資料庫 (，則必須先將它關閉， [然後再卸](./jetclosedatabase-function.md) 離。

僅限 Windows 2000：下次呼叫[JetInit](./jetinit-function.md)時，未在呼叫[JetTerm](./jetterm-function.md)之前卸離的資料庫將會自動重新連接。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetDetachDatabase2W</strong> (Unicode) 和 <strong>JetDetachDatabase2A</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetInit](./jetinit-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetTerm](./jetterm-function.md)
