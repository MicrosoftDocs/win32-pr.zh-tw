---
description: 深入瞭解： JET_InstanceMiscInfo 列舉
title: 'JET_InstanceMiscInfo 列舉 (的 < a0/&gt; < a1/&gt;) '
TOCTitle: JET_InstanceMiscInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_instancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 39516547
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo.LogSignature
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo.LogSignature
- Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f3e311eddaf2cf6bdb3a7e06ef2a3acd719696a47accd055725c44f9a2b25b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979998"
---
# <a name="jet_instancemiscinfo-enumeration"></a>JET_InstanceMiscInfo 列舉

[JetGetInstanceMiscInfo (JET_INSTANCE、JET_SIGNATURE JET_InstanceMiscInfo) ](./vistaapi.jetgetinstancemiscinfo-method.md)的資訊層級。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_InstanceMiscInfo
'Usage
Dim instance As JET_InstanceMiscInfo
```

``` csharp
[FlagsAttribute]
public enum JET_InstanceMiscInfo
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
<td>LogSignature</td>
<td>取得與此順序相關聯之交易記錄的簽章。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
