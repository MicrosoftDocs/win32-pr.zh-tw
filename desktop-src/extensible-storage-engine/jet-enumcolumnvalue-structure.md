---
description: 深入瞭解： JET_ENUMCOLUMNVALUE 結構
title: JET_ENUMCOLUMNVALUE 結構
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980605"
---
# <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE 結構

**JET_ENUMCOLUMNVALUE** 結構會使用 [JetEnumerateColumns](./jetenumeratecolumns-function.md)函數來列舉記錄的資料行值。 [JetEnumerateColumns](./jetenumeratecolumns-function.md) 會傳回 **JET_ENUMCOLUMNVALUE** 結構的陣列。 陣列會在使用提供給該函式之 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼所配置的記憶體中傳回。

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>成員

**itagSequence**

以一為基礎的索引) 所 (的資料行值。

**犯 錯**

由資料行值列舉所產生的資料行狀態碼。

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
<td><p>JET_wrnColumnNull</p></td>
<td><p>要求的資料行值為 Null。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>在對應于此<strong>JET_ENUMCOLUMNVALUE</strong>結構的<a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a>結構中，于<em>rgtagSequence</em>陣列的元素中指定的<em>itagSequence</em>為零。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnTruncated</p></td>
<td><p>要求的資料行值在傳回之前已被截斷為指定的大小。</p>
<p>只有包含大量資料的長文字和長二進位資料行才會發生截斷。</p></td>
</tr>
</tbody>
</table>


**cbData**

為數據行列舉的資料行值。

輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。

**pvData**

為數據行列舉的資料行值。

輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。

### <a name="requirements"></a>規格需求

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
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
