---
description: 深入瞭解： JET_COLUMNID。LessThan 運算子
title: JET_COLUMNID。LessThan 運算子
TOCTitle: 'LessThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthan(v=EXCHG.10)
ms:contentKeyID: 39512911
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 263cb7be0377da007e6294b29701613628ec692d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973005"
---
# <a name="jet_columnidlessthan-operator"></a>JET_COLUMNID。LessThan 運算子

判斷其中一個 columnid 是否在另一個 columnid 之前。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Operator < ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs < rhs)
```

``` csharp
public static bool operator <(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a>參數

  - lhs  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    要比較的第一個 columnid。

<!-- end list -->

  - rhs  
    類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    要比較的第二個 columnid。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果 lhs 在 rhs 之前，則為 True。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COLUMNID 結構](./jet-columnid-structure.md)

[JET_COLUMNID 成員](./jet-columnid-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
