---
description: 深入瞭解： JET_COMMIT_ID 等號比較運算子
title: 'JET_COMMIT_ID 的等號比較運算子 (Windows8) '
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Equality(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_equality(v=EXCHG.10)
ms:contentKeyID: 55104297
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Equality
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb259e54141e3e94e6ee106724e4e737334519398c42ceb11c86026417407db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112367"
---
# <a name="jet_commit_idequality-operator"></a>JET_COMMIT_ID 等號比較運算子

判斷其中一個 commitid 是否等於另一個 commitid。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a>參數

  - lhs  
    類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    要比較的第一個 commitid。

<!-- end list -->

  - rhs  
    類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    要比較的第二個 commitid。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果 lhs 等於 rhs，則為 True。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_COMMIT_ID 類別](./jet-commit-id-class.md)

[JET_COMMIT_ID 成員](./jet-commit-id-members.md)

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
