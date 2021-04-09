---
description: 深入瞭解： JetCommitTransaction 函數
title: JetCommitTransaction 函式
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945177"
---
# <a name="jetcommittransaction-function"></a>JetCommitTransaction 函式


_**適用于：** Windows |Windows Server_

## <a name="jetcommittransaction-function"></a>JetCommitTransaction 函式

**JetCommitTransaction** 函式會在目前的儲存點期間認可對資料庫狀態所做的變更，並將其遷移至先前的儲存點。 如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*grbit*

指定零或多個下列選項的位群組。

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
<td><p>JET_bitCommitLazyFlush</p></td>
<td><p>交易會正常認可，但此 API 不會等到交易被排清到交易記錄檔，然後再傳回給呼叫者。 這可大幅減少認可作業的持續時間，代價是持久性。 在下次呼叫 <a href="gg294068(v=exchg.10).md">JetInit</a>期間，任何未在損毀之前排清到記錄檔的交易都會自動中止。</p>
<p>如果指定 JET_bitWaitLastLevel0Commit 或 JET_bitWaitAllLevel0Commit，則會忽略此選項。</p>
<p>如果這個 <strong>JetCommitTransaction</strong> 呼叫與此會話的第一次呼叫 <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> 不相符，則會忽略此選項。 這是因為在最外層儲存點上發生的最後一個動作，就是整個交易實際上是否認可到磁片的決定因素。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWaitAllLevel0Commit</p></td>
<td><p>所有先前由尚未排清至交易記錄檔的會話所認可的交易，都會立即進行清除。 此 API 會等到交易已排清之後，再返回呼叫端。</p>
<p>即使會話目前不在交易中，也可以使用此選項。</p>
<p>此選項不能與任何其他選項搭配使用。</p>
<p>此選項僅適用于 Windows Server 2003。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitWaitLastLevel0Commit</p></td>
<td><p>如果會話先前已認可任何交易，而且它們尚未排清到交易記錄檔，則應該立即排清它們。 此 API 會等到交易已排清之後，再返回呼叫端。 如果應用程式先前已使用 JET_bitCommitLazyFlush 認可數筆交易，而現在想要將所有交易排清到磁片上，這項功能就很有用。</p>
<p>即使會話目前不在交易中，也可以使用此選項。</p>
<p>此選項不能與任何其他選項搭配使用。</p></td>
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
<td><p>JET_errInvalidgrbit</p></td>
<td><p>其中一個要求的選項無效或未執行。 <strong>JetCommitTransaction</strong>會在下列情況傳回此錯誤：</p>
<ul>
<li><p>指定了不合法的 <em>grbit</em> 。</p></li>
<li><p>JET_bitWaitLastLevel0Commit 已與另一個 <em>grbit</em>一起指定。</p></li>
<li><p>JET_bitWaitAllLevel0Commit 已與另一個 <em>grbit</em>一起指定。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>作業失敗，因為指定的會話不在交易中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。</p>
<p>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
</tbody>
</table>


成功時，將會認可指定會話目前儲存點期間對資料庫所做的任何變更，而且儲存點將會結束。 如果會話的最後一個儲存點已結束，則交易會選擇性地排清至交易記錄檔，而且會話將會結束交易。

失敗時，會話的交易式狀態將保持不變。 不會變更資料庫狀態。 應用程式應該呼叫 [JetRollback](./jetrollback-function.md) 來中止交易。

#### <a name="remarks"></a>備註

必須呼叫 **JetCommitTransaction** 或 [JetRollback](./jetrollback-function.md) ，以比對指定會話的每個 [JetBeginTransaction](./jetbegintransaction-function.md) 呼叫。

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
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction]()  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)
