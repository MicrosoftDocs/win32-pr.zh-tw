---
description: 深入瞭解： ObjectInfoFlags 列舉
title: ObjectInfoFlags 列舉
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06cd7cecaa536106f70cc469e3b690a46bee8301fe2d1142bc3fa1ff2c045346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780268"
---
# <a name="objectinfoflags-enumeration"></a>ObjectInfoFlags 列舉

 (資料表) 之 ESENT 物件的旗標。 用於 [JET_OBJECTINFO](./jet-objectinfo-class.md)。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
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
<td>無</td>
<td>預設選項。</td>
</tr>
<tr class="even">
<td></td>
<td>系統</td>
<td>物件僅供內部使用。</td>
</tr>
<tr class="odd">
<td></td>
<td>TableFixedDDL</td>
<td>資料表的 DDL 是固定的。</td>
</tr>
<tr class="even">
<td></td>
<td>TableTemplate</td>
<td>資料表的 DDL 是可繼承的。</td>
</tr>
<tr class="odd">
<td></td>
<td>TableDerived</td>
<td>資料表的 DDL 繼承自範本資料表。</td>
</tr>
<tr class="even">
<td></td>
<td>TableNoFixedVarColumnsInDerivedTables</td>
<td>固定或 (衍生資料表中的資料行，讓固定或變數資料行可以在未來的) 中加入至範本。 與 TableTemplate 搭配使用。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
