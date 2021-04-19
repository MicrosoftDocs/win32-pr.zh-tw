---
description: 深入瞭解： JetStopServiceInstance 函數
title: JetStopServiceInstance 函式
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b2e3307f13a63d00cbbaf33f491750bbfcdb9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986315"
---
# <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance 函式


_**適用于：** Windows |Windows Server_

## <a name="jetstopserviceinstance-function"></a>JetStopServiceInstance 函式

**JetStopServiceInstance** 函式會準備實例以進行終止。

**Windows xp：**  **JetStopServiceInstance** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>參數

*實例*

要用於 API 呼叫的正在執行實例。

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


如果此函式成功，它會準備未來終止。 針對終止進行準備所採取的步驟如下：

  - 如果正在執行，請停止線上磁碟重組。

  - 啟動版本存放區清除。

  - 藉由開始排清緩衝區管理員中的中途分頁，以降低檢查點深度。

  - 避免未來對該實例的大部分函式進行呼叫。

如果此函式失敗，則不會執行準備實例終止的任何步驟，因此不會對實例狀態進行任何變更。

#### <a name="remarks"></a>備註

此函式會減少實例終止時必須執行的工作，但不會終止實例。 如此一來，此函式只是優化，而且不一定要使用。 請注意，在 Windows 2000 和 Windows XP 中進行準備所需的工作量較小。 一旦函式成功，呼叫不再允許的函式將會傳回 JET_errClientRequestToStopJetService。 此呼叫之後仍允許的函式為： [JetRollback](./jetrollback-function.md)、 [JetCloseTable](./jetclosetable-function.md)、 [JetEndSession](./jetendsession-function.md)、 [JetCloseDatabase](./jetclosedatabase-function.md)、 [JetDetachDatabase](./jetdetachdatabase-function.md) 和 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md)。

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
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionCoNtext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
