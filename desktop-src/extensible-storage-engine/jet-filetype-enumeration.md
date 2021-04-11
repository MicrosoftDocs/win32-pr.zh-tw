---
description: 深入瞭解： JET_filetype 列舉
title: JET_filetype 列舉
TOCTitle: JET_filetype enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_filetype
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_filetype(v=EXCHG.10)
ms:contentKeyID: 39516829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_filetype
- Microsoft.Isam.Esent.Interop.JET_filetype.Checkpoint
- Microsoft.Isam.Esent.Interop.JET_filetype.Database
- Microsoft.Isam.Esent.Interop.JET_filetype.Log
- Microsoft.Isam.Esent.Interop.JET_filetype.TempDatabase
- Microsoft.Isam.Esent.Interop.JET_filetype.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_filetype.Database
- Microsoft.Isam.Esent.Interop.JET_filetype
- Microsoft.Isam.Esent.Interop.JET_filetype.Unknown
- Microsoft.Isam.Esent.Interop.JET_filetype.Log
- Microsoft.Isam.Esent.Interop.JET_filetype.Checkpoint
- Microsoft.Isam.Esent.Interop.JET_filetype.TempDatabase
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e1f6b21d521babdf7b5c36411ea8bd19d5ebba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849550"
---
# <a name="jet_filetype-enumeration"></a>JET_filetype 列舉

Esent 檔案類型。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration JET_filetype
'Usage
Dim instance As JET_filetype
```

``` csharp
public enum JET_filetype
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
<td>Unknown</td>
<td>未知的檔案。</td>
</tr>
<tr class="even">
<td></td>
<td>資料庫</td>
<td>資料庫檔案。</td>
</tr>
<tr class="odd">
<td></td>
<td>記錄</td>
<td>交易記錄檔。</td>
</tr>
<tr class="even">
<td></td>
<td>Checkpoint</td>
<td>檢查點檔案。</td>
</tr>
<tr class="odd">
<td></td>
<td>TempDatabase</td>
<td>暫存資料庫。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
