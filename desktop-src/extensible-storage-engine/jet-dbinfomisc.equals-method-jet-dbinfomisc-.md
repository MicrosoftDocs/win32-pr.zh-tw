---
description: '深入瞭解： JET_DBINFOMISC。Equals 方法 (JET_DBINFOMISC) '
title: 'JET_DBINFOMISC。Equals 方法 (JET_DBINFOMISC) '
TOCTitle: Equals method (JET_DBINFOMISC)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals(Microsoft.Isam.Esent.Interop.JET_DBINFOMISC)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.equals(v=EXCHG.10)
ms:contentKeyID: 39514332
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbe29fe112b82b5c88673d9301b3feb4b0c94536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112129"
---
# <a name="jet_dbinfomiscequals-method-jet_dbinfomisc"></a>JET_DBINFOMISC。Equals 方法 (JET_DBINFOMISC) 

指出目前的物件是否等於另一個相同類型的物件。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Function Equals ( _
    other As JET_DBINFOMISC _
) As Boolean
'Usage
Dim instance As JET_DBINFOMISC
Dim other As JET_DBINFOMISC
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_DBINFOMISC other
)
```

#### <a name="parameters"></a>參數

  - 其他  
    類型： [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)  
    
    要與此物件進行比較的物件。

#### <a name="return-value"></a>傳回值

型別： [system.object](/dotnet/api/system.boolean)  
如果目前的物件等於另一個參數，則為 True;否則為 false。  

#### <a name="implements"></a>實作

[IEquatable \<T\> 。等於 (T) ](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_DBINFOMISC 類別](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC 成員](./jet-dbinfomisc-members.md)

[等於多載](./jet-dbinfomisc.equals-method.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
