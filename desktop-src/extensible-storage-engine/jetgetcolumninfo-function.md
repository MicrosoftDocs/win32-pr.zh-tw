---
description: 深入瞭解： JetGetColumnInfo 函數
title: JetGetColumnInfo 函式
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985248"
---
# <a name="jetgetcolumninfo-function"></a>JetGetColumnInfo 函式


_**適用于：** Windows |Windows Server_

## <a name="jetgetcolumninfo-function"></a>JetGetColumnInfo 函式

**JetGetColumnInfo** 函數會抓取資料行的相關資訊。

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*dbid*

識別包含從中抓取資訊之資料行的資料表，以及 *szTableName*。

*szTableName*

識別包含從中抓取資訊之資料行的資料表，以及 *dbid*。

*szColumnName*

提取資訊所針對的資料行名稱。

*pvResult*

將接收資訊的緩衝區指標。 緩衝區的類型取決於 *InfoLevel*。 呼叫端必須設定為適當地對齊緩衝區。

*cbMax*

在 *pvResult* 中傳遞的緩衝區大小（以位元組為單位）。

*InfoLevel*

要針對 *szColumnName* 所指定的資料行取得的資訊類型。 *PvResult* 中儲存的資料格式取決於此參數。 如需臨時表的架構，請參閱 [JET_COLUMNLIST](./jet-columnlist-structure.md)。

這些 *InfoLevels* 的差異如下：

  - JET_ColInfoListSortColumnid 會依 *columnid* 排序臨時表。

  - JET_ColInfoListCompact 將壓縮輸出。 如需 compact 輸出的詳細資訊，請參閱 [JET_COLUMNLIST](./jet-columnlist-structure.md)。

下列選項可用於此參數。

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
<td><p>JET_ColInfo</p></td>
<td><p>JET_ColInfo 和 JET_ColInfoByColid 都會取得相同的資訊。 <em>pvResult</em> 會被視為 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>，而 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> 結構的欄位會適當地填入。</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBase</p></td>
<td><p><em>pvResult</em> 會被視為 <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> 結構。 這類似于 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> 結構。 如果此函式成功，則會以適當的值填入結構。 如果此函式失敗，結構會包含未定義的資料。</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoByColid</p></td>
<td><p>就像 JET_ColInfo 一樣， <em>pvResult</em> 會被視為 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>，但此 <em>InfoLevel</em> 表示要求的資料行 (<em>szColumName</em>) 不是字串資料行名稱，而是指向 <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>的指標。</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoList</p></td>
<td><p><em>pvResult</em> 會被視為 <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> 結構。 如果此函式成功，則會以適當的值填入結構。 臨時表會開啟，並由<a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>結構的<strong>tableid</strong>成員識別。 資料表必須以 <a href="gg294087(v=exchg.10).md">JetCloseTable</a>關閉。 如果此函式失敗，結構會包含未定義的資料。</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoListCompact</p></td>
<td><p>與 JET_ColInfoList 相同。</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoListSortColumnid</p></td>
<td><p>等同于 JET_ColInfoList;不過，產生的資料表會依 columnid 排序，而不是資料行名稱。</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoSysTabCursor</p></td>
<td><p>JET_ColInfoSysTabCursor 已被取代，而且使用它將會傳回 JET_errFeatureNotAvailable。</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBaseByColId</p></td>
<td><p>就像 JET_ColInfoBase 一樣， <em>pvResult</em> 會被視為 <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>，但此 <em>InfoLevel</em> 表示要求的資料行 (<em>szColumName</em>) 不是字串資料行名稱，而是指向 <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>的指標。</p>
<p><strong>Windows Vista：  </strong>此值是在 Windows Vista 中引進。</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitNonDerivedColumnsOnly</p></td>
<td><p>只有當資料表衍生自範本) 時，才會傳回非衍生的資料行 (。</p>
<p>當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</p>
<p><strong>Windows Vista：  </strong>這個值是 Windows Vista 引進的。</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoGrbitMinimalInfo</p></td>
<td><p>只傳回資料行名稱和每個資料行的 columnid。</p>
<p>當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</p>
<p><strong>Windows Vista：  </strong>此值是在 Windows Vista 中引進。</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitSortByColumnid</p></td>
<td><p>依 columnid 排序傳回的資料行清單 (預設為依資料行名稱排序清單) 。</p>
<p>當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</p>
<p><strong>Windows Vista：  </strong>此值是在 Windows Vista 中引進。</p></td>
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
<td><p>JET_errColumnNotFound</p></td>
<td><p>在資料表中找不到名為 <em>szColumnName</em> 的資料行。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>指定了不正確的 <em>InfoLevel</em> 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>下列情況可能會傳回此錯誤：</p>
<ul>
<li><p>指定了 <em>szTableName</em> 的錯誤名稱。</p></li>
<li><p>指定了 <em>szColumnName</em> 的錯誤名稱。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>下列情況可能會傳回此錯誤：</p>
<ul>
<li><p>指定了不正確的 <em>InfoLevel</em> 。</p></li>
<li><p>傳入的是 Null <em>szTableName</em> 。</p></li>
<li><p>緩衝區太小。</p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>備註

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) 和 **JetGetColumnInfo** 都能取出資料行的相關資訊。 它們之間的差異在於如何識別資料表：

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) 會依 *tableid* 識別資料表。

  - **JetGetColumnInfo** 會依 *dbid* 和 *szTableName* 組合來識別資料表。

使用 JET_ColInfoList、JET_ColInfoListSortColumnid 或 JET_ColInfoListCompact 來抓取資料時，將會開啟臨時表。 臨時表包含資料，而 [JET_COLUMNLIST](./jet-columnlist-structure.md) 結構包含足夠的資訊來跨越臨時表。 臨時表必須以 [JetCloseTable](./jetclosetable-function.md)關閉。

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
<td><p>實作為 <strong>JetGetColumnInfoW</strong> (Unicode) 和 <strong>JetGetColumnInfoA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[錯誤處理參數](./error-handling-parameters.md)  
[可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
