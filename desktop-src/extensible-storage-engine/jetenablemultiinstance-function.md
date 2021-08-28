---
description: 深入瞭解： JetEnableMultiInstance 函數
title: JetEnableMultiInstance 函式
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 618552b01a4702790fca0d234ee40aff0de39f45
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481364"
---
# <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance 函式

**JetEnableMultiInstance** 函式會設定資料庫引擎，以便在相同的進程中搭配多個實例使用。 第一個呼叫端可以使用全域系統參數的選擇性陣列，以允許變更多重實例模式。

**Windows xp： JetEnableMultiInstance** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>參數

*psetsysparam*

全域系統參數的陣列，這些參數會在引擎因為此呼叫而進入多重實例模式時進行設定。 如果 *csetsysparam* 為零，則會忽略 *psetsysparam* 。

*csetsysparam*

要設定之全域參數陣列的元素計數（如果引擎因為此呼叫而進入多重實例模式，則為）。 如果 *csetsysparam* 為零，則會忽略 *psetsysparam* 。

*pcsetsucceed*

全域系統參數計數的指標，這些參數已成功設定為此呼叫的結果。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>不允許指定的元組索引參數。 只有將<a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>、 <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>或<a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a>設定為不合法的值時， <strong>JetEnableMultiInstance</strong>才會傳回此錯誤。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errInvalidPath</p> | <p>指定的檔案系統路徑無效。 只有在設定代表檔案系統路徑的系統參數時， <strong>JetEnableMultiInstance</strong> 才會傳回此錯誤。 例如， <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> 可能會傳回這個錯誤。</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>作業失敗，因為當 database engine 在單一實例模式中作業時，這是不合法的 (Windows 2000 相容性模式) 。</p> | 
| <p>JET_errSystemParamsAlreadySet</p> | <p><strong>JetEnableMultiInstance</strong> 失敗，因為引擎已處於多重實例模式。</p><p><strong>注意  </strong>即使未指定任何系統參數，也會發生這種情況。</p> | 



如果此函式成功，資料庫引擎將設定為在多重實例模式中執行。 引擎也已使用全域系統參數的選擇性清單成功設定。

如果此函式失敗，database engine 將維持在目前的模式。 如果 *pcsetsucceed* 不是零，則系統參數的數目將維持不變。

#### <a name="remarks"></a>備註

只有當應用程式在設定資料庫引擎以在相同進程的多重使用者案例中使用時，必須以不可部分完成的方式設定一組指定的系統參數時，才應該使用此函數。 如果有另一種同步處理方法，最好是分別呼叫 [JetCreateInstance](./jetcreateinstance-function.md) 和 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetEnableMultiInstanceW</strong> (Unicode) 和 <strong>JetEnableMultiInstanceA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
