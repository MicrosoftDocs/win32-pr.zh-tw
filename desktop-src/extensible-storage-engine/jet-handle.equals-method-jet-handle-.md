---
description: '深入瞭解： JET_HANDLE。Equals 方法 (JET_HANDLE) '
title: 'JET_HANDLE。Equals 方法 (JET_HANDLE) '
TOCTitle: Equals method (JET_HANDLE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals(Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.equals(v=EXCHG.10)
ms:contentKeyID: 39515292
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a08fae12ee7928f40df4ea6244e2666af3f629d21ad35a1bb21314eeec664767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617118"
---
# <a name="jet_handleequals-method-jet_handle"></a>JET_HANDLE。Equals 方法 (JET_HANDLE) 

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function Equals ( _
    other As JET_HANDLE _
) As Boolean
'Usage
Dim instance As JET_HANDLE
Dim other As JET_HANDLE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_HANDLE other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IEquatable \<T\> 。等於 (T) ](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_HANDLE 結構](./jet-handle-structure.md)

[JET_HANDLE 成員](./jet-handle-members.md)

[等於多載](./jet-handle.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
