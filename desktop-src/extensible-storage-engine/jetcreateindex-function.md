---
description: 深入瞭解： JetCreateIndex 函數
title: JetCreateIndex 函式
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988843"
---
# <a name="jetcreateindex-function"></a>JetCreateIndex 函式


_**適用于：** Windows |Windows Server_

## <a name="jetcreateindex-function"></a>JetCreateIndex 函式

**JetCreateIndex** 函式可讓您在可延伸的儲存引擎 (ESE) 資料庫中建立資料的索引，您可以用它來快速找出特定資料。

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a>參數

*sesid*

用於特定 API 呼叫的資料庫會話內容。

*tableid*

將為其建立索引的資料表。

*szIndexName*

以 null 結束的字串指標，指定要建立之索引的名稱。

索引名稱必須符合下列指導方針：

  - 它必須包含少於 JET_cbNameMost 的字元數，而不包含終止的 null 字元。

  - 它必須只包含下列類別的字元：0到9、A 到 Z、a 到 z，以及 "" 以外的所有標點符號字元 \!  (驚嘆號) 、"、" (逗號) 、" \[ " (左括弧) 和 " \] " (右括弧) ，也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。

  - 不得以空格開頭。

  - 它至少必須包含一個非空白字元。

*grbit*

位群組，其中包含要用於特定呼叫的選項。 這個參數可以包含在 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構中找到的零或多個選項。

*szKey*

Null 分隔標記的雙 null 結束字串指標。

如需此參數的詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構。

*cbKey*

*SzKey* 參數的長度（以位元組為單位），包括兩個終止的 null 字元。

*lDensity*

初始索引 B + 樹狀結構的百分比密度。

如需此參數的詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構。

### <a name="return-value"></a>傳回值

此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
</tbody>
</table>


如需 **JetCreateIndex** 函數可傳回的其他錯誤清單，請參閱 [JetCreateIndex2](./jetcreateindex2-function.md)。

#### <a name="remarks"></a>備註

呼叫 **JetCreateIndex** 函數等同于呼叫具有 [JET_INDEXCREATE](./jet-indexcreate-structure.md)結構的 [JetCreateIndex2](./jetcreateindex2-function.md)函式，其中包含與 **JetCreateIndex** 參數相同的設定，以及等於1的 *cIndexCreate* 參數。 如果 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構的欄位在 **JetCreateIndex** 中沒有對應的參數，則會假設為0值。

請注意， **JetCreateIndex** 已被 [JetCreateIndex2](./jetcreateindex2-function.md)取代。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>用戶端</p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p>伺服器</p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p>標頭</p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p>程式庫</p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>會實作為 <strong>JetCreateIndexW</strong> (Unicode) 和 <strong>JetCreateIndexA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
