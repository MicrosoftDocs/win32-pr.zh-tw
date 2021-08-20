---
description: 深入瞭解： JetStopService 函數
title: JetStopService 函式
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4a8acc7d6213868387832a8db96e5abcdc0e24058043a089352a18be5cbe98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890952"
---
# <a name="jetstopservice-function"></a>JetStopService 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetstopservice-function"></a>JetStopService 函式

**JetStopService** 函式會準備實例以進行終止。

**JetStopService** 是僅允許一個實例時的舊版呼叫。 在此情況下，唯一的作用中實例是準備進行終止的實例。

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>參數

此函式沒有參數。

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
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>使用具有多個實例模式的 <strong>JetStopService</strong> 時，不會清除要準備終止的實例。</p>
<p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p></td>
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

此函式會減少實例終止時必須執行的工作，但不會終止實例。 如此一來，此函式只是優化，而且不一定要使用。 請注意，在 Windows 2000 和 Windows XP 中，進行準備所需的工作量較小。 一旦函式成功，呼叫不再允許的函式將會傳回 JET_errClientRequestToStopJetService。 此呼叫之後仍允許的函式為： [JetRollback](./jetrollback-function.md)、 [JetCloseTable](./jetclosetable-function.md)、 [JetEndSession](./jetendsession-function.md)、 [JetCloseDatabase](./jetclosedatabase-function.md)、 [JetDetachDatabase](./jetdetachdatabase-function.md) 和 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md)。

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
