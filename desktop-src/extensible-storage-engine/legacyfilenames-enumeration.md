---
description: 深入瞭解： LegacyFileNames 列舉
title: 'LegacyFileNames 列舉 (的列舉) '
TOCTitle: LegacyFileNames enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.legacyfilenames(v=EXCHG.10)
ms:contentKeyID: 55104275
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f3cade11450bcfbad13dcdd114dca6701c5369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943527"
---
# <a name="legacyfilenames-enumeration"></a>LegacyFileNames 列舉

LegacyFileNames 的選項

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration LegacyFileNames
'Usage
Dim instance As LegacyFileNames
```

``` csharp
public enum LegacyFileNames
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
<td>ESE98FileNames</td>
<td>當這個選項存在時，database engine 將會針對其檔案使用下列命名慣例： o 交易記錄檔將會使用。記錄檔，其副檔名為 o 的檢查點檔案將會使用。副檔名的 .CHK</td>
</tr>
<tr class="even">
<td></td>
<td>EightDotThreeSoftCompat</td>
<td>盡可能保留8.3 命名語法。  (不應變更，請確保沒有記錄檔) </td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
