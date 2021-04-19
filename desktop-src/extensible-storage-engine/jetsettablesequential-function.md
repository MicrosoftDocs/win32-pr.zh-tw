---
description: 深入瞭解： JetSetTableSequential 函數
title: JetSetTableSequential 函式
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966689"
---
# <a name="jetsettablesequential-function"></a>JetSetTableSequential 函式


_**適用于：** Windows |Windows Server_

## <a name="jetsettablesequential-function"></a>JetSetTableSequential 函式

**JetSetTableSequential** 函式會通知資料庫引擎應用程式正在掃描包含指定資料指標的整個目前索引。 因此，用來存取索引資料的方法將會進行微調，使此案例的速度越快越好。

**Windows xp：**  **JetSetTableSequential** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

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
<td><p>JET_bitPrereadForward</p></td>
<td><p>此選項是用來以正向方向編制索引。</p>
<p><strong>Windows 7：</strong>  <strong>JET_bitPrereadForward</strong> 是在 windows 7 中引進的。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitPrereadBackward</p></td>
<td><p>此選項可用來在反向方向編制索引。</p>
<p><strong>Windows 7：</strong>  <strong>JET_bitPrereadBackward</strong> 是在 windows 7 中引進的。</p></td>
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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>作業無法完成，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>時，與會話相關聯之實例上的所有活動都已停止。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p></td>
</tr>
</tbody>
</table>


如果此函式成功，則資料指標的目前索引會針對整個索引的連續掃描進行優化。 不會變更資料庫狀態。

如果此函式失敗，將不會變更資料指標的設定。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

如果應用程式需要有效率地掃描索引的已知子集，則在使用 [JetSetIndexRange](./jetsetindexrange-function.md)建立索引範圍時也會執行類似的優化。 這項優化只適用于 Windows XP 和更新版本。

如果應用程式需要有效率地掃描索引的未知子集，則不應採取任何動作。 引擎可以自動偵測掃描行為，而且會事先提取資料。 不過，這種行為並不是積極的。

這項優化可讓您有效率地掃描主要索引，並讓您只在次要索引中以有效率的方式掃描索引項目目資料。 它不會在您有效率地抓取記錄資料時，掃描次要索引。 這是因為引擎不會在記錄資料上執行預先讀取。

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
