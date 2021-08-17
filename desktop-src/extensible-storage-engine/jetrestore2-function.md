---
description: 深入瞭解： JetRestore2 函數
title: JetRestore2 函式
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38b669fdf38d6dcaffe5d8a0ac77c8ac362142faca2df03fb23eb45d869ed0ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117704042"
---
# <a name="jetrestore2-function"></a>JetRestore2 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetrestore2-function"></a>JetRestore2 函式

**JetRestore2** 會還原並復原實例的串流備份，包括所有附加的資料庫。 這個函數主要是為了與 Windows 2000 和舊版的資料庫引擎回溯相容，其中只允許一個資料庫的實例。 在此情況下，使用中的實例是已還原的實例。

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>參數

*深圳*

備份所在的資料夾。 應使用 [JetBackup](./jetbackup-function.md) api 來產生備份。

*szDest*

將從備份組複製和復原資料庫檔案的資料夾名稱。 如果這是設定為 Null (這是舊版 [JetRestore](./jetrestore-function.md)) 的情況，則會將資料庫檔案複製和復原到其原始位置。

*pfn*

函式的選擇性指標，將會呼叫該函式做為還原作業進度的通知資訊。

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
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>作業失敗，因為此實例的引擎已初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLogSequence</p></td>
<td><p>來自備份組和目前記錄檔路徑的記錄檔集合不相符。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 當引擎處於多重實例模式時， <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a>會傳回這個錯誤，而 pinstance 指的是不正確實例 Windows XP 和更新的版本。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>作業失敗，因為提供的部分路徑 (備份路徑、目的地路徑、實例的記錄檔或系統路徑) 無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errPageSizeMismatch</p></td>
<td><p>作業失敗，因為引擎設定 <a href="gg294044(v=exchg.10).md">為使用資料庫</a> 頁面大小 (針對 <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) 不符合用來建立交易記錄檔的資料庫頁面大小，或與交易記錄檔相關聯的資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>作業失敗，因為參數隱含的單一實例模式 (Windows 2000 相容性) 模式，而引擎已在多重實例模式中。</p></td>
</tr>
</tbody>
</table>


成功時，會將備份組的資料庫檔案還原至其位置，並執行復原，讓資料庫處於乾淨的交易一致性狀態。 如果有這類檔案，復原將會從備份組和記錄檔路徑中重新執行記錄檔。 這項復原會導致變更檢查點檔案、交易記錄檔，以及這些交易記錄檔所參考的任何資料庫。

失敗時，實例會保持未初始化的狀態。 交易記錄檔的狀態以及這些交易記錄檔所參考的任何資料庫，在嘗試初始化還原和復原資料庫時，可能已經變更。

#### <a name="remarks"></a>備註

復原進程會在備份期間重建附加至實例的資料庫，並將變更儲存回資料庫檔案。 結果會是交易一致的資料庫。 可能的話，它也會儲存到資料庫中，因為備份是在交易記錄中找到最新的變更之後所做的變更。 如果建立備份後產生的交易記錄仍存在於交易記錄檔目錄中，就可能會發生這種情況。 請注意，如果已啟用實例的迴圈記錄，則會重複使用所產生的交易記錄，讓復原能夠儲存在備份時所發生的變更。 在任何情況下，如果要對資料庫重新執行的交易記錄檔數目很大，則此程式可能需要相當長的時間。

在針對該實例呼叫[JetInit](./jetinit-function.md)之前，必須在實例上呼叫[JetRestore](./jetrestore-function.md)函數。

由於復原期間會使用大量的資料庫頁面和交易記錄，因此有一系列的錯誤可能會由這些函數傳回。 這類錯誤可能來自暫時性的資源配置失敗，例如 Jet_errOutOfMemory 為代表實體損毀的錯誤，例如 JET_errReadVerifyFailure、JET_errLogFileCorrupt 或 JET_errBadPageLink。 這些錯誤幾乎都是由硬體問題所造成，因此無法避免。 檔案 mismanagement 本身最常是 JET_errMissingLogFile 或 JET_errAttachedDatabaseMismatch 或 JET_errDatabaseSharingViolation 或 JET_errInvalidLogSequence 的資訊清單。 這些錯誤是由應用程式所 preventable。 應用程式必須小心保護這些檔案的存放庫，使其不受使用者或其他應用程式這類外部強制操作的影響。 如果應用程式想要完全終結實例，則必須刪除與該實例相關聯的所有檔案。 這些包括檢查點檔案、交易記錄檔，以及附加至實例的任何資料庫檔案。

復原的不同步驟將會產生事件記錄檔專案，包括交易記錄檔的重新執行進度和最後的還原結果。

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetRestore2W</strong> (Unicode) 和 <strong>JetRestore2A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetRestore](./jetrestore-function.md)  
[JetRestoreInstance](./jetrestoreinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
