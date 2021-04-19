---
description: 深入瞭解： JetCreateInstance 函數
title: JetCreateInstance 函式
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989052"
---
# <a name="jetcreateinstance-function"></a>JetCreateInstance 函式


_**適用于：** Windows |Windows Server_

## <a name="jetcreateinstance-function"></a>JetCreateInstance 函式

**JetCreateInstance** 函式會配置新的 database engine 實例，以便在單一進程中使用。

**Windows xp： JetCreateInstance** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>參數

*pinstance*

接收新建立之實例的輸出緩衝區。

*szInstanceName*

要建立之實例的唯一字串識別碼。 這個字串在主控資料庫引擎的指定進程內必須是唯一的。

**注意** Null 值會被視為實例的有效字串識別碼。 只有一個實例可以有 Null 字串識別碼。

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
<td><p>JET_errInstanceNameInUse</p></td>
<td><p>指定的實例名稱已用於此進程。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 當<em>pinstance</em>為<strong>Null</strong>時， <strong>JetCreateInstance</strong>可能會發生這種情況。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>作業失敗，因為當 database engine 在單一實例模式中運作時，無法使用此作業 (Windows 2000 相容性模式) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances</p></td>
<td><p>因為已達到實例的數目上限，所以無法建立新的實例。 支援的實例數目上限是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> （使用 <em>JET_paramMaxInstances</em>）來設定。</p></td>
</tr>
</tbody>
</table>


成功時，將會配置新的實例，並傳回它的識別碼。 此時，實例的所有系統參數都會有全域預設系統參數的值。 一旦配置實例之後，就必須稍後再將其終止及/或釋放。

失敗時，將會傳回代表失敗原因的錯誤，且不會配置任何實例。

#### <a name="remarks"></a>備註

必須先使用 [JetInit](./jetinit-function.md) 的呼叫來初始化實例，才能由 [JetSetSystemParameter](./jetsetsystemparameter-function.md)以外的任何人使用。

實例會透過呼叫 [JetTerm](./jetterm-function.md) 函式終結，即使該實例從未使用 [JetInit](./jetinit-function.md)初始化也是一樣。 可以在任何時間建立的實例數目上限是由 [JET_paramMaxInstances](./resource-parameters.md)所控制，可以透過呼叫 [JetSetSystemParameter](./jetsetsystemparameter-function.md)來設定。 實例是 database engine 的復原單位。 它會控制所有檔案的生命週期，用來保護一組資料庫檔案中資料的完整性。 這些檔案包括檢查點檔案和交易記錄檔。

如果函式成功，資料庫引擎將會自動變更為多重實例模式，做為此呼叫的副作用。 如果應用程式想要在進程中只允許一個實例，則應該使用 [JetInit](./jetinit-function.md) 來啟動 Windows 2000 相容性模式中的 database engine。

如果有的話， *szDisplayName* 會用來識別事件記錄檔中的實例，或與其他呼叫端（例如，透過 [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) 或 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)) 等函式的備份應用 (程式）。 如果未提供顯示名稱，則會改用唯一的 *szInstanceName* （如果有的話），否則會傳回空字串。 如果引擎沒有設定執行中的模式，則在呼叫之後，它會設定為多重實例模式。

可能執行多個 Jet 實例之進程的一般啟動順序為：

  - 呼叫 [JetCreateInstance2](./jetcreateinstance2-function.md) ，它會配置並命名實例。

  - 針對該實例的多個 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 呼叫，以便設定不同的系統參數。 請注意，某些系統參數在每個實例上都必須是唯一的 (例如 [JET_paramSystemPath](./transaction-log-parameters.md) 或 [JET_paramLogFilePath](./transaction-log-parameters.md)) 因此最有可能需要設定每一種。

  - 使用 [JetInit](./jetinit-function.md) 或 [JetInit2](./jetinit2-function.md)來啟動實例。 為了終止及/或釋放實例，必須使用 [JetTerm](./jetterm-function.md)、 [JetTerm2](./jetterm2-function.md) 。

如果這是第一個要啟動的實例，則在此呼叫期間會執行一些額外的步驟，以便進行基本系統初始化和設定。 其中一些步驟可能會導致從 JET_errOutOfMemory 開始的特定錯誤，但也 (看到上述錯誤) 。

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetCreateInstanceW</strong> (Unicode) 和 <strong>JetCreateInstanceA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[可擴充儲存引擎檔案](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
