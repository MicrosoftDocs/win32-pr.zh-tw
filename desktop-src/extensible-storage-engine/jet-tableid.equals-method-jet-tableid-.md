---
description: '深入瞭解： JET_TABLEID。Equals 方法 (JET_TABLEID) '
title: 'JET_TABLEID。Equals 方法 (JET_TABLEID) '
TOCTitle: Equals method (JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.Equals(Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.equals(v=EXCHG.10)
ms:contentKeyID: 39514708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f4c794e07efd291ddbf75ce5ab697d61f9ebed0db5a3e5ce66aef561fe91fc26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889998"
---
# <a name="jet_tableidequals-method-jet_tableid"></a>JET_TABLEID。Equals 方法 (JET_TABLEID) 

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function Equals ( _
    other As JET_TABLEID _
) As Boolean
'Usage
Dim instance As JET_TABLEID
Dim other As JET_TABLEID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_TABLEID other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IEquatable \<T\> 。等於 (T) ](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_TABLEID 結構](./jet-tableid-structure.md)

[JET_TABLEID 成員](./jet-tableid-members.md)

[等於多載](./jet-tableid.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
