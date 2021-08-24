---
description: 深入瞭解： JET_DBINFOMISC。物件)  (Equals 方法
title: JET_DBINFOMISC。物件)  (Equals 方法
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.equals(v=EXCHG.10)
ms:contentKeyID: 39513216
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46be2130cbb57cc216f570e944d6959ae355780134f90bc94101d01d6f38bb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617598"
---
# <a name="jet_dbinfomiscequals-method-object"></a>JET_DBINFOMISC。物件)  (Equals 方法

判斷指定的 [物件](/dotnet/api/system.object) 是否等於目前的 [物件](/dotnet/api/system.object)。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_DBINFOMISC
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
    
    要與目前[物件](/dotnet/api/system.object)比較的[物件](/dotnet/api/system.object)。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果指定的 [物件](/dotnet/api/system.object) 等於目前的 [物件](/dotnet/api/system.object)，則為 True;否則為 false。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[等於多載](./jet-dbinfomisc.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
