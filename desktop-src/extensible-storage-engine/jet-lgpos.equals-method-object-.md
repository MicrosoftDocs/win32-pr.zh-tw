---
description: 深入瞭解： JET_LGPOS。物件)  (Equals 方法
title: JET_LGPOS。物件)  (Equals 方法
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.equals(v=EXCHG.10)
ms:contentKeyID: 39512677
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0263e0c83c5d757c1b5eef92da0fb1e9bcca927a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978276"
---
# <a name="jet_lgposequals-method-object"></a>JET_LGPOS。物件)  (Equals 方法

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
Dim instance As JET_LGPOS
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

[JET_LGPOS 結構](./jet-lgpos-structure2.md)

[JET_LGPOS 成員](./jet-lgpos-members.md)

[等於多載](./jet-lgpos.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
