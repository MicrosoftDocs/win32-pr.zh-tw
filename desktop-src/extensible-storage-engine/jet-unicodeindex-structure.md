---
description: 深入瞭解： JET_UNICODEINDEX 結構
title: JET_UNICODEINDEX 結構
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104386534"
---
# <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX 結構

**JET_UNICODEINDEX** 結構自訂在 unicode 資料行上建立索引時，如何將 Unicode 資料正規化。

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a>成員

**lcid**

正規化資料時要使用的地區設定識別碼。 只要電腦上已安裝適當的語言套件，即可使用任何地區設定。 其中一個例外狀況是，非語言相關地區設定 (LCID 為零) 不合法。

**dwMapFlags**

當 Unicode 資料正規化至索引鍵時，這些旗標會傳遞至 [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) ，如此可讓使用者定義旗標覆寫預設值。

**Windows 2000**： **dwFlags** 的唯一兩個合法值為：

  -  ( LCMAP_SORTKEY |NORM_IGNORECASE |NORM_IGNOREKANATYPE |NORM_IGNOREWIDTH |NORM_IGNORENONSPACE ) 

<!-- end list -->

  -  ( LCMAP_SORTKEY |NORM_IGNORECASE |NORM_IGNOREKANATYPE |NORM_IGNOREWIDTH ) 

**dwMapFlags** 具有下列限制。

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
<td><p>LCMAP_SORTKEY</p></td>
<td><p>Mandatory。</p></td>
</tr>
<tr class="even">
<td><p>LCMAP_BYTEREV</p></td>
<td><p>選擇性。</p></td>
</tr>
<tr class="odd">
<td><p>NORM_IGNORECASE</p></td>
<td><p>選擇性。</p></td>
</tr>
<tr class="even">
<td><p>NORM_IGNORENONSPACE</p></td>
<td><p>選擇性。</p></td>
</tr>
<tr class="odd">
<td><p>NORM_IGNORESYMBOLS</p></td>
<td><p>選擇性。</p></td>
</tr>
<tr class="even">
<td><p>NORM_IGNOREKANATYPE</p></td>
<td><p>選擇性。</p></td>
</tr>
<tr class="odd">
<td><p>NORM_IGNOREWIDTH</p></td>
<td><p>選擇性。</p></td>
</tr>
<tr class="even">
<td><p>SORT_STRINGSORT</p></td>
<td><p>選擇性。</p></td>
</tr>
</tbody>
</table>


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

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)
