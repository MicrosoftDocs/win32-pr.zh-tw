---
description: 深入瞭解： JetTerm 函數
title: JetTerm 函式
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a22e9f21ab1c3d296a770c53bc6ad5847264b703
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988411"
---
# <a name="jetterm-function"></a>JetTerm 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetterm-function"></a>JetTerm 函式

**JetTerm** 函式會起始由 [JetInit](./jetinit-function.md)初始化之實例的關機。

**JetTerm** 也可用來終結 [JetCreateInstance](./jetcreateinstance-function.md)所建立的未初始化實例。

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>參數

*實例*

指定要用於此呼叫的實例。

**Windows 2000：** 此參數會被忽略，且應一律為 **Null**。

**Windows XP 和更新版本：** 此參數已多載。 如果引擎在舊版模式下運作 (Windows 2000 相容性模式) 只支援一個實例，此參數可能是 **Null** 或包含 [JetInit](./jetinit-function.md)所傳回的實際實例。 如果引擎以多重實例模式運作，則此參數必須是使用 [JetCreateInstance](./jetcreateinstance-function.md)建立之實例的指標。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或數個參數的組合產生了非預期的結果。 當引擎處於多重實例模式時，以及<em>pinstance</em>參考不正確實例時， <strong>JetTerm</strong>會傳回這個錯誤。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為尚未初始化實例。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成操作，因為正在關閉實例。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為實例上的還原作業正在進行中。</p> | 
| <p>JET_errBackupInProgress</p> | <p>作業無法完成，因為實例上的備份作業正在進行中。</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>因為目前的會話具有指定實例的使用中交易，所以無法關閉實例。 只有使用 JET_bitTermComplete 時，才會發生此錯誤。</p> | 



如果此函數成功，將會關閉指定的實例。 實例控制碼也將會關閉，並且可供任何採用實例控制碼的 API 使用。 與實例相關聯的所有其他物件（例如會話）也會關閉。 檢查點檔案、交易記錄檔和附加至實例的資料庫檔案的狀態，會在關閉程式期間進行修改。

如果使用錯誤的結果導致此函式失敗，則實例會維持在初始化狀態，而且不會有任何變更。 否則，實例仍會依據成功案例關閉。 不同之處在于實例在下次初始化時，必須經歷損毀復原。 引擎會嘗試盡可能將最多的資料排清，以將所需的復原量降至最低。 就概念而言， **JetTerm** 失敗與進程損毀並無不同。

#### <a name="remarks"></a>備註

如果實例的主機進程基於任何原因而結束，則在該實例上成功呼叫 **JetTerm** 之前，系統會將實例視為處於損毀狀態。 當您下次嘗試初始化該實例時，將會發生損毀復原。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm2](./jetterm2-function.md)
