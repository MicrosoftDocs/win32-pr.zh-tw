---
description: 深入瞭解： JetSetLS 函數
title: JetSetLS 函式
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511114"
---
# <a name="jetsetls-function"></a>JetSetLS 函式


_**適用于：** Windows |Windows Server_

## <a name="jetsetls-function"></a>JetSetLS 函式

**JetSetLS** 函數可讓應用程式將稱為本機儲存的內容控制碼與資料指標或與該資料指標相關聯的資料表產生關聯。 應用程式可以使用此內容控制碼來儲存與資料指標或資料表相關聯的輔助資料。 當內容控制碼必須釋放時，應用程式稍後會使用執行時間回呼來通知。 這樣就可以將動態配置的狀態與資料指標或資料表產生關聯。

**Windows xp：**  **JetSetLS** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*ls*

要與資料指標或資料表相關聯的內容控制碼。

當指定 JET_bitLSReset 時，會忽略這個參數的實際值，並使用 JET_LSNil。

*grbit*

位群組，其中包含要用於此呼叫的選項，包括下列零或多個。

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
<td><p>此選項表示內容控制碼應該與指定的資料指標相關聯。</p>
<p>如果沒有指定 JET_bitLSCursor 或 JET_bitLSTable，則會假設 JET_bitLSCursor。</p>
<p>搭配 JET_bitLSTable 使用此選項是不合法的。 如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSReset</p></td>
<td><p>此選項表示應該忽略指定的內容控制碼，並將所選物件的內容控制碼重設為 JET_LSNil。</p>
<p>請務必注意，此動作不會導致回呼清除所選物件的先前內容控制碼值。 您可以使用 <a href="gg269234(v=exchg.10).md">JetGetLS</a> 搭配 JET_bitLSReset 來完成先前內容控制碼的適當清除。 如需詳細資訊，請參閱 <a href="gg269234(v=exchg.10).md">JetGetLS</a> 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>此選項表示內容控制碼應該與指定資料指標相關聯的資料表相關聯。</p>
<p>搭配 JET_bitLSCursor 使用此選項是不合法的。 如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>其中一個要求的選項無效、使用不正確或未執行。 當同時指定 JET_bitLSCursor 和 JET_bitLSTable 時， <strong>JetSetLS</strong> 可能會發生這種情況。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet</p></td>
<td><p>給定的內容控制碼無法與要求的物件建立關聯，因為它已經有與其相關聯的內容控制碼。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified</p></td>
<td><p>給定的內容控制碼無法與要求的物件建立關聯，因為尚未針對與會話相關聯的實例設定執行時間回呼。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
</tbody>
</table>


成功時，指定的內容控制碼已成功與要求的物件相關聯。 不會變更資料庫狀態。

失敗時，不會變更所要求物件的狀態。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

資料指標或資料表的本機儲存區應視為暫時性快取。 應用程式應該會先嘗試使用 [JetGetLS](./jetgetls-function.md)來取出內容控制碼。 如果未將值設定 (也就是 JET_LSNil) 則應用程式應該建立新的內容，並使用 **JetSetLS** 將它載入至快取。 應用程式可以使用 JET_bitLSReset 呼叫 [JetGetLS](./jetgetls-function.md) 來清除快取。 如果資料庫引擎清除快取，則會產生執行時間回呼，讓應用程式有機會清除該內容。 回呼型別會針對與資料指標相關聯的內容控制碼 JET_cbtypFreeCursorLS，以及與資料表相關聯之內容控制碼的 JET_cbtypFreeTableLS。 無論是哪一種情況，內容控制碼都會以 pvArg1 的形式傳遞。 如需詳細資訊，請參閱 [JET_CALLBACK](./jet-callback-callback-function.md) 。

在可以使用本機儲存體之前，必須為與指定會話相關聯的實例正確設定執行時間回呼。 您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramRuntimeCallback](./callback-parameters.md)來設定此回呼。 如需詳細資訊，請參閱系統參數中的 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 和 [JET_paramRuntimeCallback](./callback-parameters.md) 。

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
<td><p>需要 Windows Server 2008 或 Windows Server 2003。</p></td>
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

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLS](./jetgetls-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
