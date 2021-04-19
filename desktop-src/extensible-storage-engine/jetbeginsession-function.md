---
description: 深入瞭解： JetBeginSession 函數
title: JetBeginSession 函式
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983883"
---
# <a name="jetbeginsession-function"></a>JetBeginSession 函式


_**適用于：** Windows |Windows Server_

## <a name="jetbeginsession-function"></a>JetBeginSession 函式

**JetBeginSession** 函式會啟動會話，並初始化並傳回 ESE 會話控制碼 ([JET_SESID](./jet-sesid.md)) 。 會話會控制資料庫的所有存取權，並且用來控制交易的範圍。 會話可以用來開始、認可或中止交易。 會話也會用來附加、建立或開啟資料庫。 此會話會當做所有 DDL 和 DML 作業的內容使用。 若要增加資料庫的平行存取和平行存取，可以開始多個會話。

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a>參數

*實例*

此呼叫所要使用的資料庫實例。

*psesid*

在成功傳回時，會話控制碼初始化之變數的指標。

*szUserName*

此參數已保留備用。

*szPassword*

此參數已保留備用。

### <a name="return-value"></a>傳回值

此函數可讓您傳回在此 API 中定義的任何 [JET_ERR](./jet-err.md)。 如需有關 Jet 錯誤的詳細資訊，請參閱 [可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>因為無法配置記憶體，所以操作失敗。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSessions</p></td>
<td><p>引擎可讓用戶端啟動的會話數目有限。 您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 JET_paramMaxSessions 常數來變更這個值。 會話的預設數目為16。 如需 JET_paramMaxSessions 的詳細資訊，請參閱 <a href="gg294139(v=exchg.10).md">系統參數</a> 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
</tbody>
</table>


成功時，會初始化會話控制碼，並可用於資料庫作業。

失敗時，沒有可用的會話，或無法初始化新的會話。

#### <a name="remarks"></a>備註

使用不同執行緒之間的會話時，必須小心使用。 會話會追蹤在 [JetBeginTransaction](./jetbegintransaction-function.md)、 [JetCommitTransaction](./jetcommittransaction-function.md)或 [JetRollback](./jetrollback-function.md)期間所使用的執行緒，如果在具有開啟交易的多個執行緒上使用，則會擲回錯誤。 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md)， [JetSetSessionCoNtext](./jetsetsessioncontext-function.md)可以變更此行為。 因為會話仍是序列化的內容，而且無法同時在單一會話上執行多個資料庫作業，所以只能以序列方式執行。 不過，您可以使用多個會話來達成並行資料庫存取。 您可以藉由設定和重設會話內容，在跨執行緒的交易內使用會話。

會話控制碼應該使用 [JetEndSession](./jetendsession-function.md)來關閉。

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
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
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
<td><p>實作為 <strong>JetBeginSessionW</strong> (Unicode) 和 <strong>JetBeginSessionA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetDupSession](./jetdupsession-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionCoNtext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionCoNtext](./jetsetsessioncontext-function.md)  
[JetStopService](./jetstopservice-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
