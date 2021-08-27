---
description: 深入瞭解： JetCloseFileInstance 函數
title: JetCloseFileInstance 函式
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d837d1932559c39d6a3b249f934ef77cc56de11a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982974"
---
# <a name="jetclosefileinstance-function"></a>JetCloseFileInstance 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetclosefileinstance-function"></a>JetCloseFileInstance 函式

**JetCloseFileInstance** 函式會在使用 [JetReadFileInstance](./jetreadfileinstance-function.md)解壓縮該檔案中的資料之後，關閉使用 [JetOpenFileInstance](./jetopenfileinstance-function.md)開啟的檔案。

**Windows xp： JetCloseFileInstance** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的實例。

針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。 在此情況下，這種全域實例的使用是隱含的。

針對 Windows XP 和更新版本，只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變體 (Windows 2000 相容性模式) 只支援一個實例。 否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。

*hfFile*

要讀取之檔案的控制碼。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或多個參數值的組合產生了非預期的結果。 在下列情況下， <strong>JetCloseFileInstance</strong> 可能會發生：</p><ul><li><p> (Windows XP 和更新版本中，指定的實例控制碼無效) </p></li><li><p>指定的檔案控制代碼無效</p></li></ul> | 
| <p>JET_errNoBackup</p> | <p>作業失敗，因為沒有任何外部備份正在進行中。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只有當有多個實例存在時，才支援一個實例。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，會關閉檔案控制代碼。 如果資料庫檔案已關閉，則相關聯的資料庫修補檔 (（如果有任何) 損毀）。

失敗時，不會發生任何變更。

#### <a name="remarks"></a>備註

資料庫引擎目前僅支援透過 [JetOpenFileInstance](./jetopenfileinstance-function.md) 一次開啟一個開啟的檔案。 如果使用 [JetOpenFileInstance](./jetopenfileinstance-function.md) 來開啟檔案控制代碼，則必須先使用 **JetCloseFileInstance** 關閉，才能開啟另一個檔案。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopServiceInstance](./jetstopserviceinstance-function.md)
