---
description: 深入瞭解： JET_DbInfo 列舉
title: JET_DbInfo 列舉
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c364b89ccb50542130c988a643fed594a34e370e5adb5e9d0a13f77eab5b04d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112227"
---
# <a name="jet_dbinfo-enumeration"></a>JET_DbInfo 列舉

用於抓取資料庫資訊的資訊層級。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a>成員

<table>
<thead>
<tr class="header">
<th></th>
<th>成員名稱</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>檔案名稱</td>
<td>傳回資料庫檔案的路徑， (字串) 。</td>
</tr>
<tr class="even">
<td></td>
<td>LCID</td>
<td>傳回與這個資料庫相關聯的地區設定識別碼 (LCID)  (Int32) 。</td>
</tr>
<tr class="odd">
<td></td>
<td>選項</td>
<td>傳回 <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>。 這會指出資料庫是否在獨佔模式中開啟。 如果資料庫處於獨佔模式，則會傳回 <a href="hh579532(v=exchg.10).md">獨佔</a> ，否則會傳回零。 不會傳回 JetAttachDatabase 和 JetOpenDatabase 的其他資料庫 grbit 選項。</td>
</tr>
<tr class="even">
<td></td>
<td>交易</td>
<td>傳回一個大於最大層級的數位，可將交易進行嵌套。 如果以嵌套方式 (呼叫 <a href="dn292105(v=exchg.10).md">JetBeginTransaction (JET_SESID) </a> ，也就是在相同的會話上，如果沒有認可或復原) 與此值多次相同，則會傳回 (Int32) 的最後一個呼叫 <a href="hh564840(v=exchg.10).md">TransTooDeep</a> 。</td>
</tr>
<tr class="odd">
<td></td>
<td>版本</td>
<td>傳回資料庫引擎的主要版本 (Int32) 。</td>
</tr>
<tr class="even">
<td></td>
<td>Filesize</td>
<td>傳回資料庫的 filesize，以 pages (Int32) 。</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceOwned</td>
<td>傳回資料庫的擁有空間，以 pages (Int32) 。</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAvailable</td>
<td>傳回資料庫中的可用空間，以 pages (Int32) 。</td>
</tr>
<tr class="odd">
<td></td>
<td>其他</td>
<td>傳回 <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> 物件。</td>
</tr>
<tr class="even">
<td></td>
<td>DBInUse</td>
<td>傳回布林值，指出資料庫是否附加 (布林值) 。</td>
</tr>
<tr class="odd">
<td></td>
<td>PageSize</td>
<td>傳回資料庫 (Int32) 的頁面大小。</td>
</tr>
<tr class="even">
<td></td>
<td>FileType</td>
<td>傳回資料庫 (<a href="hh566739(v=exchg.10).md">JET_filetype</a>) 的型別。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
