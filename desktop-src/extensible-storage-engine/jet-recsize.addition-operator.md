---
description: 深入瞭解： JET_RECSIZE。加法運算子
title: JET_RECSIZE。 (，) 的加法運算子
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_addition(v=EXCHG.10)
ms:contentKeyID: 39512451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c675e0b7fffc00f181bc56f314ddcbbdac56c9c910abbaa0f88f69ad321bce2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890388"
---
# <a name="jet_recsizeaddition-operator"></a>JET_RECSIZE。加法運算子

將大小新增至兩個 JET_RECSIZE 結構。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Operator + ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left + right)
```

``` csharp
public static JET_RECSIZE operator +(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a>參數

  - left  
    類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    第一個 JET_RECSIZE。

<!-- end list -->

  - 向右  
    類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    第二個 JET_RECSIZE。

#### <a name="return-value"></a>傳回值

類型： [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
JET_RECSIZE，其中包含在左邊和右邊新增大小的結果。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RECSIZE 結構](./jet-recsize-structure2.md)

[JET_RECSIZE 成員](./jet-recsize-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
