---
description: 深入瞭解： JET_OBJECTINFO 結構
title: JET_OBJECTINFO 結構
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
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
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027147"
---
# <a name="jet_objectinfo-structure"></a>JET_OBJECTINFO 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_objectinfo-structure"></a>JET_OBJECTINFO 結構

**JET_OBJECTINFO** 結構會保存物件的相關資訊。 資料表是目前唯一支援的物件類型。

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a>成員

**cbStruct**

**JET_OBJECTINFO** 結構的大小（以位元組為單位）。

**objtyp**

保存結構的 [JET_OBJTYP](./jet-objtyp.md) 。 目前只有資料表會傳回 (也就是 JET_objtypTable) 。

**dtCreate**

已過時。 請勿使用。

**dtUpdate**

已過時。 請勿使用。

**grbit**

位群組，其中包含可用於此呼叫的選項，包括下列零或多個。

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
<td><p>JET_bitTableInfoBookmark</p></td>
<td><p>資料表可以有書簽。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableInfoRollback</p></td>
<td><p>資料表可以復原。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableInfoUpdatable</p></td>
<td><p>您可以更新資料表。</p></td>
</tr>
</tbody>
</table>


**flags**

包含零或多個下列旗標的位欄位。

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
<td><p>JET_bitObjectSystem</p></td>
<td><p>資料表是系統資料表，僅供內部使用。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableDerived</p></td>
<td><p>資料表繼承自範本資料表的 DDL。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableFixedDDL</p></td>
<td><p>無法修改資料表的 DDL。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p></td>
<td><p>搭配 JET_bitObjectTableTemplate 使用，以不允許衍生資料表中的固定或變數資料行 (因此，在未來的) 中，可以將固定或變數資料行新增至範本。</p>
<p><strong>WINDOWS XP：  </strong>此值是在 Windows XP 中引進。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableTemplate</p></td>
<td><p>資料表是範本資料表。</p></td>
</tr>
</tbody>
</table>


**cRecord**

資料表中的記錄數目。

只有當 **JET_OBJECTINFO** 已傳遞至 [JetGetObjectInfo](./jetgetobjectinfo-function.md)時，才會抓取此值。

**cPage**

資料表正在使用的頁面數目。

只有當 **JET_OBJECTINFO** 已傳遞至 [JetGetObjectInfo](./jetgetobjectinfo-function.md)時，才會抓取此值。

### <a name="remarks"></a>備註

[JetGetObjectInfo](./jetgetobjectinfo-function.md)或 [JetGetTableInfo](./jetgettableinfo-function.md)的呼叫會填入 **JET_OBJECTINFO** 結構。 如果 API 呼叫不成功，則結構的內容是未定義的。

如果適用的話，資料表統計資料會包含記錄的數目以及叢集索引中的頁面數目 (也就是包含記錄資料) 的索引。 索引統計資料是使用 [JetGetIndexInfo](./jetgetindexinfo-function.md) 或 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)，依名稱個別存取。

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
