---
description: 深入瞭解： JET_ENUMCOLUMN 結構
title: JET_ENUMCOLUMN 結構
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112108"
---
# <a name="jet_enumcolumn-structure"></a>JET_ENUMCOLUMN 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_enumcolumn-structure"></a>JET_ENUMCOLUMN 結構

使用 [JetEnumerateColumns](./jetenumeratecolumns-function.md)函數時， **JET_ENUMCOLUMN** 結構會列舉記錄的資料行值。 [JetEnumerateColumns](./jetenumeratecolumns-function.md) 會傳回 **JET_ENUMCOLUMN** 結構的陣列。 陣列會在記憶體中傳回，此記憶體是使用提供給該 API 的 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼來配置。

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a>成員

**columnid**

列舉的資料行識別碼。

**犯 錯**

由資料行列舉所產生的資料行狀態碼。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>錯誤碼</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>資料行識別碼超出資料行識別碼的合法限制。</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>資料行識別碼所描述的資料行不存在於資料表中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>此資料行的所有值都是 Null。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnPresent</p></td>
<td><p>指定了 JET_bitEnumeratePresenceOnly，而且此資料行至少有一個非 Null 的資料行值會傳回。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>已指定 JET_bitEnumerateCompressOutput，且已為此資料行傳回剛好一個非 Null 的資料行值。 如此一來，就會傳回壓縮格式的 <strong>JET_ENUMCOLUMN</strong> 。 如需詳細資訊，請參閱 <strong>JET_ENUMCOLUMN</strong> 。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>對應至此<strong>JET_ENUMCOLUMN</strong>結構的<a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a>結構中的資料行識別碼為零。</p></td>
</tr>
</tbody>
</table>


**cEnumColumnValue**

針對資料行列舉的資料行值陣列。 輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。

當資料行狀態碼不等於 JET_wrnColumnSingleValue 時，會使用這個輸出緩衝區。 如需詳細資訊，請參閱 [JetEnumerateColumns](./jetenumeratecolumns-function.md)。

如果 "err = JET_wrnColumnSingleValue"，則會傳回 \! 。

**rgEnumColumnValue**

針對資料行列舉的資料行值陣列。 輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。

當資料行狀態碼不等於 JET_wrnColumnSingleValue 時，會使用這個輸出緩衝區。 如需詳細資訊，請參閱 [JetEnumerateColumns](./jetenumeratecolumns-function.md)。

如果 "err = JET_wrnColumnSingleValue"，則會傳回 \! 。

**cbData**

為數據行列舉的資料行值。

輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。

只有在 JET_wrnColumnSingleValue 資料行狀態碼時，才會使用此輸出緩衝區。 如需詳細資訊，請參閱 [JetEnumerateColumns](./jetenumeratecolumns-function.md)。

如果 "err = = JET_wrnColumnSingleValue"，則會傳回。

**pvData**

為數據行列舉的資料行值。

輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。

只有在 JET_wrnColumnSingleValue 資料行狀態碼時，才會使用此輸出緩衝區。 如需詳細資訊，請參閱 [JetEnumerateColumns](./jetenumeratecolumns-function.md)。

如果 "err = = JET_wrnColumnSingleValue"，則會傳回。

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
