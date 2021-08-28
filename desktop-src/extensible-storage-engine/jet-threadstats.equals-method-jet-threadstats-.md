---
description: '深入瞭解： JET_THREADSTATS。Equals 方法 (JET_THREADSTATS) '
title: JET_THREADSTATS。Equals 方法 (JET_THREADSTATS)  (的) 。
TOCTitle: Equals method (JET_THREADSTATS)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equals(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.equals(v=EXCHG.10)
ms:contentKeyID: 39515931
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 391a4eb50f5b3dcf599c89296e36ca1f683d6594e8edd0c90254c431ea792e26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832598"
---
# <a name="jet_threadstatsequals-method-jet_threadstats"></a>JET_THREADSTATS。Equals 方法 (JET_THREADSTATS) 

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function Equals ( _
    other As JET_THREADSTATS _
) As Boolean
'Usage
Dim instance As JET_THREADSTATS
Dim other As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_THREADSTATS other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    要與這個實例比較的實例。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

#### <a name="implements"></a>實作

[IEquatable \<T\> 。等於 (T) ](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_THREADSTATS 結構](./jet-threadstats-structure2.md)

[JET_THREADSTATS 成員](./jet-threadstats-members.md)

[等於多載](./jet-threadstats.equals-method.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
