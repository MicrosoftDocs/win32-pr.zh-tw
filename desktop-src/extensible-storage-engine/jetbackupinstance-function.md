---
description: 深入瞭解： JetBackupInstance 函數
title: JetBackupInstance 函式
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5cf601593d970f56be80b75ef5744295e7b4cf0941a6c401d8bae78c15542f21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889718"
---
# <a name="jetbackupinstance-function"></a>JetBackupInstance 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetbackupinstance-function"></a>JetBackupInstance 函式

**JetBackupInstance** 函式會執行實例（包括所有附加的資料庫）至目錄的資料流程備份。 如果引擎支援多個備份方法，這是最簡單且最簡單的封裝函數。

**Windows xp： JetBackupInstance** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a>參數

*實例*

要備份之資料庫的實例。

*szBackupPath*

儲存備份的目錄。 如果備份路徑為 Null，則使用函式會盡可能截斷記錄。

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
<td><p>JET_bitBackupAtomic</p></td>
<td><p>建立資料庫的完整備份。 這可在新備份失敗時，將現有的備份保留在相同的目錄中。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>建立增量備份，而不是完整備份。 這表示只會備份自上次完整或增量備份之後所建立的記錄檔。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>保留供未來使用。</p></td>
</tr>
</tbody>
</table>


*pfnStatus*

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)回呼函式的指標，它會提供有關備份作業進度的通知資訊。

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
<td><p>JET_errBackupInProgress</p></td>
<td><p>相同實例的備份已經在進行中。 不允許多個備份。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBackupNotAllowedYet</p></td>
<td><p>實例在初始化時尚未準備好進行備份。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>作業無法完成，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p><strong>Windows XP：</strong>此傳回值會在 Windows XP 中引進。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBackup</p></td>
<td><p>如果迴圈記錄開啟，則不允許增量備份。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>指定的選項無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>傳遞至 API 的參數無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>目的地路徑不存在。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLoggingDisabled</p></td>
<td><p>實例正在執行，但未記錄。 不允許備份。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>記錄檔發生總和檢查碼驗證錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errLogWriteFail</p></td>
<td><p>因為發生未預期的錯誤，所以實例的記錄是暫時性的或永久停用。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>資料庫頁面上發生總和檢查碼驗證錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。</p>
<p><strong>Windows XP：</strong>此傳回值會在 Windows XP 中引進。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p></td>
</tr>
</tbody>
</table>


在函式傳回成功之後，備份目錄中的所有還原備份所需的檔案都會出現在備份目錄中。 如果這是完整備份，檔案將會是資料庫檔案，以及將資料庫帶入一致狀態所需的記錄檔。 如果這是增量備份，則只會將記錄檔新增至目錄，但現有的檔案 (資料庫和記錄檔，) 連同新的記錄檔將可以還原，並使資料庫回到備份當時的狀態。

備份的副作用是，不再需要的記錄檔將會被截斷。

在相同的時間內，資料庫標頭會在最後一次備份時，以資訊更新。

失敗時，備份目錄目的地中將不會有任何檔案，因此不會有任何還原。 在相同的時間內，目前的記錄檔不會被截斷。

#### <a name="remarks"></a>備註

備份的不同步驟將會產生事件記錄檔專案，包括檔案名、記錄截斷，以及備份的最終結果。

只有在執行完整備份之後，才可能進行增量備份。 此外，只有在迴圈記錄關閉時，才可能進行增量備份。 建議備份目錄不應該包含其他檔案，然後是備份所牽涉的檔案，或是先前成功備份所新增的檔案。

除非針對實例設定了參數 *JET_paramCreatePathIfNotExist* ，否則備份目錄應該會存在。 如需詳細資訊，請參閱 [系統參數](./extensible-storage-engine-system-parameters.md)。

備份也會在所有已使用的資料庫頁面上進行總和檢查碼驗證，並且在記錄檔上從 Windows Server 2003 開始。 這讓您有機會評估資料庫的健全狀況，即使是在正常作業期間未讀取的頁面也是一樣。 如果發生任何這類損毀，備份將會失敗。

在備份期間，目前的記錄檔將會完成，而且我們會開始新的記錄產生。 這將允許複製所需的記錄檔，因為最後一個必要的記錄檔將不再使用。

強烈建議您不要將備份用於其他設定，然後備份並在引擎層級還原。 這可將在備份和還原作業期間取得錯誤的變更降至最低。

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetBackupInstanceW</strong> (Unicode) 和 <strong>JetBackupInstanceA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestore2](./jetrestore2-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
