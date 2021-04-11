---
description: 深入瞭解： JetTerm2 函數
title: JetTerm2 函式
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113601"
---
# <a name="jetterm2-function"></a>JetTerm2 函式


_**適用于：** Windows |Windows Server_

## <a name="jetterm2-function"></a>JetTerm2 函式

**JetTerm2** 函式會起始由 [JetInit](./jetinit-function.md)初始化之實例的關機。

**JetTerm2** 也可以終結由 [JetCreateInstance](./jetcreateinstance-function.md)所建立的未初始化實例。

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的實例。

**Windows 2000：**  此參數會被忽略，且應一律為 **Null**。

**WINDOWS XP 和更新版本：**  此參數已多載。 如果引擎在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 **Null** 或包含 [JetInit](./jetinit-function.md)所傳回的實際實例。 如果引擎以多重實例模式運作，則此參數必須是使用 [JetCreateInstance](./jetcreateinstance-function.md)建立之實例的指標。

*grbit*

位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列值。

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
<td><p>JET_bitTermComplete</p></td>
<td><p>要求完全關閉實例。 通常會在執行時間于背景中完成的任何選擇性清除工作會立即完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermAbrupt</p></td>
<td><p>要求實例盡可能快速關閉。 在執行時間，通常會在背景中完成的任何選擇性工作都會被放棄。</p>
<p><strong>注意</strong>  此選項可能會在資料庫中造成暫存或永久的空間遺失。 這個遺失的空間隨時都可以透過資料庫的離線磁碟重組來復原。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTermStopBackup</p></td>
<td><p>要求即使目前正在進行備份，也會關閉實例。 一般來說，暫止的備份會導致 <a href="gg269298(v=exchg.10).md">JetTerm</a> 失敗，並 JET_errBackupInProgress。 如果這個參數不存在，則會假設其值為 JET_bitTermAbrupt。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermDirty</p></td>
<td><p>要求將所有附加的資料庫都保持在中途狀態時，關閉實例。</p>
<p>Windows 7： JET_bitTermDirty 是在 Windows 7 中引進的。</p></td>
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
<td><p>JET_errBackupInProgress</p></td>
<td><p>作業無法完成，因為實例上的備份作業正在進行中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或數個參數的組合產生了非預期的結果。 當引擎處於多重實例模式時，以及<em>pinstance</em>參考不正確實例時， <a href="gg269298(v=exchg.10).md">JetTerm</a>會傳回這個錯誤。</p>
<p><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為尚未初始化實例。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成操作，因為正在關閉實例。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為實例上的還原作業正在進行中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyActiveUsers</p></td>
<td><p>因為目前的會話具有指定實例的使用中交易，所以無法關閉實例。 只有使用 JET_bitTermComplete 時，才會發生此錯誤。</p></td>
</tr>
</tbody>
</table>


如果此函數成功，將會關閉指定的實例。 實例控制碼也將會關閉，並且可供任何採用實例控制碼的 API 使用。 與實例相關聯的所有其他物件（例如會話）也會關閉。 檢查點檔案、交易記錄檔和附加至實例的資料庫檔案的狀態，會在關閉程式期間進行修改。

如果此函式因使用錯誤而失敗，則實例會維持在初始化狀態，而且不會有任何變更。 否則，實例仍會依照成功案例的規定關閉。 不同之處在于實例在下次初始化時，必須經歷損毀復原。 引擎會嘗試盡可能將最多的資料排清，以將所需的復原量降至最低。 就概念而言， [JetTerm](./jetterm-function.md) 失敗與進程損毀並無不同。

#### <a name="remarks"></a>備註

請參閱 [JetTerm](./jetterm-function.md)。

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

[可擴充儲存引擎檔案](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm](./jetterm-function.md)
