---
description: 深入瞭解： JetRestoreInstance 函數
title: JetRestoreInstance 函式
TOCTitle: JetRestoreInstance Function
ms:assetid: 7ba2b6ee-96f5-44c5-9842-5e58580f60f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269306(v=EXCHG.10)
ms:contentKeyID: 32765597
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestoreInstanceW
- JetRestoreInstance
- JetRestoreInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 700cbb29fe34700da953df5a20aa94d5a2df4a06
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985661"
---
# <a name="jetrestoreinstance-function"></a>JetRestoreInstance 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetrestoreinstance-function"></a>JetRestoreInstance 函式

**JetRestoreInstance** 函式會還原和復原實例的串流備份，包括所有附加的資料庫。 它是設計來搭配使用 [JetBackupInstance](./jetbackupinstance-function.md) 函式所建立的備份。 這是最簡單且最封裝的還原功能。

**Windows xp：****JetRestoreInstance** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetRestoreInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a>參數

*實例*

指定要用於此呼叫的實例。

針對 Windows XP 和更新版本，此參數的使用取決於引擎的作業模式。 如果引擎是在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可以是 null，也可以設定為包含 null 或 JET_instanceNil 的有效輸出緩衝區，此緩衝區會傳回做為初始化的副作用所建立的全域實例控制碼。 然後，這個實例控制碼可以傳遞給任何其他接受實例的 API。 如果引擎是在多重實例模式中作業，則這個參數必須設定為有效的輸入緩衝區，其中包含正在初始化的 [JetCreateInstance](./jetcreateinstance-function.md) 所傳回的實例控制碼。

*深圳*

備份所在的資料夾。 應使用 [JetBackup](./jetbackup-function.md) api 來產生備份。

*szDest*

將從備份組複製和復原資料庫檔案的資料夾名稱。 如果這是設定為 Null (這是舊版 [JetRestore](./jetrestore-function.md)) 的情況，則會將資料庫檔案複製和復原到其原始位置。

*pfn*

函式的選擇性指標，將會呼叫該函式做為還原作業進度的通知資訊。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>作業失敗，因為此實例的引擎已初始化。</p> | 
| <p>JET_errInvalidLogSequence</p> | <p>來自備份組和目前記錄檔路徑的記錄檔集合不相符。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 當引擎處於多重實例模式時， <strong>JetRestoreInstance</strong>會傳回這個錯誤，而 pinstance 指的是不正確實例 Windows XP 和更新的版本。</p> | 
| <p>JET_errInvalidPath</p> | <p>作業失敗，因為提供的部分路徑 (備份路徑、目的地路徑、實例的記錄檔或系統路徑) 無效。</p> | 
| <p>JET_errPageSizeMismatch</p> | <p>作業失敗，因為引擎設定 <a href="gg294044(v=exchg.10).md">為使用資料庫</a> 頁面大小 (針對 <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) 不符合用來建立交易記錄檔的資料庫頁面大小，或與交易記錄檔相關聯的資料庫。</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>作業失敗，因為參數隱含的單一實例模式 (Windows 2000 相容性) 模式，而引擎已在多重實例模式中。</p> | 



成功時，會將備份組的資料庫檔案還原至其位置，並執行復原，讓資料庫處於乾淨的交易一致性狀態。 如果有這類檔案，復原將會從備份組和記錄檔路徑中重新執行記錄檔。 這項復原會導致變更檢查點檔案、交易記錄檔，以及這些交易記錄檔所參考的任何資料庫。

失敗時，實例會保持未初始化的狀態。 交易記錄檔的狀態以及這些交易記錄檔所參考的任何資料庫，在嘗試初始化還原和復原資料庫時，可能已經變更。

#### <a name="remarks"></a>備註

復原進程會在備份期間重建附加至實例的資料庫，並將變更儲存回資料庫檔案。 結果會是交易一致的資料庫。 可能的話，它也會儲存到資料庫中，因為備份是在交易記錄中找到最新的變更之後所做的變更。 如果建立備份後產生的交易記錄仍存在於交易記錄檔目錄中，就可能會發生這種情況。 請注意，如果已啟用實例的迴圈記錄，則會重複使用所產生的交易記錄，讓復原能夠儲存在備份時所發生的變更。 在任何情況下，如果要對資料庫重新執行的交易記錄檔數目很大，則此程式可能需要相當長的時間。

您必須在已經使用 [JetCreateInstance](./jetcreateinstance-function.md)建立的實例上呼叫 **JetRestoreInstance** 。

由於復原期間會使用大量的資料庫頁面和交易記錄，因此有一系列的錯誤可能會由這些函數傳回。 這類錯誤可能來自暫時性的資源配置失敗，例如 Jet_errOutOfMemory 為代表實體損毀的錯誤，例如 JET_errReadVerifyFailure、JET_errLogFileCorrupt 或 JET_errBadPageLink。 這些錯誤幾乎都是由硬體問題所造成，因此無法避免。 檔案 mismanagement 本身最常是 JET_errMissingLogFile 或 JET_errAttachedDatabaseMismatch 或 JET_errDatabaseSharingViolation 或 JET_errInvalidLogSequence 的資訊清單。 這些錯誤是由應用程式所 preventable。 應用程式必須小心保護這些檔案的存放庫，使其不受使用者或其他應用程式這類外部強制操作的影響。 如果應用程式想要完全終結實例，則必須刪除與該實例相關聯的所有檔案。 這些包括檢查點檔案、交易記錄檔，以及附加至實例的任何資料庫檔案。

復原的不同步驟將會產生事件記錄檔專案，包括交易記錄檔的重新執行進度和最後的還原結果。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetRestoreInstanceW</strong> (Unicode) 和 <strong>JetRestoreInstanceA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetBackup](./jetbackup-function.md)  
[JetBackupInstance](./jetbackupinstance-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
