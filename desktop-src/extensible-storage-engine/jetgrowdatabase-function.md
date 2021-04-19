---
description: 深入瞭解： JetGrowDatabase 函數
title: JetGrowDatabase 函式
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975136"
---
# <a name="jetgrowdatabase-function"></a>JetGrowDatabase 函式


_**適用于：** Windows |Windows Server_

## <a name="jetgrowdatabase-function"></a>JetGrowDatabase 函式

**JetGrowDatabase** 函數會擴充目前開啟之資料庫的大小。

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*dbid*

將擴充的資料庫。

*Cpg*

所需的資料庫大小（以頁面為限）。

*pcpgReal*

在 API 呼叫之後，接收資料庫大小（以頁面為限）的數位指標。 如果 API 呼叫失敗， *pcpgReal* 的內容會是未定義的。

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
<td><p>JET_errDiskFull</p></td>
<td><p>磁片區上的可用空間不足，無法執行成長作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO</p></td>
<td><p><a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>傳回檔案相關的錯誤。 如需可能傳回之其他檔案相關錯誤的詳細資訊，請參閱 <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>。</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>備註

如果在插入大量資料之前呼叫 **JetGrowDatabase** ，資料庫檔案將會在一項作業中成長。 這樣可以減少資料庫檔案在檔案系統層級上的片段，也可以減少資料庫檔案必須成長的次數。 成長資料庫檔案一次可能會比將其成長數次快。

目前只支援成長盤案。 若要壓縮檔案，請使用 **esentutl.exe** 公用程式的磁碟重組功能。

若要設定未開啟之資料庫的大小，請參閱 [JetSetDatabaseSize](./jetsetdatabasesize-function.md)。

檔案大小可能不符合 *pcpgReal* 中傳回的頁面數目。 有兩個額外的保留頁面可能不會在 *pcpgReal* 中計算。

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
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
