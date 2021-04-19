---
description: 深入瞭解： JET_TblInfo 列舉
title: JET_TblInfo 列舉
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981605"
---
# <a name="jet_tblinfo-enumeration"></a>JET_TblInfo 列舉

使用 JetGetTableInfo 來抓取資料表資訊的資訊層級。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
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
<td>預設選項。 抓取 <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> ，其中包含資料表的相關資訊。 使用這個選項搭配 <a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、JET_OBJECTINFO JET_TblInfo) </a>。</td>
</tr>
<tr class="even">
<td></td>
<td>Name</td>
<td>抓取資料表的名稱。 使用這個選項搭配 <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、字串、JET_TblInfo) </a>。</td>
</tr>
<tr class="odd">
<td></td>
<td>Dbid</td>
<td>抓取包含資料表之資料庫的 <a href="hh596176(v=exchg.10).md">JET_DBID</a> 。 使用這個選項搭配 <a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、JET_DBID JET_TblInfo) </a>。</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceUsage</td>
<td>方法的行為取決於傳遞給方法的陣列大小。 陣列必須至少有兩個專案。 第一個專案會包含資料表中擁有的範圍數目。 第二個專案會包含資料表中可用範圍的數目。 如果陣列有兩個以上的專案，則緩衝區的剩餘位元組將由表示範圍清單的結構陣列所組成。 此結構包含兩個成員：範圍中的最後一個頁碼和範圍中的頁面數目。 使用這個選項搭配 <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、[]、JET_TblInfo) </a>。</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAlloc</td>
<td>傳遞至 JetGetTableInfo 的陣列必須有兩個專案。 第一個專案會設定為數據表中的頁面數目。 第二個專案將會設定為數據表之頁面的目標密度。 使用這個選項搭配 <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、[]、JET_TblInfo) </a>。</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceOwned</td>
<td>取得資料表中擁有的頁面數目。 使用這個選項搭配 <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、Int32、JET_TblInfo) </a>。</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceAvailable</td>
<td>取得資料表中可用的頁面數目。 使用這個選項搭配 <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、Int32、JET_TblInfo) </a>。</td>
</tr>
<tr class="even">
<td></td>
<td>TemplateTableName</td>
<td>如果資料表是衍生的資料表，則會以衍生資料表繼承其 DDL 的資料表名稱填入結果。 如果資料表不是衍生的資料表，則緩衝區將會是空字串。 使用這個選項搭配 <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID、JET_TABLEID、字串、JET_TblInfo) </a>。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
