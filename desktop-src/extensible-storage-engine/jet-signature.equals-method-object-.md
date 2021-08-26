---
description: 深入瞭解： JET_SIGNATURE。物件)  (Equals 方法
title: JET_SIGNATURE。物件)  (Equals 方法
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.equals(v=EXCHG.10)
ms:contentKeyID: 39510778
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b05543654592dc610d560e8db7b0b7d61dd8a25420e6797b8d55890673c4377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115998"
---
# <a name="jet_signatureequals-method-object"></a>JET_SIGNATURE。物件)  (Equals 方法

傳回值，這個值表示這個實例是否等於另一個實例。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_SIGNATURE
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a>參數

  - obj  
    類型： [system.object](/dotnet/api/system.object)  
    
    與這個執行個體相互比較的物件。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果兩個實例相等，則為 True。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SIGNATURE 結構](./jet-signature-structure2.md)

[JET_SIGNATURE 成員](./jet-signature-members.md)

[等於多載](./jet-signature.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
