---
description: 深入瞭解： JetGetInstanceInfo 函數
title: JetGetInstanceInfo 函式
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850708"
---
# <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo 函式


_**適用于：** Windows |Windows Server_

## <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo 函式

**JetGetInstanceInfo** 函數會抓取正在執行之實例的相關資訊。

**Windows xp： JetGetInstanceInfo** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>參數

*pcInstanceInfo*

緩衝區的指標，此緩衝區會接收儲存在 *paInstanceInfo* 中的元素數目。

*paInstanceInfo*

緩衝區的指標，此緩衝區會接收結構陣列第一個元素的位址。

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
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 <strong>JetGetInstanceInfo</strong>會在下列情況傳回此錯誤：</p>
<ul>
<li><p><em>pcInstanceInfo</em> 或 <em>paInstanceInfo</em> 為 Null。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>記憶體不足，無法處理要求。</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>備註

資料庫引擎會配置 [JET_INSTANCE_INFO](./jet-instance-info-structure.md) 結構的陣列。 呼叫端負責使用 [JetFreeBuffer](./jetfreebuffer-function.md)釋出此記憶體。

如果沒有使用中的實例， **JetGetInstanceInfo** 會傳回 JET_errSuccess，而 *pcInstanceInfo* 會收到值為0的值。

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
<td><p>實作為 <strong>JetGetInstanceInfoW</strong> (Unicode) 和 <strong>JetGetInstanceInfoA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
