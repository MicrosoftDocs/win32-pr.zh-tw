---
description: 深入瞭解： JetCloseDatabase 函數
title: JetCloseDatabase 函式
TOCTitle: JetCloseDatabase Function
ms:assetid: e17a05dd-c30b-4e8f-8538-91a65e8052d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294123(v=EXCHG.10)
ms:contentKeyID: 32765737
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 606a99610843b822635217042ee3293c53570d42d3a8c17baee0b5416d45ec54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472438"
---
# <a name="jetclosedatabase-function"></a>JetCloseDatabase 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetclosedatabase-function"></a>JetCloseDatabase 函式

**JetCloseDatabase** 函式會關閉先前以 [JetOpenDatabase](./jetopendatabase-function.md)開啟的資料庫檔案。

```cpp
    JET_ERR JET_API JetCloseDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

將用於 API 呼叫的資料庫會話內容。

*dbid*

要關閉的資料庫。

*grbit*

保留供未來使用。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>描述</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>先前未開啟資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p><em>Dbid</em>參數不是有效的資料庫識別碼。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p><strong>程式庫</strong></p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)
