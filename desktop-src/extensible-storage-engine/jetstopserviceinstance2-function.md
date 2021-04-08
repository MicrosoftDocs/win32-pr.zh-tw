---
description: 深入瞭解： JetStopServiceInstance2 函數
title: JetStopServiceInstance2 函式
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690816"
---
# <a name="jetstopserviceinstance2-function"></a>JetStopServiceInstance2 函式


_**適用于：** Windows |Windows Server_

**JetStopServiceInstance2** 函式會在暫停之前準備實例，並在繼續之後準備實例。 暫止和繼續是 Windows Store 應用程式生命週期模型的執行狀態。

**JetStopServiceInstance2** 函式是在 Windows 8 引進。

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>參數

*實例*

目標實例。 **JET_INSTANCE** 資料類型是要用於呼叫 JET API 之資料庫實例的控制碼。 當您藉由呼叫 [JetCreateInstance](./jetcreateinstance-function.md)、 [JetCreateInstance2](./jetcreateinstance2-function.md)、 [JetInit](./jetinit-function.md)或 [JetInit2](./jetinit2-function.md) 函式來建立資料庫的實例時，就會取得此控制碼。

*grbit*

位群組，指定下表中列出和定義的一或多個值。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>描述</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitStopServiceAll</p></td>
<td><p>針對指定的實例停止所有可延伸的儲存引擎 (ESE) 服務。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceBackgroundUserTasks</p></td>
<td><p>停止可重新開機的用戶端指定的背景維護工作 (B + 樹狀重組，例如) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitStopServiceQuiesceCaches</p></td>
<td><p>將所有中途快取 Quiesces 至磁片。 這個值是非同步，而且可以取消。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceResume</p></td>
<td><p>繼續先前發行的 StopService 作業;也就是說，它會重新開機服務。 這個值可以與 <em>grbits</em> 參數結合以繼續特定服務，或使用 JET_bitStopServiceAll 繼續所有先前停止的服務。 此位只能用來繼續 StopServiceBackgroundUserTasks 和 JET_bitStopServiceQuiesceCaches。 如果您先前已使用 JET_bitStopServiceAll 呼叫，則嘗試使用 JET_bitStopServiceResume 將會失敗。 如果未呼叫第二個恢復步驟，應用程式將會降低效能。 在這種情況下，檢查點會保持為零。</p></td>
</tr>
</tbody>
</table>


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
</tbody>
</table>


#### <a name="remarks"></a>備註

這項功能可讓 JET 應用程式將資料庫快取移到乾淨或近乎乾淨的狀態 (使用作業系統 i/o 閒置) ，如此一來，如果要終止應用程式，復原就會很快速。 這種方法優於透過呼叫 [JetTerm](./jetterm-function.md) 或 [JetDetachDatabase](./jetdetachdatabase-function.md) 函式來終止 JET，因此在較常見的案例中，應用程式只是 unsuspended，稍後應用程式會有完整的快取，而且已準備好繼續進行。

如果此函式成功，它會準備資料庫快取以供即將暫停。 此函式會將工作排入背景工作者執行緒，並立即返回呼叫端。 應該根據 PLM VisibilityNotice 來呼叫函式，而不是從應用程式的暫止事件處理常式呼叫，以確保 JET 有時間在 PLM 暫停或終止進程之前排清中途緩衝區。 就內部而言，JET 會在設定變更時立即觸發檢查點維護 (檢查點更新或這個新的靜止快取位) 。 如需 VisibilityNotice 事件的詳細資訊，請參閱 [VisibilityChangedEventArgs 類別](/uwp/api/windows.ui.core.visibilitychangedeventargs)。

您必須呼叫此函式兩次。 它會在應用程式從作業系統收到暫停通知之後，但在應用程式暫停之前呼叫。 然後在作業系統繼續應用程式之後，再次呼叫它。 例如：

當呼叫以暫停： JET_ERR JET_API JetStopServiceInstance2 ( 實例，JET_bitStopServiceQuiesceCaches) ;

繼續時： JET_ERR JET_API JetStopServiceInstance2 ( 實例，JET_bitStopServiceQuiesceCaches |JET_bitStopServiceResume ) ;

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows 8。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2012。</p></td>
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
