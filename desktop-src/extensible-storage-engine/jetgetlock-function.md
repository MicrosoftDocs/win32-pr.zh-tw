---
description: 深入瞭解： JetGetLock 函數
title: JetGetLock 函式
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfb055c0a11d701e3eabbc4049d85e4e4b77468d97e14fd4506bf04600182f0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979038"
---
# <a name="jetgetlock-function"></a>JetGetLock 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetlock-function"></a>JetGetLock 函式

**JetGetLock** 函式會提供一種方法來明確保留更新資料列、寫入鎖定的能力，或是明確防止任何其他會話、讀取鎖定更新資料列。 一般來說，資料列寫入鎖定是以隱含方式取得，因為更新資料列的結果。 由於記錄版本控制，通常不需要讀取鎖定。 不過，在某些情況下，交易可能會想要明確地鎖定資料列以強制執行序列化，或確保後續的作業會成功，因為已採取必要的鎖定。

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>參數

*sesid*

此呼叫將使用的會話。

*tableid*

將用於此呼叫的資料指標。

*grbit*

位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitReadLock</p></td>
<td><p>此旗標會在目前的記錄上取得讀取鎖定。 讀取鎖定與其他會話已保留的寫入鎖定不相容，但與其他會話所持有的讀取鎖定相容。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWriteLock</p></td>
<td><p>此旗標會在目前的記錄上取得寫入鎖定。 寫入鎖定與其他會話所持有的寫入或讀取鎖定不相容，但與相同會話所持有的讀取鎖定相容。</p></td>
</tr>
</tbody>
</table>


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
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>指定的 <em>grbit</em> 不是 JET_bitReadLock 或 JET_bitWriteLock。 它必須是這兩個旗標的其中一個。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>資料指標必須在記錄上，才能取得鎖定。 鎖定一律為 on 記錄。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p>鎖定只能由交易中的會話取得。</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>資料指標不可以是唯讀的，而是取得寫入鎖定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>會話必須有寫入權限，才能取得寫入鎖定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>要求衝突鎖定時傳回的錯誤。</p></td>
</tr>
</tbody>
</table>


成功時，會話已取得要求的鎖定。

失敗時，會話尚未取得要求的鎖定。

#### <a name="remarks"></a>備註

無法使用具有唯讀許可權的會話或資料指標取得寫入鎖定，即使會話和資料指標最終不會執行更新作業。 會話和資料指標都必須有寫入權限，才能取得寫入鎖定。

讀取和寫入鎖定是一種封閉式鎖定的方式。 封閉式鎖定預期會有多個並行會話衝突並事先取得鎖定，以確保其作業成功。

大部分的作業都可透過隱含採用鎖定的方式進行序列化。 不過，某些作業將不會。 為了說明這一點，請考慮兩個交易：

T1： R () 、U (B) 

T2： R (B) ，U (A) 

記錄層級版本控制會確保同時執行的每個交易都會看到 A 和 B 的原始值。在結果相依于讀取資料的情況下，不會執行任何序列順序來產生 A 和 B 的相同結果。 為了讓應用程式能夠序列化此交易，在讀取值時，應該會在每個交易中取得 A 和 B 的明確讀取鎖定。

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
