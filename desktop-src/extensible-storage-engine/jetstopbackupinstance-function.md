---
description: 深入瞭解： JetStopBackupInstance 函數
title: JetStopBackupInstance 函式
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112516"
---
# <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance 函式


_**適用于：** Windows |Windows Server_

## <a name="jetstopbackupinstance-function"></a>JetStopBackupInstance 函式

**JetStopBackupInstance** 函式會防止串流備份相關的活動繼續執行特定執行中的實例，進而以可預測的方式結束串流備份。

**Windows xp：**  **JetStopBackupInstance** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>參數

*實例*

識別要用於 API 呼叫的正在執行的實例。

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>指定的實例參數有不正確值 (不是目前正在執行) 的實例。</p>
<p><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</p></td>
</tr>
</tbody>
</table>


如果此函式成功，則指定的實例將開始失敗任何新的串流備份 Api。

如果此函式失敗，就不會執行在實例上進行備份終止的任何步驟，也不會發生實例狀態的變更。

#### <a name="remarks"></a>備註

備份通常是由進程機制之外的事件所觸發，而使用此 API 時，ESENT 應用程式本身會對串流備份 Api 進行任何進一步的呼叫，以使其失敗。 大部分的串流備份 Api 都會隨著 JET_errBackupAbortByServer 開始失敗。 因此，任何串流備份進度 (例如 [JetReadFileInstance](./jetreadfileinstance-function.md)) 都會傳回錯誤。 備份終止 (的備份作業（例如 [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) ）仍會被允許。

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

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)  
[JetReadFileInstance](./jetreadfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)
