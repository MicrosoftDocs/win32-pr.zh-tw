---
description: 深入瞭解： JetGetDatabaseFileInfo 函數
title: JetGetDatabaseFileInfo 函式
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b19d783480a8d82485bce32689b8d49e046b0285
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623504"
---
# <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo 函式

**JetGetDatabaseFileInfo** 函式會抓取與資料庫相關的各種資訊類型。 當資料庫已附加或線上 (使用 [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) ，或資料庫或資料庫引擎離線 (**JetGetDatabaseFileInfo**) 時，可以呼叫這個 API。

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>參數

*szDatabaseName*

從中取得資訊的資料庫路徑。

*pvResult*

將接收指定資訊之緩衝區的指標。 緩衝區的大小（以位元組為單位）會以 *cbMax* 傳遞。

如果此函式失敗， *pvResult* 的內容會是未定義的。

儲存在 *pvResult* 中的資訊取決於 *InfoLevel*。

*cbMax*

傳入 *pvResult* 的緩衝區大小（以位元組為單位）。

*InfoLevel*

*InfoLevel* 指定應該針對指定的資料庫抓取何種類型的資訊。 它會影響 *pvResult* 的解讀方式。 某些 *InfoLevel* 物件僅適用于離線 (**JetGetDatabaseFileInfo**) 或線上 ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) 版本的 API。

如果提供的 *pvResult* 緩衝區太小，可能會傳回 JET_errInvalidBufferSize 或 JET_errBufferTooSmall，視 *InfoLevel* 而定。

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvResult</em> 將會被視為 QWORD (8 個位元組) 。 傳回資料庫的大小（以位元組為單位）。</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoUpgrade</p></td>
<td><p><em>pvResult</em> 將會被視為 <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>。 <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>結構將會填入與指定資料庫相關的資訊。</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> 將會被視為 <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>。 <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>結構將會填入與指定資料庫相關的資訊。</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoDBInUse</p></td>
<td><p><em>pvResult</em> 將會被視為 BOOL (4 個位元組) 。 這會傳回資料庫引擎目前是否有任何開啟或附加的資料庫。</p>
<p><strong>Windows XP：</strong>此值會在 Windows XP 中引進。</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p><em>pvResult</em> 將會被視為不帶正負號的 long。 這會傳回資料庫的頁面大小（以位元組為單位）。</p>
<p><strong>Windows XP：</strong>此值會在 Windows XP 中引進。</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>這些 <em>InfoLevels</em> 尚未受到支援，並會傳回預設值。 請勿使用這些 <em>InfoLevels</em>。</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>這些 <em>InfoLevels</em> 尚未受到支援，並會傳回預設值。 請勿使用這些 <em>InfoLevels</em>。</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCollate</p></td>
<td><p>與 JET_DbInfoCp 相同。</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>這些 <em>InfoLevels</em> 已被取代，目前不受支援。 請勿使用這些 <em>InfoLevels</em>。</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>與 JET_DbInfoIsam 相同。</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFileType</p></td>
<td><p><strong>Windows Vista：</strong>此<em>InfoLevel</em>值會在 Windows Vista 中引進。</p>
<p><em>pvResult</em> 會被視為 DWORD 指標。 傳回列舉值，這個值表示引擎將此視為何種檔案類型。 下表列出檔案類型。 如需這些檔案類型及其使用方式的詳細資訊，請參閱可擴展的<a href="gg294069(v=exchg.10).md">儲存體引擎</a>檔案。</p>
<div class="tableSection">
<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_filetypeUnknown</p></td>
<td><p>檔案類型未知，或不是 ESE 檔案類型。</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeDatabase</p></td>
<td><p>檔案是資料庫檔案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeLog</p></td>
<td><p>檔案是交易記錄檔。</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeCheckpoint</p></td>
<td><p>檔案是檢查點檔案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeTempDatabase</p></td>
<td><p>檔案是暫存的資料庫檔案。</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>描述</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>JET_DbInfoIsam 要求的 <em>InfoLevel</em> 。 不支援此連結方式。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBufferTooSmall</p></td>
<td><p><em>CbMax</em>中提供的緩衝區太小，無法取得所需的資訊。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p><em>CbMax</em>中提供的緩衝區不是所需資訊的正確大小。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或多個參數值的組合產生了非預期的結果。 當提供的 DBID 不是附加) 資料庫的有效 (時， <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> 會傳回這個錯誤。 當該版本的函式不支援要求的<em>InfoLevel</em>時， <strong>JetGetDatabaseFileInfo</strong>和<a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a>會傳回此錯誤。</p></td>
</tr>
</tbody>
</table>


如果此函式成功，則會在輸出緩衝區中傳回所要求的資料。

如果此函式失敗，輸出緩衝區將會處於未定義狀態。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col  />
<col  />
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetGetDatabaseFileInfoW</strong> (Unicode) 和 <strong>JetGetDatabaseFileInfoA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)
