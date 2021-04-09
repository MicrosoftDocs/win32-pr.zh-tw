---
description: 深入瞭解： JET_SETCOLUMN ibLongValue 屬性
title: JET_SETCOLUMN ibLongValue 屬性
TOCTitle: 'ibLongValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ibLongValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.iblongvalue(v=EXCHG.10)
ms:contentKeyID: 55103931
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ibLongValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.ibLongValue
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_ibLongValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d98f1b49f5e4815f2ffaeb5d796c6139ad582e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689932"
---
# <a name="jet_setcolumniblongvalue-property"></a>JET_SETCOLUMN ibLongValue 屬性

取得或設定要在 [LongBinary](./jet-coltyp-enumeration.md) 或 [LongText](./jet-coltyp-enumeration.md)類型的資料行中設定之第一個位元組的位移。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property ibLongValue As Integer
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Integer

value = instance.ibLongValue

instance.ibLongValue = value
```

``` csharp
public int ibLongValue { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SETCOLUMN 類別](./jet-setcolumn-class.md)

[JET_SETCOLUMN 成員](./jet-setcolumn-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
