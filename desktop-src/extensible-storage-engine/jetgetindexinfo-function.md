---
description: 深入瞭解： JetGetIndexInfo 函數
title: JetGetIndexInfo 函式
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997835"
---
# <a name="jetgetindexinfo-function"></a>JetGetIndexInfo 函式


_**適用于：** Windows |Windows Server_

## <a name="jetgetindexinfo-function"></a>JetGetIndexInfo 函式

**JetGetIndexInfo** 函式會捕獲索引的相關資訊。

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*dbid*

用於 API 呼叫的資料庫識別碼。

*szTableName*

包含索引的資料表名稱，其中包含要取出的資訊。

*szIndexName*

具有要取出之資訊的索引名稱。

*pvResult*

將接收所需資訊的緩衝區指標。 緩衝區應該對齊以保存所需的類型。 緩衝區的類型取決於 *InfoLevel* 參數。

*cbResult*

傳遞為 *pvResult* 的緩衝區大小（以位元組為單位）。

*InfoLevel*

將儲存在 *pvResult* 中的資訊。 下列選項可用於此參數。

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
<td><p>JET_IdxInfo</p></td>
<td><p><em>pvResult</em> 會被視為 <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構。 成功時， <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構會接收有關索引的資訊。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCount</p></td>
<td><p><em>pvResult</em> 會被解釋為 ULONG。 成功時，ULONG 會保存指定資料表上的索引計數。 <em>szIndexName</em> 會被忽略。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoIndexId</p></td>
<td><p><em>pvResult</em> 會被解釋為 <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>。 成功時， <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> 結構會接收有關索引的資訊。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoLangid</p></td>
<td><p>JET_IdxInfoLangid 已被取代。 請改用 JET_IdxInfoLCID 和 <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> 宏。</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoLCID</p></td>
<td><p><em>pvResult</em> 會被解釋為 LCID。 成功時，LCID 會保存索引的地區設定識別碼。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p>
<p><strong>WINDOWS XP：  </strong>JET_IdxInfoLCID 是在 Windows XP 中引進。</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoList</p></td>
<td><p><em>pvResult</em> 會被視為 <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構。 成功時， <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> 結構會接收有關索引的資訊。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoOLC</p></td>
<td><p>JET_IdxInfoOLC 已淘汰。</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoResetOLC</p></td>
<td><p>JET_IdxInfoResetOLC 已淘汰。</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoSpaceAlloc</p></td>
<td><p><em>pvResult</em> 會被解釋為 ULONG。 成功時，ULONG 會保存索引的空間使用量。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoSysTabCursor</p></td>
<td><p>JET_IdxInfoSysTabCursor 已淘汰。</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoVarSegMac</p></td>
<td><p><em>pvResult</em> 會被解釋為 USHORT。 成功時，USHORT 會保存建立索引時所使用的 <em>cbVarSegMac</em> 值。 如需<em>cbVarSegMac</em>的說明，請參閱<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoKeyMost</p></td>
<td><p><em>pvResult</em> 會被解釋為 USHORT。 成功時，USHORT 會保存建立索引時所使用的 <em>cbKeyMost</em> 值。 如需<em>cbKeyMost</em>的說明，請參閱<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p>
<p><strong>Windows Vista：  </strong>JET_IdxInfoKeyMost 是在 Windows Vista 中引進。</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoCreateIndex</p></td>
<td><p><em>pvResult</em> 會被視為 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 結構。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p>
<p><strong>Windows 7：  </strong>JET_IdxInfoCreateIndex 是在 Windows 7 中引進的。</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCreateIndex2</p></td>
<td><p><em>pvResult</em> 會被視為 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 結構。 失敗時， <em>pvBuffer</em> 的內容是未定義的。</p>
<p><strong>Windows 7：  </strong>JET_IdxInfoCreateIndex2 是在 Windows 7 中引進的。</p></td>
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
<td><p>JET_errIndexNotFound</p></td>
<td><p>在指定的資料表中找不到指定的索引。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>傳入作為 <em>pvResult</em> 的緩衝區太小。 緩衝區的內容是未定義的。</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>備註

**JetGetIndexInfo** 和 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) 會取得有關索引的相同資訊。 不同之處在于如何指定資料表。 **JetGetIndexInfo** 預期資料庫 (*dbid*) 和資料表名稱 (*szTableName*) ，而 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) 預期資料表識別碼 (*tableid*) 。

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
<td><p>實作為 <strong>JetGetIndexInfoW</strong> (Unicode) 和 <strong>JetGetIndexInfoA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
