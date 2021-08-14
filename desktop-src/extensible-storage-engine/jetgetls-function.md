---
description: 深入瞭解： JetGetLS 函數
title: JetGetLS 函式
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a359bb2899a2dea604e236a7118c914e795bffba7ca675229e28ad3a7f25dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979058"
---
# <a name="jetgetls-function"></a>JetGetLS 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetls-function"></a>JetGetLS 函式

**JetGetLS** 函式可讓應用程式取出與資料指標相關聯的內容句儲存體柄，或與該資料指標相關聯的資料表。 此內容控制碼必須先前已使用 [JetSetLS](./jetsetls-function.md)設定。 **JetGetLS** 也可以用來同時提取資料指標或資料表的目前內容控制碼，並重設該內容控制碼。

**Windows xp： JetGetLS** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pls*

輸出緩衝區，這個輸出緩衝區會接收目前與資料指標或資料表相關聯的內容控制碼。

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
<td><p>JET_bitLSCursor</p></td>
<td><p>表示應該抓取與指定之資料指標相關聯的內容控制碼。</p>
<p>如果沒有指定 JET_bitLSCursor 或 JET_bitLSTable，則會假設 JET_bitLSCursor。</p>
<p>此選項不能搭配 JET_bitLSTable 使用。 如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>表示應該抓取與包含指定資料指標之資料表相關聯的內容控制碼。 搭配 JET_bitLSCursor 使用此選項是不合法的。 如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>指出所選物件的內容控制碼應該重設為 JET_LSNil。 內容控制碼的目前值會在輸出緩衝區中傳回。</p></td>
</tr>
</tbody>
</table>


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
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>其中一個要求的選項無效、以不合法的方式使用，或未執行。</p>
<p>當 JET_bitLSCursor 和 JET_bitLSTable 都已設定時， <strong>JetGetLS</strong> 就會發生這種情況。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>無法傳回內容控制碼，因為目前沒有任何內容控制碼與要求的物件相關聯。</p>
<p><strong>注意  </strong> 如果指定 JET_bitLSReset 但沒有與要求的物件相關聯的內容控制碼，就不會傳回這個錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
</tbody>
</table>


成功時，已成功從要求的物件抓取內容控制碼。 如果指定 JET_bitLSReset，則也會成功從物件中移除該內容控制碼。 不會變更資料庫狀態。

失敗時，不會變更所要求物件的狀態。 不會變更資料庫狀態。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista 或 Windows XP。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows server 2008 或 Windows server 2003。</p></td>
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
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetLS](./jetsetls-function.md)
