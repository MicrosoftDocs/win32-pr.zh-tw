---
description: 深入瞭解： JetGetInstanceMiscInfo 函數
title: JetGetInstanceMiscInfo 函式
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ada8dfcd69a4e1933bcb60756d1b812f3b358cd37a3cda914819d2a9f6f4275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472348"
---
# <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo 函式

當實例在線上時， **JetGetInstanceMiscInfo** 函式會抓取實例的相關資訊。

**Windows vista： JetGetInstanceMiscInfo** 是 Windows vista 引進。

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>參數

*實例*

識別將用於 API 呼叫的資料庫實例。

*pvResult*

將接收資訊的緩衝區指標。 緩衝區的類型取決於 *InfoLevel*。 呼叫端會負責適當地對齊緩衝區。

*cbMax*

傳入 *pvResult* 的緩衝區大小（以位元組為單位）。

*InfoLevel*

判斷針對 *實例* 指定的實例，將會抓取何種類型的資訊。 *PvResult* 中儲存的資料格式取決於 *InfoLevel*。

下列選項可用於此參數。

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
<td><p>JET_InstanceMiscInfoLogSignature</p></td>
<td><p><em>pvResult</em> 會被視為與此實例相關聯之交易記錄順序的 <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> 結構。</p></td>
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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>緩衝區太小。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>不正確 <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> 或指定的 <em>InfoLevel</em> 無效。</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008。</p></td>
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
[JET_SIGNATURE](./jet-signature-structure.md)
