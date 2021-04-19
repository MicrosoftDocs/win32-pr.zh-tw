---
description: 深入瞭解： JET_IdxInfo 列舉
title: JET_IdxInfo 列舉
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f2cb50537ed492a428c82fd9a6f6541c5fad2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988423"
---
# <a name="jet_idxinfo-enumeration"></a>JET_IdxInfo 列舉

使用 JetGetIndexInfo 取得索引資訊的資訊層級。 和 JetGetTableIndexInfo。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
```

## <a name="members"></a>成員

<table>
<thead>
<tr class="header">
<th></th>
<th>成員名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>預設</td>
<td>傳回包含索引相關資訊的 <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> 結構。</td>
</tr>
<tr class="even">
<td></td>
<td>List</td>
<td>傳回包含索引相關資訊的 <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> 結構。</td>
</tr>
<tr class="odd">
<td></td>
<td>SysTabCursor</td>
<td><strong>已淘汰。</strong> SysTabCursor 已淘汰。</td>
</tr>
<tr class="even">
<td></td>
<td>OLC</td>
<td><strong>已淘汰。</strong> OLC 已淘汰。</td>
</tr>
<tr class="odd">
<td></td>
<td>ResetOLC</td>
<td><strong>已淘汰。</strong> 重設 OLC 已淘汰。</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAlloc</td>
<td>傳回具有索引空間使用量的整數。</td>
</tr>
<tr class="odd">
<td></td>
<td>LCID</td>
<td>傳回具有索引 LCID 的整數。</td>
</tr>
<tr class="even">
<td></td>
<td>Langid</td>
<td><strong>已淘汰。</strong> Langid 已淘汰。 請改用 LCID。</td>
</tr>
<tr class="odd">
<td></td>
<td>Count</td>
<td>傳回包含資料表中索引計數的整數。</td>
</tr>
<tr class="even">
<td></td>
<td>VarSegMac</td>
<td>傳回具有以 cbVarSegMac 建立索引之值的 ushort。</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexId</td>
<td>傳回識別索引的 <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> 。</td>
</tr>
<tr class="even">
<td></td>
<td>KeyMost</td>
<td>在 Windows Vista 中引進。 傳回具有以 cbKeyMost 建立索引之值的 ushort。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
