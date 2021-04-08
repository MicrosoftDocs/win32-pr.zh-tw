---
description: 深入瞭解： JetOpenDatabase 函數
title: JetOpenDatabase 函式
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695667"
---
# <a name="jetopendatabase-function"></a>JetOpenDatabase 函式


_**適用于：** Windows |Windows Server_

## <a name="jetopendatabase-function"></a>JetOpenDatabase 函式

**JetOpenDatabase** 函式會使用 [JetAttachDatabase](./jetattachdatabase-function.md)或 [JetAttachDatabase2](./jetattachdatabase2-function.md)函數來開啟先前附加的資料庫，以搭配資料庫會話使用。 您可以針對相同的資料庫多次呼叫這個函數。

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*szFilename*

要開啟之資料庫的名稱。

*szConnect*

保留的。 設定為 NULL。

*pdbid*

在成功呼叫時，緩衝區的指標，其中包含資料庫的識別碼。 如果呼叫失敗，則值為未定義。

*grbit*

指定零或多個下列選項的位群組。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDbExclusive</p></td>
<td><p>只允許單一會話附加資料庫。 一般來說，數個會話可以開啟資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbReadOnly</p></td>
<td><p>防止修改資料庫。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>已要求獨佔存取權，但無法授與。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p><em>SzFilename</em>中提供了不正確路徑。 <em>szFilename</em> 必須為非 Null，並參考有效的檔案。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>另一個會話已 (使用 JET_bitDbExclusive) ，以獨佔方式開啟資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>嘗試開啟的檔案不是有效的資料庫檔案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>嘗試開啟一個以上的資料庫，並已設定 <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> 。 如需詳細資訊，請參閱 <a href="gg294139(v=exchg.10).md">系統參數</a>。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>檔案已附加為唯讀，但 <strong>JetOpenDatabase</strong> 未通過 JET_bitDbReadOnly。 資料庫仍會以唯讀存取權開啟。</p></td>
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
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetOpenDatabaseW</strong> (Unicode) 和 <strong>JetOpenDatabaseA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
