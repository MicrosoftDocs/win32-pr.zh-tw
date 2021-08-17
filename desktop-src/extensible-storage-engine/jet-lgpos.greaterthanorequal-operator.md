---
description: 深入瞭解： JET_LGPOS。GreaterThanOrEqual 運算子
title: JET_LGPOS。GreaterThanOrEqual 運算子
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510730
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef9f6835d4c65d08eeb6b3765bd5f2319048986daac439b7b2059b02ecf9735a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109265"
---
# <a name="jet_lgposgreaterthanorequal-operator"></a>JET_LGPOS。GreaterThanOrEqual 運算子

判斷一個記錄檔位置是否位於或等於另一個記錄位置。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a>參數

  - lhs  
    類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    要比較的第一個記錄檔位置。

<!-- end list -->

  - rhs  
    類型： [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  
    
    要比較的第二個記錄檔位置。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果 lhs 在或等於 rhs，則為 True。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_LGPOS 結構](./jet-lgpos-structure2.md)

[JET_LGPOS 成員](./jet-lgpos-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
