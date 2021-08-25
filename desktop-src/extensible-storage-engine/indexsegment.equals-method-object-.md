---
description: 深入瞭解： (物件) IndexSegment Equals 方法
title: " (物件) IndexSegment Equals 方法"
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.IndexSegment.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexsegment.equals(v=EXCHG.10)
ms:contentKeyID: 55103251
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.IndexSegment.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d01af10b308cff4074f3a2b6730d1e6b0481c209033b0e57dbbb47fa4759e8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017758"
---
# <a name="indexsegmentequals-method-object"></a> (物件) IndexSegment Equals 方法

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
Dim instance As IndexSegment
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

[IndexSegment 類別](./indexsegment-class.md)

[IndexSegment 成員](./indexsegment-members.md)

[等於多載](./indexsegment.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
